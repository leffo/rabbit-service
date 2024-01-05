<template>
  <h1>Counter: {{ counter }}</h1>
  <button class="btn btn-success"
          @click="increment"
  >
    Increment
  </button>
</template>

<script lang='ts'>
import { defineComponent, computed } from 'vue'
import { useStore } from "vuex";

export default defineComponent({
  name: "SomePage",

  components: {},
  setup() {
    const store = useStore();

    const counter = computed(() => {
      return store.state.count;
    });

    const increment = () => {
      store.commit('increment')
    }

    return {
      counter,
      increment
    };
  }
})
</script>

<style scoped lang="less">

</style>
