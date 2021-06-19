<template>
  <q-btn
    flat
    dense
    round
    class="btn-container"
    :icon="isFav ? 'favorite' : 'o_favorite_border'"
    :color="isFav ? 'red' : 'white'"
    @click="isFav = !isFav"
  />
</template>

<script>
export default {
  name: "Like",
  data() {
    return {
      isFav: false
    };
  }
};
</script>

<style>
.btn-container {
  padding: 5px;
  border-radius: 100%;
  background: #999999a8;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
