<template>
  <div class="container">
    <div class="row">
      <div class="col-12">
        <section>
          <b-card-group>
            <b-card>
              <b-form @submit="onSubmit" @reset="onReset" v-if="show">
                <div class="row">
                  <b-form-group
                    id="company-input-group"
                    label="Empresa"
                    label-for="company"
                    class="col-sm-12"
                  >
                    <b-form-input
                      id="group-id"
                      v-model="form.company"
                      required
                    ></b-form-input>
                  </b-form-group>

                  <b-form-group
                    id="url-group"
                    label="Url"
                    label-for="url"
                    class="col-sm-12"
                  >
                    <b-form-input
                      id="group-id"
                      v-model="form.icone"
                      required
                    ></b-form-input>
                  </b-form-group>
                </div>
                <div class="float-right">
                    <b-button type="submit" variant="secondary" class="mr-2">Ocultar</b-button>
                    <b-button type="reset" variant="secondary">Salvar</b-button>
                </div>
              </b-form>
              <b-card class="mt-5" header="Form Data Result">
                <pre class="m-0">{{ form }}</pre>
              </b-card>
            </b-card>
          </b-card-group>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Management",
  data() {
    return {
      form: {
        company: "",
        icone: ""
      },
      show: true,
    };
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(event) {
      event.preventDefault();
      // Reset our form values
      this.form.company = "";
      this.form.icone = "";
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.container {
  padding-top: 5%;
}
</style>