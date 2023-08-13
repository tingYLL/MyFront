<template>
  <div>

    <MyCategory title="电影" >
      <template scope="jdjm" slot="slot1">
<!--        {{jdjm}}-->
        <ul>
          <li v-for="(item,index) in jdjm.films" :key="index">{{item}}</li>
        </ul>
        <h3>{{jdjm.message}}</h3>
      </template>
      <h3 slot="slot2">hello</h3>
    </MyCategory>
    <MyCategory title="游戏" >
      <template slot-scope="jdjm" slot="slot2">
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
