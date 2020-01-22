<template>

  <div>
    <p>Name:{{name}}</p>
    <p>Sending Balance:{{sendingBalance}}$</p>
  </div>
</template>

<script>
export default {
  data: function(){
    return {
      name: "Ather",
      sendingBalance: 50
    }
  },
  methods: {
    setDetails: function(){

    }
  }
}
</script>


<style scoped>
div{
  height: 20%;
  width: 20%;
  background-color: floralwhite;
  overflow: auto;
  float: left;
  text-align: center;
}
</style>