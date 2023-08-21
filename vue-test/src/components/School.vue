<template>
  <div>
    <h2>学校:{{name}}</h2>
    <h2>地址:{{address}}</h2>
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
    mounted(){
      this.x.$on('hello',(data)=>{
        console.log('我是school组件，收到了数据',data)
      })
    }
  }
</script>