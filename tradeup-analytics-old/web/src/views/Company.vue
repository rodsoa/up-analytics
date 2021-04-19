<template>
  <div class="container">
    <div class="row">
        <b-card
            title="Vendas"
            style="width: 293px; height: 220px"
            class="text-center"
            @click="goto()"
        >
            <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
            </b-card-text>

            <b-button block variant="primary">Visualizar</b-button>
        </b-card>

        <b-card
            title="Qualidade"
            style="width: 293px; height: 220px"
            class="text-center"
            @click="goto()"
        >
            <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
            </b-card-text>

            <b-button block variant="primary">Visualizar</b-button>
        </b-card>

        <b-card
            title="Contábil"
            style="width: 293px; height: 220px"
            class="text-center"
            @click="goto()"
        >
            <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
            </b-card-text>

            <b-button block variant="primary">Visualizar</b-button>
        </b-card>

        <b-card
            title="Help Desk"
            style="width: 293px; height: 220px"
            class="text-center"
            @click="goto()"
        >
            <b-card-text>
                Some quick example text to build on the card title and make up the bulk of the card's content.
            </b-card-text>

            <b-button block variant="primary">Visualizar</b-button>
        </b-card>

        <b-card
            title="DRE"
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
  name: 'Company',
  methods: {
    goto () {
      this.$router.push('/dashboard');
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
