<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css';
</script>

<template>
  <header class="relative">
    <!-- opening -->
    <div class="bg-zinc-200">
      <div class="container mx-auto p-3">
        <div class="flex text-blue-950">
          <p>Окрыто с 08:00 до 21:00</p>
          <div class="ml-auto flex gap-3 text-blue-950 ">
            <a href=""><i class="fab fa-vk"></i></a>
            <a href=""><i class="fab fa-facebook"></i></a>
            <a href=""><i class="fab fa-instagram"></i></a>
            <a href=""><i class="fab fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-white pb-[50px]">
      <div class="container mx-auto p-5 flex">
        <div class="ml-right text-5xl font-bold text-blue-950">
          <a href="/">
            DNS
          </a>
        </div>
        <div class="ml-auto flex gap-5">
          <!-- mail -->
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 text-2xl rounded-full w-[50px] h-[50px] flex items-center justify-around hover:bg-blue-950 hover:text-amber-500 transition-colors">
              <a href="/" class="far fa-envelope"></a>
            </div>
            <div class="flex flex-col text-zinc-700">
              <p>Напиши нам</p>
              <a href="">Info@bluecollar.com</a>
            </div>
          </div>
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 text-2xl rounded-full w-[50px] h-[50px] flex items-center justify-around hover:bg-blue-950 hover:text-amber-500 transition-colors">
              <a href="/" class="fa fa-phone"></a>
            </div>
            <div class="flex flex-col text-zinc-700">
              <p>Позвони нам</p>
              <a href="">+7949 000 00</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container absolute right-[10%] top-[150px] bg-amber-500 py-3 px-10 flex items-center">
      <nav class="">
        <ul class="flex gap-5">
          <li class=""><a href="/" class="hover:text-white transition-all">Главная</a></li>
          <li class=""><a href="/" class="hover:text-white transition-all">О нас</a></li>
          <li class=""><a href="/" class="hover:text-white transition-all">Наши работы</a></li>
        </ul>
      </nav>
      <div class="ml-auto text-white">
        <button class="bg-blue-950 px-10 py-3 hover:bg-white hover:text-blue-950 hover:scale-[102%] transition-all">Есть
          вопрос?</button>
      </div>
    </div>
  </header>

  <main class="bg-zinc-200 h-screen">
    <!-- hero -->
    <div class="bg-[url(/img/hero.jpg)] h-screen bg-cover bg-fixed">
      <div class="container mx-auto pt-70 flex flex-col gap-5">
        <div class="flex gap-3 items-center bg-[rgba(255,255,255,0.3)] w-160 px-3">
          <i class="text-amber-500 fa fa-gear"></i>
          <span class="flex">Улучшить жизнь наших клиентов, предоставляя эффективные решения.</span>
        </div>
        <div class=" text-white text-7xl mb-10">
          <p>Признанный лидер<br>в сфере услуг</p>
        </div>
        <div class="">
          <button
            class="bg-amber-500 text-blue-950 px-10 py-3 hover:bg-blue-950 hover:text-amber-500 hover:scale-[102%] transition-all">Наши
            работы</button>
        </div>
      </div>
    </div>
    <!-- about us -->
    <section class="bg-white h-screen">
      <div class="container mx-auto flex gap-10 pt-30">
        <div class="max-w-[50%]">
          <img src="/img/IMAGE.jpg" class="img-fluid rounded-top" alt="" />
        </div>
        <div class="max-w-[50%] text-left flex flex-col gap-5 px-3 py-5">
          <div class="flex items-center gap-3 bg-zinc-100 px-5 py-1">
            <img src="/img/icongear.png" alt="icon">
            <p>Welcome to Don Stroy City</p>
          </div>
          <div class="">
            <p class="text-5xl text-blue-950">Мы обеспечиваем ваше будущее</p>
          </div>
          <div class="flex flex-col gap-2 text-sm text-zinc-700">
            <p>Компания Don Stroy City была основана в 2008 году. Мы — проверенные и надежные строители,
              которые обслуживают клиентов как в городе, так и по всей территории Донецкой области.</p>
            <p>У нас большой опыт в области бытовых и коммерческих электроустановок, и для нас не существует слишком
              маленьких работ. Наши клиенты ценят наш профессионализм, трудовую этику и конкурентоспособные цены.</p>
          </div>
          <div class="mt-auto flex items-center gap-5">
            <div class="w-[250px] h-[250px] bg-zinc-100 flex items-center flex-col pt-8">
              <p class="text-9xl text-amber-500">17</p>
              <p class="text-3xl text-blue-950">Лет опыта</p>
            </div>
            <div class="text-zinc-700">
              <ul class="flex flex-col gap-4">
                <li>- Для всех ваших системных требований</li>
                <li>- Все работы выполняются квалифицированными специалистами</li>
                <li>- Опытный офисный персонал на связи</li>
                <li>- Полная гарантия на качество изготовления</li>
                <li>- Properties at a reasonable price.</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- what we ofer -->
    <section class="relative bg-amber-500 h-screen pt-50">
      <div class="container mx-auto">
        <div class="flex flex-col gap-5 items-center">
          <div class="bg-[rgba(255,255,255,0.7)] px-2 py-1 flex items-center gap-3">
            <img src="/img/icongear.png" class="img-fluid rounded-top" alt="" />
            <p>Что вы получаете</p>
          </div>
          <div class="flex flex-col items-center gap-5">
            <h3 class="text-blue-950 text-5xl">Основные профессиональные услуги</h3>
            <p class="text-blue-950 max-w-[1000px] text-center">У нас большой опыт в области косметических и глобальных
              строительных работ,
              и для нас не
              существует слишком
              маленьких работ. Наши клиенты ценят наш профессионализм, трудовую этику и конкурентоспособные цены.</p>
          </div>
          <div class="flex gap-10 mt-5">
            <div
              class="flex items-center gap-3 outline-2 outline-blue-950 px-5 py-3 text-blue-950 hover:bg-white hover:outline-none hover:scale-[102%] transition-all">
              <img src="/img/commercial.png" class="img-fluid rounded-top" alt="" />
              <p>Коммерческий</p>
            </div>
            <div
              class="flex items-center gap-3 outline-2 outline-blue-950 px-5 py-3 text-blue-950 hover:bg-white hover:outline-none hover:scale-[102%] transition-all">
              <img src="/img/residential.png" class="img-fluid rounded-top" alt="" />
              <p>Жилой</p>
            </div>
            <div
              class="flex items-center gap-3 outline-2 outline-blue-950 px-5 py-3 text-blue-950 hover:bg-white hover:outline-none hover:scale-[102%] transition-all">
              <img src="/img/Industrial.png" class="img-fluid rounded-top" alt="" />
              <p>Промышленный</p>
            </div>
          </div>
          <div class="bg-white absolute p-5 top-140 shadow-2xl">
            <div class="flex items-center">
              <div class="max-w-[40%]">
                <div class="bg-zinc-100 px-2 py-1 flex items-center gap-3 max-w-45">
                  <img src="/img/commercialy.png" alt="commercialy">
                  <p>Коммерческий</p>
                </div>
                <div class="flex flex-col gap-5">
                  <h3 class="text-3xl text-blue-950">Коммерческий</h3>
                  <p>Компания Don Stroy City предлагает полный спектр строительных услуг в
                    соответствии с вашими потребностями.</p>
                </div>
              </div>
              <div class=" w-[416px] ml-auto">
                <img src="/img/electrical.png" alt="electrical">
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- our services -->
    <section class="bg-zinc-300 pt-80">
      <div class="container mx-auto flex flex-col items-center gap-10">
        <div class=" flex flex-col gap-5 items-center">
          <h3 class="text-5xl text-blue-950">Другие услуги</h3>
          <p class="text-zinc-700">Мы предлагаем полный спектр строительных услуг для жилых и коммерческих помещений по
            разумной цене.</p>
        </div>
        <div class="grid grid-cols-3 gap-5">
          <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px]">
            <img src="/img/conditioner.png" alt="conditioner">
            <h4 class="text-xl text-amber-500">Установка кондиционеров</h4>
            <p class="text-sm text-zinc-300 ">Услуги позволяют обслуживать всю вашу электрическую инфраструктуру,
              начиная с тепловизионного
              сканирования системы кондиционирования воздуха и заканчивая распределительными щитами.</p>
          </div>
          <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px]">
            <img src="/img/conditioner.png" alt="conditioner">
            <h4 class="text-xl text-amber-500">Установка кондиционеров</h4>
            <p class="text-sm text-zinc-300 ">Услуги позволяют обслуживать всю вашу электрическую инфраструктуру,
              начиная с тепловизионного
              сканирования системы кондиционирования воздуха и заканчивая распределительными щитами.</p>
          </div>
          <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px]">
            <img src="/img/conditioner.png" alt="conditioner">
            <h4 class="text-xl text-amber-500">Установка кондиционеров</h4>
            <p class="text-sm text-zinc-300 ">Услуги позволяют обслуживать всю вашу электрическую инфраструктуру,
              начиная с тепловизионного
              сканирования системы кондиционирования воздуха и заканчивая распределительными щитами.</p>
          </div>
          <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px]">
            <img src="/img/conditioner.png" alt="conditioner">
            <h4 class="text-xl text-amber-500">Установка кондиционеров</h4>
            <p class="text-sm text-zinc-300 ">Услуги позволяют обслуживать всю вашу электрическую инфраструктуру,
              начиная с тепловизионного
              сканирования системы кондиционирования воздуха и заканчивая распределительными щитами.</p>
          </div>
          <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px]">
            <img src="/img/conditioner.png" alt="conditioner">
            <h4 class="text-xl text-amber-500">Установка кондиционеров</h4>
            <p class="text-sm text-zinc-300 ">Услуги позволяют обслуживать всю вашу электрическую инфраструктуру,
              начиная с тепловизионного
              сканирования системы кондиционирования воздуха и заканчивая распределительными щитами.</p>
          </div>
          <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px]">
            <img src="/img/conditioner.png" alt="conditioner">
            <h4 class="text-xl text-amber-500">Установка кондиционеров</h4>
            <p class="text-sm text-zinc-300 ">Услуги позволяют обслуживать всю вашу электрическую инфраструктуру,
              начиная с тепловизионного
              сканирования системы кондиционирования воздуха и заканчивая распределительными щитами.</p>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
