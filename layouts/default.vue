<template lang="pug">
  div
    Navbar
    .container.relative.mx-auto#main
      Nuxt
</template>

<script>
import Navbar from '@/components/Navbar'
export default {
  components: { Navbar },
}
</script>

<style>
html {
  font-family: 'Kanit', 'Open Sans', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

body {
  font-size: 1rem;
  background: #f9f9f9;
}

#main {
  margin-top: 64px;
}
</style>
