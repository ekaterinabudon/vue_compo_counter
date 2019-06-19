<template>
  <div>
    <h1>Возведение в степень</h1>
    <button @click="increment">⬆︎</button>
    <input type="text" v-model="total" @change="updateArray">
    <ul>
      <li v-for="item in arrayOfExps" :key="item.exp">{{base}}<sup>{{item.exp}}</sup> = {{item.result}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      total: 5,
      base: 2,
      arrayOfExps: [],
    }
  },
  methods: {
   increment: function() {
     this.total = this.total + 1;
     this.updateArray();
   },
   updateArray: function() {
     const array = [];
     for (let i = 0; i < this.total; i++) {
       const exp = 10 + i;
       array.push({
         exp,
         result: Math.pow(this.base, exp)
       })

     }
     this.arrayOfExps = array;

   }
 },
 created: function () {
   this.updateArray();
 }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  color: red;
}
</style>
