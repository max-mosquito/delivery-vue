

<template>
  <div class="main-wwrap wrap">
        <section class="banner">
          <div class="banner-item">
            <h2 class="banner-item-title">Онлайн-сервис доставки еды на дом</h2>
            <p class="banner-item-text">Блюда из любимого ресторана привезет курьер в перчатках, маске и с антисептиком</p>
          </div>
        </section>
        <section class="products">
          <div class="products-header">
            <h3 class="products-header--title">
              Рестораны
            </h3>
            <input type="text" class="products-header--search" placeholder="Поиск блюд и ресторанов">
          </div>
          <div class="product-wrapper" id="rests-container">
            <router-link 
              class="products-card" 
              v-for="rest in restArr" 
              :key="rest.id"
              :to="`rest?id=${rest.id}`" 
            >
              <div class="products-card__pic">
                <img :src="`./assets/img//rests/${rest.image}`" alt="">
                <!-- <img :src="getUrl(rest.image)" alt=""> -->
              </div>
              <div class="products-card__descr">
                <div class="products-card__descr-row">
                  <h4 class="products-card__descr--title">{{rest.title}}</h4>
                  <div class="products-card__descr-badge">
                    {{rest.time}} мин
                  </div>
                </div>
                <div class="products-card__descr-row2">
                  <div class="products-card__descr-row2--rating">
                    <img src="../assets/img//star.svg" alt="star">
                    {{rest.rating}}
                  </div>
                  <div class="products-card__descr-row2--price">От {{rest.price}} ₽</div>
                  <div class="products-card__descr-row2--group">
                    <img src="../assets/img//marker.svg" alt="marker">
                    {{rest.type}} </div>
                </div>
              </div>
            </router-link>
          </div>
        </section>
      </div>
</template>

<script setup>
  const restArr = [
    {
      id: 0,
      title: 'Пицца плюс',
      time: 50,
      rating: 4.5,
      price: 900,
      type: "Пицца ",
      image: 'r1.jpg',
    },
    {
      id: 1,
      title: 'Тануки ',
      time: 50,
      rating: 5,
      price: 900,
      type: "Пицца ",
      image: 'r2.jpg',
    },
    {
      id: 2,
      title: 'FoodBand',
      time: 50,
      rating: 5,
      price: 900,
      type: "Пицца ",
      image: 'r3.jpg',
    },
    {
      id: 3,
      title: 'Жадина-пицца',
      time: 50,
      rating: 5,
      price: 900,
      type: "Пицца ",
      image: 'r4.jpg',
    },
    {
      id: 4,
      title: 'Точка еды',
      time: 50,
      rating: 5,
      price: 900,
      type: "Пицца ",
      image: 'r5.jpg',
    },
    {
      id: 5,
      title: 'PizzaBurger',
      time: 50,
      rating: 5,
      price: 900,
      type: "Пицца ",
      image: 'r6.jpg',
    },
  ]

  const getUrl = (name) => {
    // return `../assets/img//rests/r1.jpg`
  // return new URL(`../assets/img//rests/r1.jpg`, import.meta.url)
  // return new URL(`../assets/img//rests/${name}`, import.meta.url)
  console.log(name);
  // console.log(new URL(`../assets/img//rests/${name}`, import.meta.url));
  }
</script>