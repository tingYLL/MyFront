<template>
  <div class="category">
    <h3>{{title}}分类</h3>
    <slot name="first">我是默认值，当父组件没有传递数值的时候我会出现</slot>
    <slot name="second"></slot>
  </div>

</template>

<script>
export default{
  props:[
    'title'
  ]
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