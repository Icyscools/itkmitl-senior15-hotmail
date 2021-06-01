<template lang="pug">
  vue-typed-js.mx-auto.text-xl(
      :strings="['ไอที 15']"
      :typeSpeed="100"
      :startDelay="300"
      :cursorChar="'_'"
    )
      h1 
        |ร่วมแสดงความยินดีหรือฝากอะไรไปบอกกับรุ่นพี่ 
        span.text-orange.italic.typing 
        span.ml-1 กันเถอะ!
</template>

<script>
import { VueTypedJs } from 'vue-typed-js'
export default {
  components: { VueTypedJs },
}
</script>
