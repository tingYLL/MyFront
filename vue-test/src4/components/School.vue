<template>
  <div>
    <h2>学校:{{name}}</h2>
    <h2>地址:{{address}}</h2>
    <button @click="getSchoolNametoApp">点我把学校名传递给父组件</button>
  </div>
</template>

<script>
  export default{
    data(){
      return {
        name:'清华大学',
        address:'北京'
      }
    },
    props:['getSchoolName'],
    methods:{
      getSchoolNametoApp(){
        this.getSchoolName(this.name)
      }
    }
  }
</script>