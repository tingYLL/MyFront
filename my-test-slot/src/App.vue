<template>
  <div class="container">
    <MyCategory title="相册">
<!--      <span v-for="film in films"></span>-->
      <img  slot="first" src="https://files.codelife.cc/wallpaper/wallspic/20230802n56l6j.jpeg?x-oss-process=image/resize,limit_0,m_fill,w_300,h_200/format,webp" alt="">
      <a slot="second" href="https://www.baidu.com">更多图片</a>
    </MyCategory>
    <MyCategory title="游戏">
<!--      这些dom是在父组件这边先完成渲染以后，再放入子组件中的-->
      <ul slot="first">
        <li v-for="(item,index) in games" :key="index">{{item}}</li>
      </ul>
<!--      <div slot="second"> ...</div> 这样的写法，其实div没有实际的意义，所以可以换成template标签 这个标签在渲染的时候不会生成 -->
      <template  slot="second">
        <div class="foot">
          <a href="#">单机游戏</a>
          <a href="#">单机游戏</a>
          <a href="#">单机游戏</a>
        </div>
      </template>


    </MyCategory>

  </div>
</template>

<script>

import MyCategory from "@/components/MyCategory";
export default {
  name: 'App',
  data(){
    return {
      films:["《消失的她》","《孤注一掷》","《灌篮高手》"],
      games:['GTAV','只狼']
    }
  },
  components: {
    MyCategory
  }
}
</script>

<style>
  .container,.foot{
  display:flex;
    justify-content: space-around;
  }
  img{
    width:100%
  }
</style>
