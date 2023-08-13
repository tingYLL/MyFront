<template>
  <div>

    <MyCategory title="电影" >
      <template scope="jdjm">
<!--        {{jdjm}}-->
        <ul>
          <li v-for="(item,index) in jdjm.films" :key="index">{{item}}</li>
        </ul>
        <h3>{{jdjm.message}}</h3>
      </template>
    </MyCategory>
    <MyCategory title="游戏" >
      <template slot-scope="jdjm">
        <!--        {{jdjm}}-->
        <ol>
          <li v-for="(item,index) in jdjm.games" :key="index">{{item}}</li>
        </ol>
        <h3>{{jdjm.message}}</h3>
      </template>
    </MyCategory>
  </div>
</template>

<script>

import MyCategory from "@/components/MyCategory";


export default {
  name: 'App',
  data(){

  },
  components: {
    MyCategory
  }
}
</script>

<style>

</style>
