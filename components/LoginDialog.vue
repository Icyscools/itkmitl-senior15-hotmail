<template>
  <vs-dialog auto-width v-model="show" v-on:close="onClose">
    <template #header>
      <!-- it kmitl logo -->
      <h4 class="not-margin">เข้าสู่ระบบ (เฉพาะรหัส 60)</h4>
    </template>

    <div class="con-form">
      <vs-input v-model="email" placeholder="Email">
        <template #icon> @ </template>
      </vs-input>
      <vs-input type="password" v-model="password" placeholder="Password">
        <template #icon>
          <i class="bx bxs-lock"></i>
        </template>
      </vs-input>
      <div class="flex">
        <vs-checkbox v-model="remember">Remember me</vs-checkbox>
        <a href="#">Forgot Password?</a>
      </div>
    </div>

    <template #footer>
      <div class="footer-dialog">
        <vs-button block> Sign In </vs-button>
      </div>
    </template>
  </vs-dialog>
</template>

<script>
export default {
  props: ['show', 'onClose'],
  data: () => ({
    email: '',
    password: '',
    remember: false,
  }),
}
</script>

<style lang="css" scope>
/* getColor(vsColor, alpha = 1)
    unquote("rgba(var(--vs-"+vsColor+"), "+alpha+")")
getVar(var)
    unquote("var(--vs-"+var+")")
.not-margin {
  margin: 0px;
  font-weight: normal;
  padding: 10px;
}

.con-form {
  width: 100%;
  .flex {
    display: flex;
    align-items: center;
    justify-content: space-between;
    a {
      font-size: 0.8rem;
      opacity: 0.7;
      &:hover {
        opacity: 1;
      }
    }
  }
  .vs-checkbox-label {
    font-size: 0.8rem;
  }
  .vs-input-content {
    margin: 10px 0px;
    width: calc(100%);
    .vs-input {
      width: 100%;
    }
  }
}

.footer-dialog {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: calc(100%);
  .new {
    margin: 0px;
    margin-top: 20px;
    padding: 0px;
    font-size: 0.7rem;
    a {
      // color getColor('primary') !important
      margin-left: 6px;
      &:hover {
        text-decoration: underlineว;
      }
    }
  }
  .vs-button {
    margin: 0px;
  }
} */
</style>
