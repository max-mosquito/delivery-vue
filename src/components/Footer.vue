<template>
  <footer class="footer">
      <div class="footer-wrap wrap">
        <div class="logo">
          <router-link class="logo-link" to="/">
            <img class="../assets/img/-logo" src="../assets/img//logo.svg" alt="logo">
          </router-link>
        </div>
        <nav class="footer-nav">
          <ul class="footer-nav-list">
            <li class="footer-nav-list-item"><a target="_blank" href="./goods.html" class="footer-nav-list-item-link">Ресторанам </a></li>
            <li class="footer-nav-list-item"><a target="_blank" href="./goods.html" class="footer-nav-list-item-link">Курьерам</a></li>
            <li class="footer-nav-list-item"><a target="_blank" href="./goods.html" class="footer-nav-list-item-link">Пресс-центр</a></li>
            <li class="footer-nav-list-item"><a target="_blank" href="./goods.html" class="footer-nav-list-item-link">Контакты</a></li>
          </ul>
        </nav>
        <div class="footer-soc">
          <a class="footer-soc-link" target="_blank" href="#">
            <img class="footer-soc-pic" src="../assets/img//instagram.svg" alt="instagram">
          </a>
          <a class="footer-soc-link" target="_blank" href="#">
            <img class="footer-soc-pic" src="../assets/img//facebook.svg" alt="facebook">
          </a>
          <a class="footer-soc-link" target="_blank" href="#">
            <img class="footer-soc-pic" src="../assets/img//vk.svg" alt="vk">
          </a>
        </div>
      </div>
    </footer>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>

.footer {
  min-height: 155px;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
}

.footer-wrap {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  gap: 24px;
  -ms-flex-wrap: wrap;
      flex-wrap: wrap;
}

.footer-nav {
  -webkit-box-flex: 1;
      -ms-flex: 1;
          flex: 1;
}

.footer-nav-list {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  gap: 15px;
  -ms-flex-wrap: wrap;
      flex-wrap: wrap;
}

.footer-nav-list-item-link {
  font-size: 18px;
  line-height: 21px;
  color: #595959;
}

.footer-soc {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
}

.footer-soc-link {
  margin-right: 21px;
}
.footer-soc-link:last-child {
  margin-right: 0;
}
</style>