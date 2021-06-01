<template lang="pug">
  .container
    .sticky-form-header.z-50
      .search-form
        vs-input.w-full(
          shadow
          v-model="search"
          :value="search"
          placeholder="ค้นหารุ่นพี่ด้วย ชื่อ หรือ รหัสนักศึกษา เช่น พี่กาน, พี่ป้อง, 60070175"
        )
          template(#icon)
            i.bx.bx-search
    .container.flex.flex-wrap.gap-5
      div(v-for="state in filterState")
        senior-card(:fullname="state")
</template>

<script>
import SeniorCard from '~/components/home/SeniorCard'
export default {
  components: { SeniorCard },
  data: () => ({
    search: '',
    lists: [1, 2, 3, 4],
  }),
  computed: {
    filterState: function () {
      const filter = this.lists.filter((i) => i.toString().includes(this.search))
      return filter
    },
  },
}
</script>

<style>
.sticky-form-header {
  @apply sticky top-0 py-5;
  background: #fafafa;
}
.search-form {
  @apply w-3/4 flex items-center justify-center;
}
.search-form .vs-input-content {
  width: 100% !important;
}
.search-form .vs-input-content input {
  width: 100% !important;
}
</style>
