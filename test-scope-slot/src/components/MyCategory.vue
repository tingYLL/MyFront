<template>
  <div class="category">
    <h3>{{title}}分类</h3>
    <slot :films="films" :games="games" message="这是一条消息" name="slot1">我是slot1，父组件没有传值的时候我会显示</slot>
    <slot :films="films" :games="films" message="这是一条消息" name="slot2">我是slot2，父组件没有传值的时候我会显示</slot>
  </div>
</template>
<script>
export default{
  props:['title'],
  data(){
    return {
      films:["《消失的她》","《孤注一掷》","《灌篮高手》"],
      games:['GTAV','只狼']
    }
  }
}
</script>

<style>
.category{
  background-color: skyblue;
  width: 200px;
  height: 300px;
}
h3{
  text-align: center;
  background-color: orange;
}

</style>