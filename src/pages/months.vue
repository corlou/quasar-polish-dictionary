<template>
  <div class="q-pa-md q-gutter-sm">
    <q-breadcrumbs>
      <q-breadcrumbs-el label="Home" to="/" />
      <q-breadcrumbs-el label="Time" to="/timeHome" />
      <q-breadcrumbs-el label="Months - Miesiąc" />
    </q-breadcrumbs>
  </div>
  <div class="q-pa-md row items-start q-gutter-md">
    <q-card v-for="months in miesiąc" :key="months.month">
      <q-img class="card-img" :src="months.image" />
      <table class="q-table">
        <tbody>
          <tr class="number-table-head">
            <td>Month</td>
            <td>Season</td>
          </tr>
          <tr>
            <td>{{ months.month }}</td>
            <td>{{ months.season }}</td>
          </tr>
        </tbody>
      </table>
    </q-card>
  </div>
</template>
<script>
import monthJson from "./month.json";
export default {
  data() {
    return {
      miesiąc: monthJson,
    };
  },
};
</script>
