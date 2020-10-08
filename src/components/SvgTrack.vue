<template>
  <div class="outerWrapper">

    <svg
      version="1.1"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      x="0px"
      y="0px"
      width="100%"
      height="100%"
      xml:space="preserve"
    >
      <!--
       <circle class="street" r="200"/>
       <circle class="stripes" r="200"/>
      -->
      
      <path
        class="street"
        d="M200,0 A200,200 0 1,1 200,400 A200,200 0 1,1 200,0"
      />

      <path
        class="stripes"
        d="M200,0 A200,200 0 1,1 200,400 A200,200 0 1,1 200,0"
      />
      

      <g
        class="bike"
        transform="translate(-50 13) rotate(-90)"
      >

        <title>bike</title>
        <rect
          x="10"
          y="49"
          width="5"
          height="31"
        />
        <rect
          x="10"
          width="5"
          height="31"
        />
        <rect
          class="cls-1"
          x="11"
          y="14"
          width="3"
          height="52"
        />
        <rect
          class="cls-2"
          x="5"
          y="25"
          width="15"
          height="15"
        />
        <rect
          x="7"
          y="28"
          width="11"
          height="11"
        />
        <rect
          class="cls-3"
          x="5"
          y="40"
          width="6"
          height="6"
        />
        <rect
          class="cls-3"
          x="14"
          y="40"
          width="6"
          height="10"
        />
        <rect
          class="cls-4"
          x="7"
          y="39"
          width="11"
          height="2"
        />
        <rect
          class="cls-2"
          x="20"
          y="25"
          width="5"
          height="9"
        />
        <rect
          class="cls-2"
          y="25"
          width="5"
          height="9"
        />
        <polygon
          class="cls-1"
          points="18 54 18 53 19 53 19 52 20 52 20 51 21 51 21 50 24 50 24 53 23 53 23 54 22 54 22 55 21 55 21 56 20 56 20 57 13 57 13 54 18 54"
        />
        <rect
          class="cls-4"
          x="20"
          y="34"
          width="5"
          height="18"
        />
        <polygon
          class="cls-1"
          points="7 54 7 53 6 53 6 52 5 52 5 51 4 51 4 50 1 50 1 53 2 53 2 54 3 54 3 55 4 55 4 56 5 56 5 57 12 57 12 54 7 54"
        />
        <rect
          class="cls-4"
          y="34"
          width="5"
          height="18"
        />
      </g>

    </svg>

  </div>
</template>

<script>
export default {
  mounted() {},
};
</script>

<style>
.outerWrapper svg {
  position: absolute;
  left: 0;
}

.outerWrapper svg .stripes {
  fill: none;
  stroke: white;
  stroke-width: 5;
  stroke-dasharray: 20, 20;
}

.outerWrapper svg .street {
  fill: none;
  stroke: grey;
  stroke-width: 100;
}

.outerWrapper svg polygon {
  fill: orange;
}

@keyframes move {
  0% {
    offset-distance: 0%;
    motion-offset: 0%;
  }
  100% {
    offset-distance: 100%;
    motion-offset: 100%;
  }
}

.bike {
  offset-path: path(
    "M200,0 A200,200 0 1,1 200,400 A200,200 0 1,1 200,0"
  );
  animation: move 22s linear infinite;
}

.bike > .cls-1 {
  fill: #ea2f09;
}

.bike > .cls-2 {
  fill: #03b0d2;
}

.bike > .cls-3 {
  fill: #392c39;
}

.bike > .cls-4 {
  fill: #f9b38c;
}

.curveTest {
  fill: none;
  stroke: black;
  stroke-width: 5;
}

.outerWrapper {
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  right: 0vw;
  /*position: relative;*/
  /*right: 0;*/
  transform: none;
  transform-origin: 0 0;
}

@media only screen and (max-width: 639px) {
  .outerWrapper {
    right: -90vw;
    /*transform: scale(0.6) translate(295px, -575px);*/
    transform: scale(0.5) translate(200px, -10px);
    width: 200%;
    height: 200%;
  }
}

@media only screen and (min-width: 640px) {
  .outerWrapper {
    right: -40vw;
  }
}

@media only screen and (min-width: 990px) {
  .outerWrapper {
    right: -40vw;
  }
}

@media only screen and (min-width: 1440px) {
  .outerWrapper {
    right: 0vw;
  }
}

@media only screen and (min-width: 1920px) {
  .outerWrapper {
    right: 20vw;
  }
}
</style>