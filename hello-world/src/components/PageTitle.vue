<template>

  <div>
    <p>{{Title}}</p>
  </div>
</template>

<script>

import { eventBus } from "../main.js"

export default {
  data: function(){
    return {
      Title: ""
    }
  },
  created(){
    eventBus.$on("itemClicked", (title) =>{
      this.Title= title
    })
    if (document.URL.includes("/Send"))
    {
        this.Title= "Send"
    }
    else if(document.URL.includes("/Touch")){
      this.Title= "Touch"
    }
    else if (document.URL.includes("/Home")){
      this.Title= "Home"
    }
    else if (document.URL.includes("/AccountBalance")){
      this.Title= "Account Balance"
    }
    else{
      this.Title= "Home"
    }

  }
}
</script>


<style scoped>
div{
  height: 20%;
  width: 80%;
  background-color: pink;
  overflow: auto;
  float: right;
  text-align: left;
  
}
</style>