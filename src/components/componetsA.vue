<template>
    <div class="glitch" data-text="Tim Huang's">Tim Huang</div>
</template>
  
<script setup>


</script>
  
<style scoped lang="scss">
.glitch {
    color: rgb(0, 0, 0);
    font-size: 50px;
    position: relative;
    width: 400px;
    margin: 0 auto;
}

@keyframes noise-anim {
    $steps: 20;

    @for $i from 0 through $steps {
        #{percentage($i*(1/$steps))} {
            clip: rect(random(100)+px, 9999px, random(100)+px, 0);
        }
    }
}

.glitch:after {
    content: attr(data-text);
    position: absolute;
    left: 2px;
    text-shadow: -1px 0 red;
    top: 0;
    color: rgb(0, 0, 0);
    background: rgb(255, 255, 255);
    overflow: hidden;
    clip: rect(0, 900px, 0, 0);
    animation: noise-anim 3s infinite linear alternate-reverse;
}

@keyframes noise-anim-2 {
    $steps: 20;

    @for $i from 0 through $steps {
        #{percentage($i*(1/$steps))} {
            clip: rect(random(100)+px, 9999px, random(100)+px, 0);
        }
    }
}

.glitch:before {
    content: attr(data-text);
    position: absolute;
    left: -2px;
    text-shadow: 1px 0 blue;
    top: 0;
    color: rgb(0, 0, 0);
    background: rgb(255, 255, 255);
    overflow: hidden;
    clip: rect(0, 900px, 0, 0);
    animation: noise-anim-2 3s infinite linear alternate-reverse;
}
</style>
  