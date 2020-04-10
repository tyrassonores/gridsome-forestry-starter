<template>
  <div class="layout" :class="{ 'sticky-header': $route.path === '/' }">
    <Header />
    <slot/>
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header"
import Footer from "@/components/Footer"

export default {
  components: {
    Header,
    Footer
  }
}
</script>


<style>
* {
  box-sizing: border-box;
}

@import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Cabin:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500;1,600;1,700&display=swap');

body {
  --color-base: rgb(255, 255, 255);
  --color-base-1: rgb(255, 255, 255);
  --color-contrast: rgb(0, 0, 0);
  --color-contrast-1: rgb(0, 0, 0);
  /*font-family: 'VT323', monospace;*/
  font-family: 'Cabin', sans-serif;
  margin:0;
  padding: 0;
  font-size: 16px;
  background: var(--color-base);
  color: var(--color-contrast);
  transition: background 0.5s ease;
  background-image: url(~../../static/background.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  image-rendering: optimizeSpeed;             /* STOP SMOOTHING, GIVE ME SPEED  */
  image-rendering: -moz-crisp-edges;          /* Firefox                        */
  image-rendering: -o-crisp-edges;            /* Opera                          */
  image-rendering: -webkit-optimize-contrast; /* Chrome (and eventually Safari) */
  image-rendering: pixelated; /* Chrome */
  image-rendering: optimize-contrast;         /* CSS3 Proposed                  */
  -ms-interpolation-mode: nearest-neighbor;   /* IE8+                           */

}

body.dark {
  --color-base: rgb(0, 0, 0);
  --color-base-1: rgb(83, 83, 83);
  --color-contrast: rgb(255, 255, 255);
  --color-contrast-1: rgb(203, 203, 203);
}

h1 {
font-family: 'VT323', monospace;
font-weight:normal;

}

.layout {
  padding: 0;
}

.layout.sticky-header {
  padding: 6rem 0 0 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

@media (min-width: 860px) {
  .container {
    padding: 0 6rem;
  }
}

a {
  color: inherit;
}

img {
  max-width: 100%;
}

.label {
  display: block;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

</style>
