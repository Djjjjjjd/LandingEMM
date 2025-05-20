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

document.addEventListener('scroll', () => {
  const scrolled = window.scrollY;
  document.querySelectorAll('.parallax-element').forEach((el) => {
    const speed = el.getAttribute('data-speed');
    el.style.transform = `translateY(${scrolled * speed}px)`;
  });
});

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
            <a href="#home">главная</a>
          </li>
          <li class="nav-link">
            <a href="#work">Наши работы</a>
          </li>
          <li class="nav-link">
            <a href="#footer">контакт</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
  <main>
    <!-- hero -->
    <section class="section" id="home">
      <div class="hero-backg">
        <div class="container hero parallax-element" data-speed="0.05">
          <!-- text -->
          <div class="hero-title">
            <h1 class="">
              Don<br>
              city<br>
              stroy
            </h1>
          </div>
          <!-- image -->
          <div class="hero-image ">
            <img src="/image/heroimage.png" alt="heroImg">
          </div>
        </div>
      </div>
      <!-- card -->
      <div class="card-section container">
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
      </div>
    </section>
    <!-- about us -->
    <section class="" id="work">
      <div class="work container">
        <!-- text -->
        <div class="work-title">
          <div class="work-text">
            <h3>фото<br>наших<br>работ</h3>
            <img src="/image/deelop.png" alt="detroy" class="work-deelop">
          </div>
          <div class="slider-container parallax-element" data-speed="0.03">
            <Swiper :slides-per-view="1" :space-between="5" :breakpoints="{
              640: { slidesPerView: 1 },
              768: { slidesPerView: 2 },
              1024: { slidesPerView: 3 }
            }" class="mySwiper">
              <SwiperSlide v-for="item in items" :key="item.id">
                <div class="work-item">
                  <img :src="item.image" :alt="item.title" class="slider-img" />
                </div>
              </SwiperSlide>
            </Swiper>
          </div>
        </div>
        <!-- about us -->
      </div>
      <div class="bg-about">
        <div class="block"></div>
        <div class="about">
          <div class="about-title">
            <h3>о нас</h3>
            <p>Уже более 5 лет наша компания оказывает услуги в сфере строительства и ремонта «ПОД КЛЮЧ» по всей
              территории ДНР и ЛНР. Мы считаем себя лучшими в этой сфере!</p>
            <p>Беремся за проекты любой сложности и работаем БЕЗ ВЫХОДНЫХ!</p>
            <p>Осуществляем выезд на замер, составление сметы - БЕСПЛАТНО!</p>
          </div>
        </div>
      </div>
    </section>
  </main>
  <!-- footer -->
  <footer class="footer" id="footer">
    <div class="container footer-contact">
      <!-- text -->
      <div class="contact">
        <h4>Контакты</h4>
        <!-- phone -->
        <div class="footerTel">
          <p>тел:</p>
          <a href="tel:+79495641922" class="">+7(949)564-19-22</a>
          <a href="tel:+79496188568" class="">+7(949)618-85-68</a>
          <a href="tel:+79497082622" class="">+7(949)708-26-22</a>
        </div>
        <div class="teleg">
          <p>telegram:</p>
          <a href="https://t.me/anna_tamozhnikova">@tamozhnikova</a>
        </div>
      </div>
      <!-- map -->
      <div class="map">
        <iframe
          src="https://yandex.ru/map-widget/v1/?ll=37.761190%2C47.988848&mode=search&ol=geo&ouri=ymapsbm1%3A%2F%2Fgeo%3Fdata%3DCgoxNDQ0NTM0NTUwEhrQoNC-0YHRltGPLCDQlNC-0L3QtdGG0YzQuiIKDR42F0IVRBBAQg%2C%2C&z=11.74"
          width="100%" height="100%" frameborder="0" loading="lazy" class="map-footer">
        </iframe>
      </div>
    </div>
  </footer>
</template>

<style scoped></style>