<template>
  <div :class="chooseBg()">
    
  </div>
</template>

<script>
export default {
  methods: {
    chooseBg(){
      if (document.URL.includes("/Send"))
      {
          return 'orangeBg'
      }
      else if(document.URL.includes("/Touch")){
        return 'greenBg'
      }
      else if (document.URL.includes("/Home")){
        return 'redBg'
      }
      else if (document.URL.includes("/AccountBalance")){
        return 'yellowBg'
      }
      else{
        return 'redBg'
      }
    }
  }
}
</script>


<style scoped>
div{
  height: 80%;
  width: 80%;
  overflow: auto;
  float: right;
}
.redBg{
  background-color: red;
}
.greenBg{
  background-color: green;
}
.yellowBg{
  background-color: yellow;
}
.orangeBg{
  background-color: orange;
}
</style>