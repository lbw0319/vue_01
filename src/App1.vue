<template>
  <div>
    <ul>
      <li v-for="(value,index) in arr" :key=index>{{ value }}</li>
    </ul>
    <input type="button" value="走一走" @click="turn">
  </div>
</template>

<script>
export default {
  data(){
    return{
      arr:['帅哥','美女','程序员','野兽','修改']
    }
  },
  methods:{
    turn(){
      this.arr.push(this.arr[0]);
      this.arr.shift();
    },
  }

}
</script>

<style>

</style>