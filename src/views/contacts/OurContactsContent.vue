<template>
    <div class="our-contacts-container">
        <bima-contacts-header/> 
        <bima-contacts-content/>
    </div>
</template>
<script>
    import BimaContactsHeader from '@/components/contact-items/BimaContactsHeader.vue';
    import BimaContactsContent from '@/components/contact-items/BimaContactsContent.vue'
export default {
    name: 'our-contacts',
    components: {BimaContactsHeader, BimaContactsContent}
}
</script>