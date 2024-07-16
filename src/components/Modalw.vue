<template>
  <div class="cart-modal__overlay" :class="{open: isOpen}"  @click.self="closeModal">
    <div class="cart-modal">
      <div class="cart-modal__header">
        <h2 class="cart-modal__header--title">Корзина</h2>
        <span class="cart-modal__header--close"  @click="closeModal">
          <img src="../assets/img//close.svg" alt="close">
        </span>
      </div>
      <div class="cart-modal__body">
        <div class="cart-item">
          <div class="cart-item__title">
            Ролл угорь стандарт
          </div>
          <div class="cart-item__btns">
            <div class="cart-item__btns--price">
              250 ₽
            </div>
            <button class="btn-decr">-</button>
            <div class="cart-item__btns--count">
              1
            </div>
            <button class="btn--ncr">+</button>
          </div>
        </div>
        <div class="cart-item">
          <div class="cart-item__title">
            Ролл угорь стандарт
          </div>
          <div class="cart-item__btns">
            <div class="cart-item__btns--price">
              250 ₽
            </div>
            <button class="btn-decr">-</button>
            <div class="cart-item__btns--count">
              1
            </div>
            <button class="btn--ncr">+</button>
          </div>
        </div>
      </div>
      <div class="cart-modal__footer">
        <div class="cart-modal__footer--price">
          1250 ₽
        </div>
        <div class="cart-modal__footer--btns">
          <button class="cart-modal__footer--btn--order">Оформить заказ</button>
          <button class="cart-modal__footer--btn--cancel">Отмена</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  const {isOpen} = defineProps({isOpen: Boolean})
  const emit = defineEmits(['toggleModal'])
  const closeModal = () => emit('toggleModal')
</script>

<style scoped>
  .cart-modal {
  max-width: 780px;
  width: 100%;
  padding: 40px 45px;
  border-radius: 5px;
  background-color: #fff;
}

.cart-modal__header {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
  margin-bottom: 45px;
}

.cart-modal__header--title {
  font-size: 36px;
  font-weight: 700;
  line-height: 42.19px;
}

.cart-modal__header--close {
  cursor: pointer;
}

.cart-modal__body {
  margin-bottom: 53px;
}

.cart-item {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  padding-bottom: 10px;
  margin-bottom: 26px;
  border-bottom: 1px solid #D9D9D9;
  -ms-flex-wrap: wrap;
      flex-wrap: wrap;
  gap: 10px;
}

.cart-item__title {
  font-size: 18px;
  font-weight: 400;
  line-height: 32px;
}

.cart-item__btns {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
}

.cart-item__btns--price {
  font-size: 20px;
  font-weight: 700;
  line-height: 32px;
  margin-right: 48px;
}

.cart-item__btns--count {
  margin-right: 16px;
  font-size: 16px;
  line-height: 24px;
}

.btn--ncr, .btn-decr {
  font-size: 14px;
  line-height: 22px;
  color: #40A9FF;
  width: 36px;
  height: 32px;
  border: 1px solid #40A9FF;
  background-color: #fff;
  border-radius: 2px;
  cursor: pointer;
  margin-right: 16px;
}

.cart-modal__footer {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  -ms-flex-wrap: wrap;
      flex-wrap: wrap;
  gap: 10px;
}

.cart-modal__footer--price {
  font-size: 20px;
  font-weight: 700;
  line-height: 23.44px;
  color: #ffffff;
  padding: 15px 20px;
  background-color: #000000;
  border-radius: 5px;
}

.cart-modal__footer--btns {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  gap: 10px;
  -ms-flex-wrap: wrap;
      flex-wrap: wrap;
}

.cart-modal__footer--btn--order {
  background-color: #1890FF;
  color: #ffffff;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  width: 157px;
  height: 40px;
  display: block;
  border-radius: 2px;
  cursor: pointer;
}

.cart-modal__footer--btn--cancel {
  display: block;
  width: 90px;
  height: 40px;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  color: #595959;
  background-color: #fff;
  border: 1px solid #D9D9D9;
  border-radius: 2px;
  cursor: pointer;
}
</style>