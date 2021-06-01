<template>
  <vs-navbar color="#fff" text-white square center-collapsed v-model="active" id="navbar">
    <!-- <template #left>
      <img src="/logos/logo-vuesax-logotipo-vuesax-png-4.png" alt="" />
    </template> -->
    <vs-navbar-item :active="active == 'guide'" id="guide"> Guide </vs-navbar-item>
    <vs-navbar-item :active="active == 'docs'" id="docs"> Documents </vs-navbar-item>
    <vs-navbar-item :active="active == 'components'" id="components"> Components </vs-navbar-item>
    <vs-navbar-item :active="active == 'license'" id="license"> license </vs-navbar-item>

    <template #right>
      <vs-button color="#333" @click="toggleLoginDialog" flat>Login</vs-button>
      <vs-switch dark v-model="darkMode">
        <template #circle>
          <i v-if="!darkMode" class="bx bxs-moon"></i>
          <i v-else class="bx bxs-sun"></i>
        </template>
      </vs-switch>
    </template>
    <login-dialog :show="loginPopup" :onClose="closeLoginDialog" />
  </vs-navbar>
</template>

<script>
import LoginDialog from './LoginDialog.vue'

export default {
  components: { LoginDialog },
  data: () => ({
    active: 'guide',
    darkMode: false,
    loginPopup: false,
  }),
  methods: {
    toggleLoginDialog() {
      this.loginPopup = !this.loginPopup
    },
    closeLoginDialog() {
      this.loginPopup = false
      console.log('close dialog down')
    },
    // toggleDarkMode() {
    //   this.darkMode = !this.darkMode
    // },
  },
}
</script>

<style>
#navbar {
  padding: 10px 0;
  color: var(--vs-dark);
}
</style>
