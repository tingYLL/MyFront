<template>
  <div>
    <h2>Child Component</h2>
    <input v-model="searchFieldList" type="text" @input="updateSearchField" />
  </div>
</template>

<script>
export default {
  props: {
    searchFieldList: {
      type: Array,
      required: true
    }
  },
  methods:{
    updateSearchField() {
      this.$emit('update:searchFieldList', this.searchFieldList);
    }
  }
};
</script>