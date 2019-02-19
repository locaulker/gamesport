<template>
  <div>
    <comp-carousel/>
    <comp-content/>
  </div>
</template>

<script>
  import compCarousel from './carousel.vue';
  import compContent from './content.vue';

  export default {
    components: {
      compCarousel,
      compContent
    }
  }
</script>