<script setup>
import { ref } from 'vue'

const currentTab = ref('home')

const setTab = (tab) => {
  currentTab.value = tab
  const target = document.getElementById(tab)
  if (target) {
    target.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<template>
  <header class="">
    <div class="container nav">
      <div class="">
        <a href="/" class="header-logo">DCS</a>
      </div>
      <div class="nav-block">
        <ul class="nav-link">
          <li class="hn-link">
            <a href="#home" class="link">Главная</a>
          </li>
          <li class="hn-link">
            <a href="#work" class="link">Наши работы</a>
          </li>
          <li class="hn-link">
            <a href="#contact" class="link">Контакт</a>
          </li>
        </ul>
      </div>
    </div>
  </header>
  <main class="main">
    <section id="home">
      <!-- heroSection -->
      <div class="hero">
        <!-- text -->
        <div class="hero-text">
          <h1 class="h1">
            don <br> city <br> stroy <br>
          </h1>
        </div>
        <!-- image -->
        <div class="hero-image">
          <img src="/image/heroimage.png" alt="hero image">
        </div>
      </div>
      <!-- item -->
       <div class="home_item">
        <!-- image -->
        <div class="item-image">
          <img src="/image/photo.png" alt="photo">
        </div>
        <!-- text + buttons-->
         <div class="item-info">
          <!-- TEXT -->
            <div class="item-info_text">
              <h3 class="">Эммануил Таможников</h3>
              <p class="subTitle">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem, assumenda. </p>
            </div>
            <!-- BUTTONS -->
            <div class="item-info_btn">
              <a href="tel:+79497560061" class="phone">
                <i class="fas fa-phone"></i>
              </a>
              <a type="mail" href="https://t.me/emmanuil_tamozhnikov" class="mail">
                <i class="fa-solid fa-paper-plane"></i>
              </a>
            </div>
         </div>
       </div>
    </section>
    <section id="work">
      <div class="work">
        <!-- text -->
         <div class="">
          <h2>Фото<br>Наших<br>работ</h2>
         </div>
      </div>
    </section>
    <section id="contact"></section>
  </main>
</template>

<style scoped>

</style>
