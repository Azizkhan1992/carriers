<template>
    <div class="bima-news-container">
        <news-header/>
        <bima-news-items/>
    </div>
</template>
<script>
    import NewsHeader from '@/components/news/NewsHeader.vue';
    import BimaNewsItems from '@/components/news/BimaNewsItems.vue'
export default {
    name: 'bima-news',
    components: {NewsHeader, BimaNewsItems}
}
</script>