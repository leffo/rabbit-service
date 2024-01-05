<template>
  <primary-header></primary-header>
  <main class="main">
    <router-view></router-view>
  </main>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PrimaryHeader from "./components/PrimaryHeader.vue";

export default defineComponent({
  components: { PrimaryHeader },
  setup() {
    return {
      username: 'Alex Huj'
    };
  },
});
</script>

<style lang="less" scoped>
.main {
  width: 992px;
  margin: 0 auto;
  padding: 20px;
}
</style>
