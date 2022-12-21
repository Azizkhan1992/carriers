<template>
  <div class="contacts-content">
    <div class="contacts-wrapper">
      <div class="contacts-inner-wrapper">
        <div class="our-contacts">
          <content-one-item />
        </div>
        <div class="write-us">
          <content-two-item />
        </div>
        <div class="our-location">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d6237.556249047512!2d68.75108829547624!3d38.58495692806504!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38b5d3db8a27940f%3A0x51826fa63e2c19d5!2z0KHRgtGA0LDRhdC-0LLQsNGPINC-0YDQs9Cw0L3QuNC30LDRhtC40Y8gwqvQkdCY0JzQkMK7!5e0!3m2!1sru!2s!4v1665126684003!5m2!1sru!2s"
            width="100%"
            height="500"
            style="border: 0"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import ContentOneItem from "./ContentOneItem.vue";
import ContentTwoItem from "./ContentTwoItem.vue";
export default {
  name: "contacts-content",
  components: { ContentOneItem, ContentTwoItem },
};
</script>
