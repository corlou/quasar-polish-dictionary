<template>
  <div class="q-pa-md q-gutter-sm">
    <q-breadcrumbs>
      <q-breadcrumbs-el label="Home" to="/" />
      <q-breadcrumbs-el label="Food" to="/food" />
      <q-breadcrumbs-el label="Grains - Ziarna" />
    </q-breadcrumbs>
  </div>
  <div class="q-pa-md row items-start q-gutter-md">
    <q-card v-for="grains in ziarna" :key="grains.english">
      <q-img class="card-img" :src="grains.image" />
      <table class="q-table">
        <tbody>
          <tr>
            <td>{{ grains.english }}</td>
            <td>{{ grains.polish }}</td>
          </tr>
        </tbody>
      </table>
    </q-card>
  </div>
</template>
<script>
import grainsJson from "./grains.json";

const vueObject = {
  data() {
    const templateObject = {
      ziarna: grainsJson,
    };

    return templateObject;
  },
};

export default vueObject;
</script>
