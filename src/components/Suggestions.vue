<template>
  <div :class="show ? 'container' : 'overflow-hidden container'">
    <div class="flex column flex-center">
      <q-icon size="25px" name="eva-minus-outline" @click="show = !show" />
      <h5>More Great Options in LONDON</h5>
      <span class="text-grey text-subtitle1">33 Slaces to Stay</span>
    </div>
    <div :class="show ? 'transition h-80' : 'transition h-0'">
      <card :hotDeal="true" />
      <card />
      <card :hotDeal="true" />
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "Suggestion",
  components: { Card },
  data() {
    return {
      show: false,
      height: "130px"
    };
  }
};
</script>

<style scoped>
.container {
  background: white;
  border-top-left-radius: 15px;
  border-top-right-radius: 15px;
  border-top: 1px solid #8080805e;
  padding: 0 10px;
  transition: all 1s ease;
  overflow-y: scroll;
  box-shadow: rgb(101 119 134 / 20%) 0px 0px 15px,
    rgb(101 119 134 / 15%) 0px 0px 3px 1px;
}

.overflow-hidden {
  overflow: hidden;
}

.transition {
  transition: all 0.3s ease 0s;
}

.h-80 {
  height: 70vh;
}

.h-0 {
  height: 0px;
}

.p-fixed {
  position: fixed;
  top: 0;
}
</style>
