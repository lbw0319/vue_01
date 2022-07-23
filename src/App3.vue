<template>
  <div>
    <table border = 1>
      <tr>
        <th>编号</th>
        <th>品牌名称</th>
        <th>创建时间</th>
        <th>操作</th>
      </tr>
      <tr v-for="(obj,index) in products" :key=index>
        <th>{{ obj.id }}</th>
        <th>{{ obj.proname }}</th>
        <th>{{ obj.createtime }}</th>
        <th><input type="button" value="删除" @click="del(index)"></th>
      </tr>
      <tr v-if="products.length === 0">
        <td colspan="4">没有数据了</td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data(){
    return{
      products:[
        {
          id:1,
          proname:'奔驰',
          createtime:'2022-07-01'
        },
         {
          id:2,
          proname:'宝马',
          createtime:'2022-08-01'
        },
         {
          id:3,
          proname:'奥迪',
          createtime:'2022-09-01'
        },
      ],
    }
  },
  methods:{
    del(index){
      this.products.splice(index,1);
    },

  }

}
</script>

<style>
table{
  width:400px;
  margin:10px auto;
  text-align: center;
  border-collapse: collapse;
}

</style>