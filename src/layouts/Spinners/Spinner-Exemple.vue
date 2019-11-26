<template>
  <v-dialog persistent fullscreen :transition="false" v-model="loading">
    <v-row justify="center" class="bg-loader" align="center" no-gutters>
      <orbit-spinner :animation-duration="1500" :size="100" color="blue" />
    </v-row>
  </v-dialog>
</template>

<script>
import { OrbitSpinner } from "epic-spinners";
export default {
  components: {
    OrbitSpinner
  },
  computed: {
    loading() {
      return true; //Substituir por getter do vuex que retorna um estado;
    }
  }
};
</script>

<style scoped>
.bg-loader {
  height: 100%;
  background-color: rgba(39, 39, 107, 0.384);
  position: relative;
}
</style>
