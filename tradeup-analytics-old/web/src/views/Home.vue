<template>
  <div class="container">
    <div class="row">
      <b-card 
        no-body 
        class="overflow-hidden round" 
        style="min-width: 300px; min-height: 240px"
        @click="goto()"
        >
        <img 
          src="../assets/tradeup.png"
          class="my-auto mx-auto"
          width="213px"
          height="60px"
        >
      </b-card>

      <b-card 
        no-body 
        class="overflow-hidden" 
        style="min-width: 300px; min-height: 240px">
        <img 
          src="../assets/claro.png"
          class="my-auto mx-auto"
          width="213px"
          height="60px"
        >
      </b-card>

      <b-card 
        no-body 
        class="overflow-hidden" 
        style="min-width: 300px; min-height: 240px">
        <img 
          src="../assets/tim.png"
          class="my-auto mx-auto"
          width="213px"
          height="60px"
        >
      </b-card>

      <b-card 
        no-body 
        class="overflow-hidden" 
        style="min-width: 300px; min-height: 240px">
        <img 
          src="../assets/mcafee.png"
          class="my-auto mx-auto"
          width="213px"
          height="60px"
        >
      </b-card>

      <b-card 
        no-body 
        class="overflow-hidden" 
        style="min-width: 300px; min-height: 240px">
        <img 
          src="../assets/tao.png"
          class="my-auto mx-auto"
          width="213px"
          height="60px"
        >
      </b-card>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
  methods: {
    goto () {
      this.$router.push('/company');
    }
  }
}

</script>

<style lang="scss" scoped>
  .row {
    margin-top: 15%;
    .card {
      margin-right: 69px;
      margin-bottom: 69px;
    }
  }
</style>
