<template>
  <div id="app">
    <HeaderComponent></HeaderComponent>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <router-view/>
        </div>
      </div>
    </div>
    <FooterComponent></FooterComponent>
  </div>
</template>
<script>
import HeaderComponent from '@/components/HeaderComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';

export default {
  components: {
    HeaderComponent,
    FooterComponent,
  },
};
</script>
