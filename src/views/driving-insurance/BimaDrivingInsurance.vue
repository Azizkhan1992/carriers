<template>
    <div class="driving-insurance-container">
        <driving-insurance-header/>
        <driving-insurance-content/>
    </div>
</template>
<script>
    import DrivingInsuranceHeader from '@/components/driving-insurance-items/DrivingInsuranceHeader.vue';
    import DrivingInsuranceContent from '@/components/driving-insurance-items/DrivingInsuranceContent.vue'
export default {
    name: 'driving-insurance',
    components: {DrivingInsuranceHeader, DrivingInsuranceContent}
}
</script>