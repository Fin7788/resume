<template>
  <componetsA />
  <div class="mainWrap">
    <div class="sublist">
      <div>
        <componetsB>Skill</componetsB>
        <componetsC />
        <componetsD />
      </div>


    </div>
    <div class="sublist">
      <div>
        <componetsB>about me</componetsB>
        <p>嗨你好，我是 Gary，來自桃園市，畢業於中山大學，目標是成為一名厲害的軟體工程師。</p>
      </div>
    </div>

  </div>
</template>

<script setup>
import componetsA from "./components/componetsA.vue"
import componetsB from "./components/componetsB.vue"
import componetsC from "./components/componetsC.vue"
import componetsD from "./components/componetsD.vue"

</script>

<style lang="scss" scoped>
.mainWrap {
  display: flex;

  .sublist {
    width: 50%;

    div {
      p {
        margin-left: 5%;
      }
    }
  }
}
</style>
