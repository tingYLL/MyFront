<template>
  <School :getSchoolName="getSchoolName"/>
</template>

<script>
import School from './components/School'

export default {
  name: 'App',
  components: {
    School
  },
  methods:{
    getSchoolName(name){
      console.log("App组件收到了学校名，学校名称是："+name)
    }
  }
}
</script>

<style>

</style>
