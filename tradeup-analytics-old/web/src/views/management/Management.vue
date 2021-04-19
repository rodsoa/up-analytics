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
                    <!--b-form-input
                      id="comapany"
                      v-model="form.company"
                      type="text"
                      placeholder="Digita nome da empresa"
                      required
                    ></b-form-input-->
                    <vue-bootstrap-typeahead
                      id="company"
                      :data="[
                        'Empresa teste 1',
                        'Empresa teste 2',
                        'Empresa teste 3',
                        'Empresa teste 4',
                        'Empresa teste 5'
                      ]"
                      v-model="form.company"
                    />
                  </b-form-group>
                </div>

                <div class="row">
                  <b-form-group
                    id="module-group"
                    label="Módulo"
                    label-for="module"
                    class="col-sm-6"
                  >
                    <b-form-input
                      id="input-2"
                      v-model="form.module"
                      placeholder="Digite o módulo"
                      required
                    ></b-form-input>
                  </b-form-group>

                  <b-form-group
                    id="dashboard-input-group"
                    label="Dashboard"
                    label-for="dashboard"
                    class="col-sm-6"
                  >
                    <b-form-input
                      id="dashboard"
                      v-model="form.dashboard"
                      required
                    ></b-form-input>
                  </b-form-group>
                </div>

                <div class="row">
                  <b-form-group
                    id="report-id-group"
                    label="Report ID"
                    label-for="report-id"
                    class="col-sm-6"
                  >
                    <b-form-input
                      id="report-id"
                      v-model="form.report_id"
                      placeholder="Digite o report id"
                      required
                    ></b-form-input>
                  </b-form-group>

                  <b-form-group
                    id="group-id-group"
                    label="Group ID"
                    label-for="group-id"
                    class="col-sm-6"
                  >
                    <b-form-input
                      id="group-id"
                      v-model="form.group_id"
                      required
                    ></b-form-input>
                  </b-form-group>
                </div>

                <div class="row">
                  <b-form-group
                    id="secret-id-group"
                    label="Secret ID"
                    label-for="secret-id"
                    class="col-sm-6"
                  >
                    <b-form-input
                      id="secret-id"
                      v-model="form.secret_id"
                      placeholder="Digite o secret id"
                      required
                    ></b-form-input>
                  </b-form-group>

                  <b-form-group
                    id="url-group"
                    label="Url"
                    label-for="url"
                    class="col-sm-6"
                  >
                    <b-form-input
                      id="group-id"
                      v-model="form.url"
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
      data: [
        'Empresa teste 1',
        'Empresa teste 2',
        'Empresa teste 3',
        'Empresa teste 4',
        'Empresa teste 5'
      ],
      selectedCompany: null,
      form: {
        company: "",
        module: "",
        dashboard: "",
        report_id: "",
        group_id: "",
        secret_id: "",
        url: ""
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
        this.form.module = "";
        this.form.dashboard = "";
        this.form.report_id = "";
        this.form.group_id = "";
        this.form.secret_id = "";
        this.form.url = "";
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
