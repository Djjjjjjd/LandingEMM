<script setup>
import { onMounted, onUnmounted } from 'vue'

function parallaxScroll() {
  const cards = document.querySelectorAll('.paralax')
  cards.forEach((card, i) => {
    // Чем больше i, тем меньше скорость (эффект глубины)
    const speed = 0.03 + i * 0.05
    card.style.transform = `translateY(${window.scrollY * speed}px)`
  })
}

onMounted(() => {
  window.addEventListener('scroll', parallaxScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', parallaxScroll)
})
</script>

<template>
  <header class="relative flex flex-col items-center">
    <!-- opening -->
    <div class="bg-zinc-200 min-w-[100%]">
      <div class="container mx-auto p-3">
        <div class="flex text-blue-950">
          <p>Окрыто с 08:00 до 21:00</p>
          <div class="ml-auto flex gap-3 text-blue-950 ">
            <a href="https://vk.com/feed"><i class="fab fa-vk"></i></a>
            <a href="https://www.facebook.com/?locale=ru_RU"><i class="fab fa-facebook"></i></a>
            <a href="https://www.instagram.com/"><i class="fab fa-instagram"></i></a>
            <a href="https://x.com/"><i class="fab fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </div>
    <!-- dns block -->
    <div class="bg-white pb-[50px] min-w-[100%]">
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
              <a href="mail:">Info@bluecollar.com</a>
            </div>
          </div>
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 text-2xl rounded-full w-[50px] h-[50px] flex items-center justify-around hover:bg-blue-950 hover:text-amber-500 transition-colors">
              <a href="/" class="fa fa-phone"></a>
            </div>
            <div class="flex flex-col text-zinc-700">
              <p>Позвони нам</p>
              <a href="tel:79495641922">+7(949)564-19-22</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- amber block -->
    <div class="container absolute top-[150px] bg-amber-500 py-5 px-10 flex items-center">
      <nav class="">
        <ul class="flex gap-5">
          <li class=""><a href="/" class="hover:text-white transition-all">Главная</a></li>
          <li class=""><a href="#about" class="hover:text-white transition-all">О нас</a></li>
          <li class=""><a href="#work" class="hover:text-white transition-all">Наши работы</a></li>
        </ul>
      </nav>
      <div class="ml-auto text-white">
        <a href="#footer" class="bg-blue-950 px-10 py-3 hover:bg-white hover:text-blue-950 hover:scale-[102%] transition-all">Есть
          вопрос?</a>
      </div>
    </div>
  </header>

  <main class="bg-zinc-200">
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
    <section class="bg-white h-screen" id="about">
      <div class="container mx-auto flex gap-10 pt-30 paralax">
        <div class="max-w-[50%] ">
          <img src="/img/IMAGE.jpg" class="img-fluid rounded-top" alt="" />
        </div>
        <div class="max-w-[50%] text-left flex flex-col gap-5 px-3 py-5">
          <div class="flex items-center gap-3 bg-zinc-100 px-5 py-1 ">
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
    <!-- our services -->
    <section class="bg-amber-500 h-screen pt-30 pb-50" id="work">
      <div class="container mx-auto flex flex-col items-center gap-10">
        <div class=" flex flex-col gap-5 items-center">
          <h3 class="text-5xl text-blue-950">Другие услуги</h3>
          <p class="text-zinc-700">Мы предлагаем полный спектр строительных услуг для жилых и коммерческих помещений по
            разумной цене.</p>
        </div>
        <!-- blue card -->
           <div class="grid grid-cols-3 gap-5 ">
             <div class="bg-blue-950 p-5 shadow-xl flex flex-col items-start gap-3 w-[300px] parallax-card">
               <img src="/img/conditioner.png" alt="conditioner">
               <h4 class="text-xl text-amber-500">Установка кондиционеров</h4>
               <p class="text-sm text-zinc-300 ">Услуги позволяют обслуживать всю вашу электрическую инфраструктуру,
                 начиная с тепловизионного
                 сканирования системы кондиционирования воздуха и заканчивая распределительными щитами.</p>
                 <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px] parallax-card">
               <img src="/img/elec.png" alt="conditioner">
               <h4 class="text-xl text-amber-500">Электрический монтаж</h4>
               <p class="text-sm text-zinc-300 ">Современные электроустановки, которые обеспечивают все необходимые электрические решения для вашего бизнеса, дома или промышленного помещения.</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px] parallax-card">
               <img src="/img/general.png" alt="conditioner">
               <h4 class="text-xl text-amber-500">Генеральный строитель</h4>
               <p class="text-sm text-zinc-300 ">Мы проводим безупречную оценку безопасности как коммерческих, так и жилых объектов. Наши опытные и знающие сотрудники.</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px] parallax-card">
               <img src="/img/security.png" alt="conditioner">
               <h4 class="text-xl text-amber-500">Система безопасности</h4>
               <p class="text-sm text-zinc-300 ">Используемый для измерения расхода, уровня температуры и давления в обрабатывающей промышленности комплекс технологий обеспечивает производительность..</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px] parallax-card">
               <img src="/img/service.png" alt="conditioner">
               <h4 class="text-xl text-amber-500">Сервис и обслуживание</h4>
               <p class="text-sm text-zinc-300 ">Компания DNC может обслуживать всю вашу электрическую инфраструктуру, начиная с тепловизионного сканирования ваших распределительных щитов..</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 p-5 shadow-md flex flex-col items-start gap-3 w-[300px] parallax-card">
               <img src="/img/house.png" alt="conditioner">
               <h4 class="text-xl text-amber-500">Расширения дома</h4>
               <p class="text-sm text-zinc-300 ">Традиционно электроэнергия подается через столбы воздушной линии электропередачи, к которым кабель подключается к вашему зданию.</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
           </div>
         </div>
    </section>
  </main>
  <footer class="bg-blue-950" id="footer">
    <div class="container mx-auto pt-30 pb-10">
      <!-- frtPt -->
      <div class="flex items center">
        <div class="flex items-center">
          <a href="/" class="text-white font-bold hover:text-amber-500 text-5xl">DNS</a>
        </div>
        <div class="flex items center ml-auto gap-7">
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 text-4xl rounded-full w-[70px] h-[70px] flex items-center justify-around hover:bg-white hover:text-amber-500 transition-colors">
              <a href="/" class="far fa-envelope"></a>
            </div>
            <div class="flex flex-col text-zinc-200">
              <p>Напиши нам</p>
              <a href="">Info@bluecollar.com</a>
            </div>
          </div>
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 text-4xl rounded-full w-[70px] h-[70px] flex items-center justify-around hover:bg-white hover:text-amber-500 transition-colors">
              <a href="/" class="fa fa-phone"></a>
            </div>
            <div class="flex flex-col text-zinc-200">
              <p>Позвони нам</p>
              <a href="">+7949 000 00</a>
            </div>
          </div>
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 text-4xl rounded-full w-[70px] h-[70px] flex items-center justify-around hover:bg-white hover:text-amber-500 transition-colors">
              <a href="/https://yandex.ru/maps/-/CHCA4-Pl" class="fa fa-map-marker-alt"></a>
            </div>
            <div class="flex flex-col text-zinc-200">
              <p>Локация</p>
              <a href="https://yandex.ru/maps/-/CHCA4-Pl">г. Донецк, Донецкая обл</a>
            </div>
          </div>
        </div>
      </div>
      <div class="container mx-auto pt-10 pb-10">
        <div class="w-[100%] h-[1px] bg-zinc-500"></div>
      </div>
      <div class="flex items-center">
        <div class="max-w-[500px] text-xl text-white flex flex-col gap-15">
          <p>Мы здесь, чтобы удовлетворить ваши потребности в основных услугах для здания вашей мечты, будь то коммерческое, жилое или промышленное здание.</p>
          <div class="flex items-center gap-5 text-white">
            <a href="" class="bg-[rgb(44,50,101)] rounded-full w-20 h-20 flex items-center justify-around text-3xl hover:bg-white hover:text-[rgb(44,50,101)] hover:scale-[102%] transition-all"><i class="fab fa-vk"></i></a>
            <a href="" class="bg-[rgb(44,50,101)] rounded-full w-20 h-20 flex items-center justify-around text-3xl hover:bg-white hover:text-[rgb(44,50,101)] hover:scale-[102%] transition-all"><i class="fab fa-facebook"></i></a>
            <a href="" class="bg-[rgb(44,50,101)] rounded-full w-20 h-20 flex items-center justify-around text-3xl hover:bg-white hover:text-[rgb(44,50,101)] hover:scale-[102%] transition-all"><i class="fab fa-instagram"></i></a>
            <a href="" class="bg-[rgb(44,50,101)] rounded-full w-20 h-20 flex items-center justify-around text-3xl hover:bg-white hover:text-[rgb(44,50,101)] hover:scale-[102%] transition-all"><i class="fab fa-twitter"></i></a>
          </div>
        </div>
        <div class="max-w-[70%] max-h-[50%] ml-auto">
            <iframe src="https://yandex.ru/map-widget/v1/?from=tableau_yabro&ll=37.802850%2C48.015877&mode=poi&poi%5Bpoint%5D=37.802773%2C48.016011&poi%5Buri%5D=ymapsbm1%3A%2F%2Fgeo%3Fdata%3DCgoxNDQ0NTM0NTUwEh7Qo9C60YDQsNGX0L3QsCwg0JTQvtC90LXRhtGM0LoiCg0eNhdCFUQQQEI%2C&z=12"  allowfullscreen="true" class="w-[800px] h-[500px]">
            </iframe>
        </div>
      </div>
      <div class="container mx-auto pt-15 pb-3">
        <div class="w-[100%] h-[1px] bg-zinc-500"></div>
      </div>
    </div>
  </footer>
</template>
