<template>
    <div class="flex justify-between pt-12 px-3">
        <div class="w-5/12 ml-3 md:ml-0 bg-zinc-900  border-2 border-gray-400 md:border-gray-300 hover:border-gray-400 rounded-lg md:rounded-xl p-3 md:px-8 md:py-6 group transition duration-300">
            <!-- <NuxtLink v-if="prev" :to="{ name: 'slug', params: { slug: prev.slug } }"> -->
            <NuxtLink v-if="prev" :to='`${prev.slug}`'>
                <div class="text-center md:text-left text-white">Previous Post</div>
                <div class="hidden md:block text-white font-medium mt-1 custom-text">{{ prev.title }}</div>
            </NuxtLink>
            <nuxt-link v-else to='/'>
                        <div class="text-center md:text-left text-white">No Previous Post</div>
                        <div class="hidden md:block text-white font-medium mt-1">
                            <span>홈으로 돌아가기</span>
                        </div>
            </nuxt-link>
        </div>
        <div class="w-5/12 mr-3 md:mr-0 bg-zinc-900   border-2 border-gray-400 md:border-gray-300 hover:border-gray-400 rounded-lg md:rounded-xl p-3 md:px-8 md:py-6 group transition duration-300">
            <!-- <NuxtLink v-if="next" :to="{ name: 'slug', params: { slug: next.slug } }"> -->
            <NuxtLink v-if="next" :to='`${next.slug}`'>
                <div class="text-center md:text-right text-white">Next Post</div>
                <div class="hidden md:block text-right text-white font-medium mt-1 custom-text">{{ next.title }}</div>
            </NuxtLink>
            <nuxt-link v-else to='/'>
                <div class="text-center md:text-right text-white">No Next Post</div>
                <div class="hidden md:block text-right text-white font-medium mt-1">
                    <span>홈으로 돌아가기</span>
                </div>
            </nuxt-link>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
        prev: {
            type: Object,
            default: () => null
        },
        next: {
            type: Object,
            default: () => null
        }
        }
    }
</script>

<style scoped>
.custom-text{
    word-break: keep-all;
}
</style>