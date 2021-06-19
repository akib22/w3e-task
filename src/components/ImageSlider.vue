<template>
  <div class="p-relative">
    <q-carousel animated v-model="slide" arrows infinite>
      <q-carousel-slide
        :name="1"
        img-src="https://cdn.quasar.dev/img/mountains.jpg"
      />
      <q-carousel-slide
        :name="2"
        img-src="https://cdn.quasar.dev/img/parallax1.jpg"
      />
      <q-carousel-slide
        :name="3"
        img-src="https://cdn.quasar.dev/img/parallax2.jpg"
      />
      <q-carousel-slide
        :name="4"
        img-src="https://cdn.quasar.dev/img/quasar.jpg"
      />
    </q-carousel>
    <div class="p-absolute like">
      <like />
    </div>
    <div class="p-absolute rating">
      <div class="flex align-center">
        <q-icon name="star" size="24px" color="green-6" />
        <span class="text-subtitle1 text-white text-weight-medium">4.8</span
        >
      </div>
    </div>
    <div class="p-absolute slider-state">
      <p class="text-subtitle1 text-white text-weight-medium">{{ slide }}/4</p>
    </div>
  </div>
</template>

<script>
import Like from "./Like.vue";

export default {
  components: { Like },
  data() {
    return {
      slide: 1
    };
  }
};
</script>

<style scoped>
.like {
  right: 5px;
  top: 5px;
}
.rating {
  left: 5px;
  bottom: 5px;
}
.slider-state {
  right: 5px;
  bottom: 5px;
}
</style>
