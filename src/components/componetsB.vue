<template>
  <h2 class="background double"><span><slot/></span></h2>
</template>
  
<script setup>

</script>
  
<style scoped lang="scss">

h2 {
  font: 33px sans-serif;
  margin-top: 30px;
  text-align: center;
  text-transform: uppercase;
}

h2.background {
  position: relative;
  z-index: 1;

  &:before {
    border-top: 2px solid #dfdfdf;
    content: "";
    margin: 0 auto;
    /* this centers the line to the full width specified */
    position: absolute;
    /* positioning must be absolute here, and relative positioning must be applied to the parent */
    top: 50%;
    left: 0;
    right: 0;
    bottom: 0;
    width: 95%;
    z-index: -1;
  }

  span {
    /* to hide the lines from behind the text, you have to set the background color the same as the container */
    background: #fff;
    padding: 0 15px;
  }
}

h2.double:before {
  /* this is just to undo the :before styling from above */
  border-top: none;
}

h2.double:after {
  border-bottom: 1px solid blue;
  -webkit-box-shadow: 0 1px 0 0 red;
  -moz-box-shadow: 0 1px 0 0 red;
  box-shadow: 0 1px 0 0 red;
  content: "";
  margin: 0 auto;
  /* this centers the line to the full width specified */
  position: absolute;
  top: 45%;
  left: 0;
  right: 0;
  width: 95%;
  z-index: -1;
}


</style>
  