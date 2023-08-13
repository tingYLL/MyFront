<template>
  <div>
    <School :getSchoolName="getSchoolName"/>
<!--    <Student v-on:atguigu="getStudentName"/>-->
    <Student ref="student"/>
  </div>

</template>

<script>
import School from './components/School'
import Student from './components/Student'
export default {
  name: 'App',
  components: {
    School,
    Student
  },
  methods:{
    getSchoolName(name){
      console.log("App组件收到了学校名，学校名称是："+name)
    },
    getStudentName(name){
      console.log("woc！！！",name)
    }
  },
  mounted(){
    this.$refs.student.$on('atguigu',this.getStudentName)
  }
}
</script>

<style>

</style>
