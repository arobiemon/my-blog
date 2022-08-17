<template>
  <div class="main_menu">
    <div class="q-pa-md">
      <q-toolbar class="bg-purple text-white shadow-2 rounded-borders">
        <q-img
          style="max-height: 50px; max-width:55px"
          src="../assets/logo.jpg"
          alt="logo"
        ></q-img>

        <q-btn style="margin-left: 5px" flat no-caps label="Move Bangladesh" />
        <q-space />

        <!--
        notice shrink property since we are placing it
        as child of QToolbar
      -->
        <q-tabs v-model="tab" shrink>
          <q-tab
            no-caps
            class="q-mr-sm my-tab"
            name="tab1"
            label="Parking bd"
          />
          <q-tab no-caps class="q-mr-sm my-tab" name="tab2" label="Contact" />
          <q-btn-dropdown no-caps flat label="Service">
            <div class="column">
              <q-btn
                color="green"
                unelevated
                dense
                icon="facebook"
                label="Facebook"
                no-caps
              ></q-btn>
              <q-btn
                color="green"
                unelevated
                dense
                icon="facebook"
                label="Facebook"
                no-caps
              ></q-btn>
              <q-btn
                color="green"
                unelevated
                dense
                icon="facebook"
                label="Facebook"
                no-caps
              ></q-btn>
              <q-btn
                color="green"
                unelevated
                dense
                icon="facebook"
                label="Facebook"
                no-caps
              ></q-btn>
            </div>
          </q-btn-dropdown>
          <q-tab no-caps class="q-mr-sm my-tab" name="tab3" label="About" />
          <q-tab no-caps class="q-mr-sm my-tab" name="tab3" label="Home" />
        </q-tabs>
      </q-toolbar>
    </div>
    <head>
      <title>Move Bangladesh</title>
    </head>
  </div>
  <div class="q-pa-md">
    <q-form @submit="onSubmit" class="q-gutter-md">
      <q-input
        name="name"
        v-model="name"
        color="primary"
        label="Full name"
        filled
        clearable
      />

      <div>
        <q-btn label="Submit" type="submit" color="primary" />
      </div>
    </q-form>

    <q-card
      v-if="submitResult.length > 0"
      flat
      bordered
      class="q-mt-md bg-grey-2"
    >
      <q-card-section
        >Submitted form contains the following formData (key =
        value):</q-card-section
      >
      <q-separator />
      <q-card-section class="row q-gutter-sm items-center">
        <div
          v-for="(item, index) in submitResult"
          :key="index"
          class="q-px-sm q-py-xs bg-grey-8 text-white rounded-borders text-center text-no-wrap"
        >
          {{ item.name }} = {{ item.value }}
        </div>
      </q-card-section>
    </q-card>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const submitResult = ref([]);

    return {
      tab: ref(""),
      name: ref("Jane Doe"),
      submitResult,

      onSubmit(evt) {
        const formData = new FormData(evt.target);
        const data = [];

        for (const [name, value] of formData.entries()) {
          data.push({
            name,
            value,
          });
        }

        submitResult.value = data;
      },
    };
  },
};
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
}

ul li {
  list-style: none;
}
a {
  text-decoration: none;
  display: inline-block;
}
.main_menu {
  background-image: url(../assets/banner.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 600px;
}

.main_menu ul li a {
  float: right;
  color: #000;
  line-height: 60px;
  padding: 0 40px;
  font-size: 20px;
  position: relative;
}
.main_menu ul li a:hover {
  color: coral;
}
.pregraph {
  /* float: right; */
  font-family: sans-serif;
  color: brown;
  font-size: 20px;
  float: right;
}
footer {
  /* background-color:cornflowerblue; */
  font-family: sans-serif;
}
h2 {
  /* background-color: cornflowerblue; */
  float: right;
}

.main_menu ul ul {
  display: none;
}
.main_menu ul li:hover > ul {
  display: block;
}

.my-tab {
  margin-right: 15px;
}
</style>
