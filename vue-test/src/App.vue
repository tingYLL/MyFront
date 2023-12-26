<template>
<!--  <div>-->
<!--    <School/>-->
<!--    <Student/>-->
<!--  </div>-->
  <div >
    <ParentComponent></ParentComponent>
  </div>

</template>

<script>
import School from './components/School'
import Student from './components/Student'
import ParentComponent from "@/components/testSync/ParentComponent";
export default {
  name: 'App',
  components: {
    ParentComponent,
    School,
    Student
  },
  methods:{

  },
  mounted(){

  }
}
</script>

<style>

</style>
