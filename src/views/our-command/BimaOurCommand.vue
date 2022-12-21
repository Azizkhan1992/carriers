<template>
    <div class="our-group-container">
        <our-group-header/>
        <our-group-content/>
    </div>
</template>
<script>
    import OurGroupHeader from '@/components/our-group/OurGroupHeader.vue';
    import OurGroupContent from '@/components/our-group/OurGroupContent.vue'
export default {
    name: 'our-command',
    components: {OurGroupHeader, OurGroupContent}
}
</script>