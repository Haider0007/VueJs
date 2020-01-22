<template>
    <a :href="itemText" :class="addNavItemClass">
    {{itemText}}
    </a>
</template>




<script>
export default {
  props:{
    itemText: String
  },
  computed: {
    addNavItemClass: function(){
      window.console.log("computed");
      return document.URL.includes(this.itemText) ? 'active' : 'navItem'
    }
  }
}
</script>




<style>
.active{
  color: black;
}
</style>