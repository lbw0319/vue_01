<template>
  <div>
    <ul>
      <li v-for="(value,index) in myarr" :key = index>
        {{ value }}
        <input type="button" value="删除" @click="del(index)">
        </li>
    </ul>
    <input type="button" value="生成" @click="add">
  </div>
</template>

<script>
export default {
  data(){
    return{
      myarr:[1,2,3]
    }
  },
  methods:{
    add(){
      let num = Math.round(Math.random()*1000);
      this.myarr.push(num);
    },
    del(index){
      this.myarr.splice(index,1);
    }
  }
}
</script>

<style>

</style>