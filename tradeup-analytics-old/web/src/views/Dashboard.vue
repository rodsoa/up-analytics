<template>
  <div class="container">
    <div class="row">
        <b-card
            title="Força de Venda"
            style="width: 293px; height: 220px"
            class="text-center"
            @click="goto()"
        >
            <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
            </b-card-text>

            <b-button block variant="primary">Visualizar</b-button>
        </b-card>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Dashboard',
  methods: {
    goto () {
      console.log('EXIBIR FULLSCREEN');
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