<template>
  <header class="header">
      <div class="header-wrap wrap">
        <div class="logo">
          <router-link class="logo-link" to="/">
            <img class="../assets/img/-logo" src="../assets/img//logo.svg" alt="logo">
          </router-link>
        </div>
        <div class="header-btns">
          <button class="header-btn-logon">
            <img class="header-btn-logon-pic" src="../assets/img//logon.svg" alt="logon">
          </button>
          <button class="header-btn-cart" @click="opemModal()">
            <img class="header-btn-cart-pic" src="../assets/img//cart.svg" alt="cart">
          </button>
        </div>
      </div>
    </header>
</template>

<script setup>
  const emit = defineEmits(['toffleModal'])
  const opemModal = () => emit('toffleModal')
</script>

<style scoped>

.header {
  margin-bottom: 40px;
}

  .header-wrap {
  padding-top: 44px;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
}

.logo {
  width: 100px;
  height: 36px;
}

.img-logo {
  width: 100%;
  height: 100%;
}

.header-btns {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}

.header-btn-logon {
  margin-right: 8px;
  width: 98px;
  height: 40px;
  cursor: pointer;
}

.header-btn-logon-pic {
  width: 100%;
  height: 100%;
}

.header-btn-cart {
  width: 116px;
  height: 40px;
  cursor: pointer;
}

.header-btn-cart-pic {
  width: 100%;
  height: 100%;
}
</style>