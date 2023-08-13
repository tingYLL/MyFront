<template>
  <div>
    <h2>姓名:{{name}}</h2>
    <h2>年龄:{{address}}</h2>
    <button @click="getStudentNametoApp">点我把学生名传给App</button>
  </div>
</template>

<script>
export default{
  data(){
    return {
      name:'小帅',
      address:22
    }
  },

  methods:{
    getStudentNametoApp(){
      //触发Student组件实例身上的atguigu事件
      this.$emit('atguigu',this.name)
    }
  }
}
</script>