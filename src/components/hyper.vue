<template>
 
    <body>
 <main>
  <div></div>
  <div></div>
  <div></div>
  <div></div>
</main>



    </body>





</template>


<style lang="scss" scoped>

div {
  position: absolute;
  top: 50%;
  left: 50%;
  --size: 40vmin;
  width: calc(var(--size) * .9);
  height: var(--size);
  transform: translate(-50%,-50%) scaleX(.925);
  background: var(--c1);
  background: linear-gradient(
    var(--c1) 17.667%,
    var(--c2) 17.667% 32.333%,
    var(--c3) 32.333% 50%,
    var(--c4) 50% 67.667%,
    var(--c5) 67.667% 82.333%,
    var(--c6) 82.333%
  );
   background: conic-gradient(
    var(--c1) 17.667%,
    var(--c2) 17.667%,
    var(--c2) 32.333%,
    var(--c3) 32.333%,
    var(--c3) 50%,
    var(--c4) 50%,
    var(--c4) 67.667%,
    var(--c5) 67.667%,
    var(--c5) 82.333%,
    var(--c6) 82.333%
  ); 
  clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
  
  mix-blend-mode: multiply;
  animation: move 3000ms infinite linear;
  
  --o1: .85;
  --o2: .7;
  --o3: .55;
  --o4: .4;
  --o5: .25;
  --o6: .1;
}
div:nth-child(1) {
  --hue: 343;
  --c1: hsla(var(--hue), 90%, 54%, var(--o1));
  --c2: hsla(var(--hue), 90%, 54%, var(--o2));
  --c3: hsla(var(--hue), 90%, 54%, var(--o3));
  --c4: hsla(var(--hue), 90%, 54%, var(--o4));
  --c5: hsla(var(--hue), 90%, 54%, var(--o5));
  --c6: hsla(var(--hue), 90%, 54%, var(--o6));
  animation-delay: -1200ms;
  animation-direction: reverse;
  animation-duration: 3200ms;
}
div:nth-child(2) {
  --hue: 143;
  --c1: hsla(var(--hue), 90%, 34%, var(--o1));
  --c2: hsla(var(--hue), 90%, 44%, var(--o2));
  --c3: hsla(var(--hue), 90%, 54%, var(--o3));
  --c4: hsla(var(--hue), 90%, 64%, var(--o4));
  --c5: hsla(var(--hue), 90%, 74%, var(--o5));
  --c6: hsla(var(--hue), 90%, 84%, var(--o6));
  animation-delay: -2100ms;
  animation-duration: 3700ms;
}
div:nth-child(3) {
  --hue: 243;
  --c1: hsla(var(--hue), 90%, 34%, var(--o1));
  --c2: hsla(var(--hue), 90%, 44%, var(--o2));
  --c3: hsla(var(--hue), 90%, 54%, var(--o3));
  --c4: hsla(var(--hue), 90%, 64%, var(--o4));
  --c5: hsla(var(--hue), 90%, 74%, var(--o5));
  --c6: hsla(var(--hue), 90%, 84%, var(--o6));
  animation-delay: -2600ms;
  animation-direction: reverse;
  animation-duration: 4200ms;
}
div:nth-child(4) {
  --hue: 43;
  --c1: hsla(var(--hue), 90%, 34%, var(--o1));
  --c2: hsla(var(--hue), 90%, 44%, var(--o2));
  --c3: hsla(var(--hue), 90%, 54%, var(--o3));
  --c4: hsla(var(--hue), 90%, 64%, var(--o4));
  --c5: hsla(var(--hue), 90%, 74%, var(--o5));
  --c6: hsla(var(--hue), 90%, 84%, var(--o6));
  animation-delay: -3200ms;
  animation-duration: 2700ms;
}
@keyframes move {
  0% {
    transform: translate(-50%,-50%) rotate(0turn);
  }
  100% {
    transform: translate(-50%,-50%) rotate(1turn);
  }
}
main {
  //filter: blur(6px);
  width: 40vw;
  height: 40vh;
}
body {
  height: 50vh;
  background: #efefff;
  overflow: hidden;
}
* {
  margin: 0;
  box-sizing: border-box;
}
</style>
