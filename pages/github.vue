<template>
    <div class="w-full z-0 bg-img section h-content" style="background-image: url(bg-img3.jpg)">
        <Header/>
        <div class="pt-20 md:pt-15 pb-3 md:pb-10 max-w-7xl mx-auto px-6">
            <div class="pb-6 text-3xl md:text-5xl font-semibold text-gray-800">
                GitHub
            </div>
            <div class="font-normal text-base md:text-xl text-gray-600">
                ZeroPage Github의 사용법에 대한 글이에요 
            </div>
        </div>

        <Search />

        <div class="max-w-7xl grid grid-cols-1 colspan mt-5 md:mt-8 pb-14 md:pb-24 mx-auto px-6">
            <div class="group" v-for="article of articles" :key="article">
                <nuxt-link :to='`article/${article.slug}`'>
                    <div class="article-inner flex items-center border-t py-5 md:py-8 border-gray-600">
                  <div class="sbox hidden md:block group-hover:shadow-lg transform group-hover:scale-105 transition group-hover:duration-500">
                    <img class="profile" :src="require(`~/assets/resources/${article.img}`)" alt="">
                  </div>
                  <div class="px-0 md:px-4 md:pl-9">
                      <p class="mb-1 md:mb-1.5 text-sm md:text-sm text-blue-900">{{article.category}} · ZeroPage</p>
                      <h2 class="mb-1 md:mb-1.5 text-lg md:text-xl font-medium  text-gray-800 transition group-hover:text-blue-500 group-hover:duration-500">{{ article.title }}</h2>
                      <p class=" text-sm md:text-base text-gray-600 custom-text">{{article.description}}</p>
                  </div>
                </div>
                </nuxt-link>
            </div>
        </div>
        <Footer />
    </div>

</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const articles = await $content('article', params.slug)
      .where({category: 'github'})
    //   .sortBy('createdAt', 'desc')
      .fetch();
    return {
      articles
    }
  },
    head: {
        title: 'ZeroPage GitHub',
        htmlAttrs: {
        lang: 'ko'
        },
        meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        { hid: 'description', name: 'description', content: 'ZeroPage Main manual' },
        { name: 'format-detection', content: 'telephone=no' }
        ]
    },
}
</script>

<style scoped>
.keepall{
    word-break: keep-all;
}

.profile {
  width: 100%;
  height: 100%;
  object-fit: 100%;
}
.sbox {
  width: 212px;
  height: 141.33px;
  border-radius: 0.75rem;
  overflow: hidden;
}
.bg-img {
        background-position: center;
        background-repeat:  no-repeat;
        background-size:  cover;
        background-color: #FFFFFF;
 }
 .section {
  position: relative;
}
</style>