<template>
  <div>
    <h2>姓名:{{name}}</h2>
    <h2>年龄:{{address}}</h2>
    <button @click="sendStudentName">把学生名给School组件</button>
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
    sendStudentName(){
      this.x.$emit('hello',666)
    }

  },
  mounted(){

  }
}
</script>