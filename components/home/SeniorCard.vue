<template lang="pug">
  vs-card
    template(#title)
      //- this should be senior fullname and nickname
      h3 
      | {{fullname}} 
      //- | ({{nickname}})
    template(#img)
      img(src="https://www.fillmurray.com/640/360" alt="")
    template(#text)
      //- this should be senior description
      //- {{description}}
      p Lorem ipsum dolor sit amet consectetur, adipisicing elit. 
      vs-button.w-full(
        gradient
      ) เขียนอะไรถึงพี่คนนี้ 
</template>

<script>
export default {
  props: ['fullname'],
}
</script>
