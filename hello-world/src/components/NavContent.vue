<template>

  <div>
    <nav>
      <ul>
        <li v-for="item in navItemTexts" :key="item">
          <NavlistItem :itemText="item"></NavlistItem>
          <hr>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
import NavlistItem from './NavListItem.vue'
import { eventBus } from "../main.js"

export default {
  components: {
    NavlistItem
  },
  data: function(){
    return {
      navItemTexts: ['Home','Touch','Send','AccountBalance']
    }
  },
  methods: {
    
  },
  created(){
    eventBus.$emit("updateActiveState","Haider")
    window.console.log(eventBus)
  }

}
</script>


<style scoped>
div{
  height: 80%;
  width: 20%;
  background-color: lightcyan;
  overflow: auto;
  float: left;
}
nav{
  margin-top: 20px
}
ul{
  list-style: none;
}
</style>