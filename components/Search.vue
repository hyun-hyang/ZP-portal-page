<template>
      <div class="max-w-7xl mx-auto px-6 pt-1 md:pt-0 md:0b-0">
        <div class="shadow-sm md:shadow w-full rounded-2xl border border-gray-800 flex items-center mb-4 py-3 md:py-3.5 px-5 bg-white">
            <SearchIcon />
            <input placeholder="궁금한 것을 검색해보세요!" v-model="query" type="search" autocomplete="off" 
            class="ml-3 bg-white flex-auto text-base text-gray-800 pr-3.5 md:pr-6 flex items-center placeholder-text-gray-400" />
        </div>

        <ul v-if="articles.length" class="shadow-sm md:shadow rounded-lg border border-gray-300 px-4 bg-white">
          <li class="text-gray-600 py-2.5 md:py-3.5 border-b text-base lastborder" v-for="article of articles" :key="article.slug">
            <!-- <NuxtLink :to="{ name: 'slug', pa`rams: { slug: article.slug } }"> -->
            <nuxt-link :to='`article/${article.slug}`'>
              {{ article.title }}
            </nuxt-link>
          </li>
        </ul>
      </div>
</template>

<script>
export default {
  data () {
    return {
      query: '',
      articles: []
    }
  },
  watch: {
    async query (query) {
      if (!query) {
        this.articles = []
        return
      }

      this.articles = await this.$content('article')
        .only(['title', 'slug'])
        .sortBy('title')
        .limit(15)
        .search(query)
        .fetch()
    }
  }
}
</script>

<style scoped>
.lastborder:last-child{
    border-bottom: none;
}
input:focus, textarea:focus, select:focus{
        outline: none;
    }
input::-ms-clear,
input::-ms-reveal{
	display:none;width:0;height:0;
}
input::-webkit-search-decoration,
input::-webkit-search-cancel-button,
input::-webkit-search-results-button,
input::-webkit-search-results-decoration{
	display:none;
}
</style>