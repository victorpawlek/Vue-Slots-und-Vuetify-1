<template>
  <div id="app">
    <DataTable :items="desserts" :headers="headers">
      <template v-slot:header>
        <h2>Watch What You Eat!</h2>
      </template>
      <template v-slot:footer> Created 2021 by Victor Pawlek </template>
      <template v-slot:body.append>
        <tr>
          <td>Total</td>
          <td>{{ totalCalories }}</td>
          <td>{{ totalFat }}</td>
          <td>{{ totalCarbs }}</td>
          <td>{{ totalProtein }}</td>
          <td></td>
        </tr>
      </template>
    </DataTable>
  </div>
</template>

<script>
import DataTable from '@/components/DataTable.vue';
export default {
  components: {
    DataTable,
  },
  computed: {
    totalCalories() {
      let n = 0;
      this.desserts.forEach((el) => (n += el.calories));
      console.log(n);
      return n;
    },
    totalFat() {
      let n = 0;
      this.desserts.forEach((el) => (n += el.fat));
      return n;
    },
    totalCarbs() {
      let n = 0;
      this.desserts.forEach((el) => (n += el.carbs));
      return n;
    },
    totalProtein() {
      let n = 0;
      this.desserts.forEach((el) => (n += el.protein));
      return n;
    },
  },
  data() {
    return {
      headers: [
        {
          text: 'Dessert (100g serving)',
          value: 'name',
        },
        { text: 'Calories', value: 'calories' },
        { text: 'Fat (g)', value: 'fat' },
        { text: 'Carbs (g)', value: 'carbs' },
        { text: 'Protein (g)', value: 'protein' },
        { text: 'Iron (%)', value: 'iron' },
      ],
      desserts: [
        {
          name: 'Frozen Yogurt',
          calories: 159,
          fat: 6.0,
          carbs: 24,
          protein: 4.0,
          iron: '1%',
        },
        {
          name: 'Ice cream sandwich',
          calories: 237,
          fat: 9.0,
          carbs: 37,
          protein: 4.3,
          iron: '1%',
        },
        {
          name: 'Eclair',
          calories: 262,
          fat: 16.0,
          carbs: 23,
          protein: 6.0,
          iron: '7%',
        },
        {
          name: 'Cupcake',
          calories: 305,
          fat: 3.7,
          carbs: 67,
          protein: 4.3,
          iron: '8%',
        },
        {
          name: 'Gingerbread',
          calories: 356,
          fat: 16.0,
          carbs: 49,
          protein: 3.9,
          iron: '16%',
        },
        {
          name: 'Jelly bean',
          calories: 375,
          fat: 0.0,
          carbs: 94,
          protein: 0.0,
          iron: '0%',
        },
        {
          name: 'Lollipop',
          calories: 392,
          fat: 0.2,
          carbs: 98,
          protein: 0,
          iron: '2%',
        },
        {
          name: 'Honeycomb',
          calories: 408,
          fat: 3.2,
          carbs: 87,
          protein: 6.5,
          iron: '45%',
        },
        {
          name: 'Donut',
          calories: 452,
          fat: 25.0,
          carbs: 51,
          protein: 4.9,
          iron: '22%',
        },
        {
          name: 'KitKat',
          calories: 518,
          fat: 26.0,
          carbs: 65,
          protein: 7,
          iron: '6%',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
