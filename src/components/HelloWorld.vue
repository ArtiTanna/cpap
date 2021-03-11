<template>
  <div id="app" class="full-height" style="width: 70%">
    <vueper-slides :class="`font-light leading-tight`">
      <vueper-slide
        style="font-size: 75px;"
        v-for="(slide, i) of slides"
        :key="i"
        title="Travel Smarter, Not Harder"
        :content="slide.content"
        :style="`background-color: ${colors[i % colors.length]}`"
      />
    </vueper-slides>
  </div>
</template>
<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
export default {
  name: "App",
  components: { VueperSlides, VueperSlide },
  data() {
    return {
      colors: ["#DFCFBE", "#EFC050", "#5B5EA6"],
      slides: [{
        content: '<button style="padding: 6px; background-color: inherit;" v-on:click="say()">LEARN MORE</button> <button style="padding: 6px; background-color: inherit;" v-on:click="say()">SHOP RESMED</button>',
        title: "Slide 1"
      },
      {
        content: '<button style="padding: 6px; background-color: inherit;" v-on:click="say()">LEARN MORE</button> <button style="padding: 6px; background-color: inherit;" v-on:click="say()">SHOP RESMED</button>',
        title: "Slide 2"
      },
      {
        content: '<button style="padding: 6px; background-color: inherit;" v-on:click="say()">LEARN MORE</button> <button style="padding: 6px; background-color: inherit;" v-on:click="say()">SHOP RESMED</button>',
        title: "Slide 3"
      }]
    };
  }
};
</script>
<style>
.vueperslides__bullet .default {
  background-color: rgba(0, 0, 0, 0.3);
  border: none;
  box-shadow: none;
  transition: 0.3s;
  width: 16px;
  height: 16px;
}
.vueperslides__bullet--active .default {
  background-color: #42b983;
}
.vueperslides__bullet span {
  display: block;
  color: #fff;
  font-size: 10px;
  opacity: 0.8;
}

html, body {
  height: 100%;
}

.full-height {
  height: 100%;
}


</style>