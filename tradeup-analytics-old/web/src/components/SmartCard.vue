<template>
  <b-card 
    no-body 
    class="overflow-hidden" 
    style="min-width: 300px; min-height: 240px">
     <img 
      :src="src"
      class="my-auto mx-auto"
      width="213px"
      height="60px"
    >
  </b-card>
</template>

<script>
export default {
  name: "SmartCard",
  props: {
    src: String
  },
  mounted () {
    console.log(this.src)
  }
};
</script>

<style lang="scss" scoped>
.card {
  background: #ffffff;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
}
</style>
