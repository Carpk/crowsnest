<script setup>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <lightgallery
    :settings="{ speed: 500, plugins: plugins }"
    :onInit="onInit"
    :onBeforeSlide="onBeforeSlide"
  >
    <a
      data-lg-size="1406-1390"
      class="gallery-item"
      data-src="/IMG_0007.jpg"
      data-sub-html="<h4>Larry 'Bear' Crow</h4> <p> unknown - unknown</p>"
    >
      <img
        class="img-responsive"
        style="width: 250px;"
        src="/IMG_0007.jpg"
      />
    </a>
    <a
      class="gallery-item"
      data-src="/IMG_0008.jpg"
      data-sub-html="<h4>Larry 'Bear' Crow</h4> <p> unknown - unknown</p>"
    >
      <img
        class="img-responsive"
        style="width: 250px;"
        src="/IMG_0008.jpg"
      />
    </a>
    <a
      class="gallery-item"
      data-src="/IMG_0012.jpg"
      data-sub-html="<h4>Larry 'Bear' Crow</h4> <p> unknown - unknown</p>"
    >
      <img
        class="img-responsive"
        style="width: 250px;"
        src="/IMG_0012.jpg"
      />
    </a>


    
  </lightgallery>
</template>


<script>
import Lightgallery from 'lightgallery/vue';
import lgZoom from 'lightgallery/plugins/zoom';
import lgVideo from 'lightgallery/plugins/video';

export default {
  name: 'App',
  components: {
    Lightgallery,
  },
  data: () => ({
    plugins: [lgZoom, lgVideo],
  }),
  methods: {
    onInit: () => {
      console.log('lightGallery has been initialized');
    },
    onBeforeSlide: () => {
      console.log('calling before slide');
    },
  },
};
</script>
<style lang="css">
@import 'lightgallery/css/lightgallery.css';
@import 'lightgallery/css/lg-zoom.css';
@import 'lightgallery/css/lg-video.css';
body {
  margin: 0;
}
.gallery-item {
  margin: 5px;
}
</style>
