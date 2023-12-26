<template>
  <div>
    <h2>Parent Component</h2>
    <p>Search List: {{ searchList }}</p>
    <ChildrenComponent :searchFieldList.sync="searchList" />
  </div>
</template>

<script>
import ChildrenComponent from "@/components/testSync/ChildrenComponent";
export default {
  data() {
    return {
      searchList: ['apple', 'banana', 'orange']
    };
  },
  components: {
    ChildrenComponent
  }
};
</script>