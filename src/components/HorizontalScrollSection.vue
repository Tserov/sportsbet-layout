<template>
    <div>
        <h2 class="section-title">{{heading}}</h2>
        <vue-custom-scrollbar class="scroll-area container px-0"
                              :settings="settings" @ps-scroll-y="scrollHanle">
                              <div class="d-flex pb-3 pt-2">
                                <slot></slot>
                              </div>
        </vue-custom-scrollbar>
    </div>
</template>

<script>
import vueCustomScrollbar from 'vue-custom-scrollbar';

export default {
  props: ['heading'],
  name: 'HorizontalScrollSection',
  components: {
    vueCustomScrollbar,
  },
  data() {
    return {
      settings: {
        maxScrollbarLength: 450,
      },
    };
  },
  methods: {
    scrollHanle(evt) {
      console.log(evt);
    },
  },
};
</script>
<style >
.scroll-area {
  position: relative;
  margin: auto;
  height: auto;
}
.ps__rail-x.ps--clicking .ps__thumb-x,
.ps__rail-x:focus>.ps__thumb-x,
.ps__rail-x:hover>.ps__thumb-x{
    height: 6px !important;
}
.ps .ps__rail-x.ps--clicking,
.ps .ps__rail-x:focus,
.ps .ps__rail-x:hover,
.ps .ps__rail-y.ps--clicking,
.ps .ps__rail-y:focus, .ps .ps__rail-y:hover{
    background: transparent !important;
}
</style>
