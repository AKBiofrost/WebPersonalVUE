<template>


<body>
<div>
  <p>
    <span></span>
  </p>
</div>
</body>

</template>

<script>


</script>

<style lang="scss" scoped>

@property --rx1 {
  syntax: '<angle>';
  inherits: false;
  initial-value: 0deg;
}
@property --rx2 {
  syntax: '<angle>';
  inherits: false;
  initial-value: 0deg;
}
@property --ry1 {
  syntax: '<angle>';
  inherits: false;
  initial-value: 0deg;
}
@property --ry2 {
  syntax: '<angle>';
  inherits: false;
  initial-value: 0deg;
}
@property --rz1 {
  syntax: '<angle>';
  inherits: false;
  initial-value: 0deg;
}
@property --rz2 {
  syntax: '<angle>';
  inherits: false;
  initial-value: 0deg;
}


div, p, span {
  animation: custom-prop-o-rama 8300ms alternate infinite ease-in-out;
}
@keyframes custom-prop-o-rama {
  33% {
    --rx1: 20deg;
    --ry1: -303deg;
    --rz1: 45deg;
  }
  50% {
    --rx1: -20deg;
    --ry2: -30deg;
  }
  67% {
    --rx2: -200deg;
    --ry2: 130deg;
    --rz2: -350deg;
  }
}

div {
  --size: 40vmin;
  
  transform: 
    rotateX(var(--rx1))
    rotateY(var(--ry2))
    rotateZ(var(--rz1))
    rotateZ(var(--rz2))
    rotateX(var(--rx2))
    rotateY(var(--ry1));
}


p {
  --size: 36vmin;
  --border-size: 2.5vmin;
  --color: 188;
  
  transform:
    rotateX(var(--rx1))
    rotateY(calc(var(--ry1) * 2))
    rotateZ(var(--rz1))
    rotateY(var(--ry2));
}


span {
  --size: 24.5vmin;
  --border-size: 2vmin;
  --color: 36;
  
  transform:
    rotateX(var(--rx2))
    rotateY(var(--ry2))
    rotateZ(var(--rz2))
    rotateZ(var(--rz1))
    rotateX(var(--rx1))
    rotateY(var(--ry1));
}



body {
  min-height: 25vh;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  background: radial-gradient(circle, hsl(180, 7%, 95%),hsl(200, 16%, 51%));
  perspective: 80vmax;
  
  font-family: system-ui, 'Segoe UI', sans-serif;
  line-height: 1.4;
  text-align: center;
}
*, *::before, *::after {
  box-sizing: border-box;
}

footer {
  color: #fafdff;
  position: absolute;
  bottom: 1rem;
  left: 1rem;
  right: 1rem;
}
.supported footer {
  display: none;
}


div, p, span {
  border-radius: 5%;
  width: var(--size);
  height: var(--size);
  border: var(--border-size, 3vmin) solid hsl(var(--color, 343), 94%, 54%);
  position: relative;
  
  display: flex;
  justify-content: center;
  align-items: center;
  
  transform-style: preserve-3d;
  will-change: transform;
  /* should will-change be on the custom properties now? */
}
</style>