<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css';


const items = [
  {
    id: 1,
    image: '/image/img_1.jpg',
    title: 'Работа 1',
    description: 'Описание первой работы',
  },
  {
    id: 2,
    image: '/image/img_2.jpg',
    title: 'Работа 2',
    description: 'Описание второй работы',
  },
  {
    id: 3,
    image: '/image/img_3.jpg',
    title: 'Работа 3',
    description: 'Описание третьей работы',
  },
]
</script>
<template>
  <!-- header -->
   <header>
    <div class="container header">
      <!-- logo -->
       <div class="logo">
        <a href="">
          dcs
        </a>
       </div>
       <nav class="">
        <ul class="nav-links">
          <li class="nav-link">
            <a href="" >главная</a>
          </li>
          <li class="nav-link">
            <a href="" >Наши работы</a>
          </li>
          <li class="nav-link">
            <a href="">контакт</a>
          </li>
        </ul>
      </nav>
      </div>
   </header>
   <main>
    <!-- hero -->
    <section class="container section">
      <div class="hero">
        <!-- text -->
        <div class="hero-title">
          <h1 class="">
            Don<br>
            city<br>
            stroy
          </h1>
        </div>
        <!-- image -->
        <div class="hero-image">
          <img src="/image/heroimage.png" alt="heroImg">
        </div>
      </div>
      <!-- card -->
      <div class="card">
        <!-- image -->
        <div class="card-img">
          <img src="/image/photo.png" alt="itesmImg">
        </div>
        <div class="card-text_btn">
          <!-- text -->
           <div class="card-text">
            <h3 class="">Эммануил Таможников</h3>
            <p class="">краткое описание</p>
           </div>
           <!-- buttons -->
            <div class="card_buttons">
              <a href="tel:+79496188568" class="item-button phone">
                <i class="fa-solid fa-phone"></i>
              </a>
              <a href="sms:+79496188568" class="item-button envelope">
                <i class="fa-solid fa-envelope"></i>
              </a>
            </div>
        </div>
      </div>
    </section>
    <!-- about us -->
    <section class="container">
      <div class="work">
        <!-- text -->
         <div class="work-title">
          <h3>фото<br>наших<br>работ</h3>
          <div class="slider-container">
            <Swiper
              :slides-per-view="1"
              :space-between="5"
              :breakpoints="{
                640: { slidesPerView: 2 },
                768: { slidesPerView: 2 },
                1024: { slidesPerView: 3 }
              }"
              class="mySwiper"
            >
              <SwiperSlide v-for="item in items" :key="item.id">
                <div class="work-item">
                  <img :src="item.image" :alt="item.title" />
                </div>
              </SwiperSlide>
            </Swiper>
          </div>
        </div>
        <!-- about us -->
        <div class="about">
          <div class="about-title">
            <h3>о нас</h3>
            <p>Уже более 5 лет наша компания оказывает услуги в сфере строительства и ремонта «ПОД КЛЮЧ» по всей территории ДНР и ЛНР. Мы считаем себя лучшими в этой сфере!</p>
            <p>Беремся за проекты любой сложности и работаем БЕЗ ВЫХОДНЫХ!</p>
            <p>Осуществляем выезд на замер, составление сметы - БЕСПЛАТНО!</p>
          </div>
        </div>
      </div>
    </section>
  </main>
  <!-- footer -->
   <footer class="footer">
    <div class="container">
      <!-- text -->
      <div class="contact">
        <h4>Контакты</h4>
        <!-- phone -->
         <div class="footerTel">
           <p>тел:</p>
           <a href="" class="">+7(949)564-19-22</a><br>
           <a href="" class="">+7(949)564-19-22</a><br>
           <a href="" class="">+7(949)564-19-22</a>
         </div>
         <div class="teleg">
           <p>telegram:</p>
           <a href="">@tamozhnikova</a>
         </div>
      </div>
      <!-- map -->
       <div class="map">
        <a href="" class=""></a>
       </div>
    </div>
   </footer>
</template>

<style scoped>

</style>