<template>
  <q-input
    dark
    dense
    rounded
    standout
    v-model="searchValue"
    @focus="showInput = true"
    @blur="showInput = false"
    input-class="text-right"
    :style="{'width': showInput ? '150px' : '40px'}"
    class="q-ml-md"
  >
    <template v-slot:append>
      <q-icon v-if="searchValue === ''" name="search" />
      <q-icon v-else name="clear" class="cursor-pointer" @click="searchValue = ''" />
    </template>
  </q-input>
</template>

<script>
export default {
  name: "Search",
  data() {
    return {
      showInput: false,
      searchValue: ""
    };
  }
};
</script>
