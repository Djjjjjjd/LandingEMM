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
  <header class="flex flex-col items-center min-w-[100%]">
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
    <div class="bg-white pb-[5px] md:pb-[50px] min-w-[100%]">
      <div class="container mx-auto p-5 flex">
        <div class="ml-right font-bold text-blue-950">
          <a href="/" class="text-3xl md:text-5xl"> DNS </a>
        </div>
        <div class="ml-auto flex gap-5">
          <!-- mail -->
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 rounded-full w-[40px] h-[40px] md:w-[50px] md:h-[50px] flex items-center justify-around hover:bg-blue-950 hover:text-amber-500 transition-colors">
              <a href="mailto:tamozhnikova.anna@yandex.ru" class="far fa-envelope text-xl md:text-2xl"></a>
            </div>
            <div class="text-zinc-700 md:flex md:flex-col hidden">
              <p class="text-sm">Напиши нам</p>
              <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-sm">tamozhnikova.anna@yandex.ru</a>
            </div>
          </div>
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 rounded-full w-[40px] h-[40px] md:w-[50px] md:h-[50px] flex items-center justify-around hover:bg-blue-950 hover:text-amber-500 transition-colors">
              <a href="tel:79495641922" class="fa fa-phone text-xl md:text-2xl"></a>
            </div>
            <div class="text-zinc-700  md:flex md:flex-col hidden">
              <p class="text-sm">Позвони нам</p>
              <a href="tel:79495641922" class="text-sm">+7(949)564-19-22</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- amber block -->
    <div class="container absolute top-[130px] md:top-[150px] bg-amber-500 py-5 px-10 flex items-center">
      <nav class="">
        <ul class="hidden md:flex gap-5">
          <li class=""><a href="/" class="hover:text-white transition-all">Главная</a></li>
          <li class=""><a href="#about" class="hover:text-white transition-all">О нас</a></li>
          <li class=""><a href="#work" class="hover:text-white transition-all">Наши работы</a></li>
        </ul>
      </nav>
      <div class="ml-auto text-white">
        <a href="#footer" class="bg-blue-950 px-10 py-3 hover:bg-white hover:text-blue-950 hover:scale-[102%] transition-all">Есть вопрос?</a>
      </div>
    </div>
  </header>
  <main class="bg-zinc-200">
    <!-- hero -->
    <div class="bg-[url(/img/hero.jpg)] h-190 md:h-screen bg-top md:bg-cover md:bg-fixed">
      <div class="container mx-auto pt-60 md:pt-70 flex flex-col gap-5">
        <div class="hidden md:flex gap-3 items-center bg-[rgba(255,255,255,0.3)] w-100 px-2 md:w-160 md:px-3">
          <i class="text-amber-500 fa fa-gear text-sm md:text-md"></i>
          <span class="text-xs md:text-md">Улучшить жизнь наших клиентов, предоставляя эффективные решения.</span>
        </div>
        <div class="text-white text-4xl md:text-7xl mb-10 md:mr-auto text-center md:text-left">
          <p>Признанный лидер<br>в сфере услуг</p>
        </div>
        <div class="pl-[120px] md:pl-0">
          <a href="#work" class="bg-amber-500 text-blue-950 px-10 py-3 hover:bg-blue-950 hover:text-amber-500 hover:scale-[102%] transition-all">Наши работы</a>
        </div>
      </div>
    </div>
    <!-- about us -->
    <section class="bg-white md:h-screen h-120" id="about">
      <div class="container mx-auto flex gap-1 md:gap-10 md:pt-30 pt-20 paralax">
        <div class="max-w-[50%] md:px-0 px-3 md:py-0 py-10">
          <img src="/img/IMAGE.jpg" class="img-fluid rounded-top" alt="" />
        </div>
        <div class="max-w-[50%] text-left flex flex-col gap-5 px-3 md:py-5 py-0">
          <div class="flex items-center gap-3 bg-zinc-100 px-5 py-1 ">
            <img src="/img/icongear.png" alt="icon" class="w-[30px] mdw-[50px]">
            <p class="text-sm md:text-md">Welcome to Don Stroy City</p>
          </div>
          <div class="">
            <p class="md:text-5xl text-xl text-blue-950">Мы обеспечиваем ваше будущее</p>
          </div>
          <div class="flex flex-col gap-2 md:text-sm text-xs text-zinc-700">
            <p class="hidden md:block">Компания Don Stroy City была основана в 2008 году. Мы — проверенные и надежные строители,
              которые обслуживают клиентов как в городе, так и по всей территории Донецкой области.</p>
            <p>У нас большой опыт в области бытовых и коммерческих электроустановок, и для нас не существует слишком
              маленьких работ. Наши клиенты ценят наш профессионализм, трудовую этику и конкурентоспособные цены.</p>
          </div>
          <div class="mt-auto hidden md:flex items-center gap-5">
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
    <!-- our services -->
    <section class="bg-amber-500 md:h-screen  pt-30 pb-50" id="work">
      <div class="container mx-auto flex flex-col items-center gap-10">
        <div class="flex flex-col gap-5 items-center md:px-0 px-3">
          <h3 class="md:text-5xl text-4xl text-blue-950">Другие услуги</h3>
          <p class="text-zinc-700 text-sm text-center md:text-md md:text-left">Мы предлагаем полный спектр строительных услуг для жилых и коммерческих помещений по
            разумной цене.</p>
        </div>
        <!-- blue card -->
           <div class="grid grid-cols-3 md:gap-5 gap-3 md:px-0 px-3">
             <div class="bg-blue-950 md:p-5 px-1 py-3 shadow-xl flex flex-col items-start gap-3 md:w-[300px] w-[120px] parallax-card">
               <img src="/img/conditioner.png" alt="conditioner" class="w-[35px] md:w-[55px]">
               <h4 class="md:text-xl text-sm text-amber-500">Установка кондиционеров</h4>
               <p class="text-sm text-zinc-300 hidden md:block">Услуги позволяют обслуживать всю вашу электрическую инфраструктуру,
                 начиная с тепловизионного
                 сканирования системы кондиционирования воздуха и заканчивая распределительными щитами.</p>
                 <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 md:p-5 px-2 py-3 shadow-md flex flex-col items-start gap-3 md:w-[300px] w-[120px] parallax-card">
               <img src="/img/elec.png" alt="conditioner" class="w-[35px] md:w-[55px]">
               <h4 class="md:text-xl text-sm text-amber-500">Электрический монтаж</h4>
               <p class="text-sm text-zinc-300 hidden md:block">Современные электроустановки, которые обеспечивают все необходимые электрические решения для вашего бизнеса, дома или промышленного помещения.</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 md:p-5 px-2 py-3 shadow-md flex flex-col items-start gap-3 md:w-[300px] w-[120px] parallax-card">
               <img src="/img/general.png" alt="conditioner" class="w-[35px] md:w-[55px]">
               <h4 class="md:text-xl text-sm text-amber-500">Генеральный строитель</h4>
               <p class="text-sm text-zinc-300 hidden md:block">Мы проводим безупречную оценку безопасности как коммерческих, так и жилых объектов. Наши опытные и знающие сотрудники.</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 md:p-5 px-2 py-3 shadow-md flex flex-col items-start gap-3 md:w-[300px] w-[120px] parallax-card">
               <img src="/img/security.png" alt="conditioner" class="w-[35px] md:w-[55px]">
               <h4 class="md:text-xl text-sm text-amber-500">Система безопасности</h4>
               <p class="text-sm text-zinc-300 hidden md:block">Используемый для измерения расхода, уровня температуры и давления в обрабатывающей промышленности комплекс технологий обеспечивает производительность..</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 md:p-5 px-2 py-3 shadow-md flex flex-col items-start gap-3 md:w-[300px] w-[120px] parallax-card">
               <img src="/img/service.png" alt="conditioner" class="w-[35px] md:w-[55px]">
               <h4 class="md:text-xl text-sm text-amber-500">Сервис и обслуживание</h4>
               <p class="text-sm text-zinc-300 hidden md:block">Компания DNC может обслуживать всю вашу электрическую инфраструктуру, начиная с тепловизионного сканирования ваших распределительных щитов..</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
             <div class="bg-blue-950 md:p-5 px-2 py-3 shadow-md flex flex-col items-start gap-3 md:w-[300px] w-[120px] parallax-card">
               <img src="/img/house.png" alt="conditioner" class="w-[35px] md:w-[55px]">
               <h4 class="md:text-xl text-sm text-amber-500">Расширения дома</h4>
               <p class="text-sm text-zinc-300 hidden md:block">Традиционно электроэнергия подается через столбы воздушной линии электропередачи, к которым кабель подключается к вашему зданию.</p>
               <a href="mailto:tamozhnikova.anna@yandex.ru" class="text-zinc-300 text-sm italic hover:text-white mt-auto">Спросить</a>
             </div>
           </div>
         </div>
    </section>
  </main>
  <footer class="bg-blue-950" id="footer">
    <div class="container mx-auto md:pt-30 md:pb-10 pt-5">
      <!-- frtPt -->
      <div class="flex items center">
        <div class="flex items-center md:pl-0 pl-3">
          <a href="/" class="text-white font-bold hover:text-amber-500 md:text-5xl text-3xl">DNS</a>
        </div>
        <div class="flex items center ml-auto md:gap-7 gap-3 md:pr-0 pr-3">
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div class="bg-amber-500 text-blue-950 md:text-4xl text-3xl rounded-full md:w-[70px] md:h-[70px] w-[60px] h-[60px] flex items-center justify-around hover:bg-white hover:text-amber-500 transition-colors">
              <a href="mailto:tamozhnikova.anna@yandex.ru" class="far fa-envelope"></a>
            </div>
            <div class="hidden md:flex flex-col text-zinc-200">
              <p>Напиши нам</p>
              <a href="mailto:tamozhnikova.anna@yandex.ru">tamozhnikova.anna@yandex.ru</a>
            </div>
          </div>
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 md:text-4xl text-3xl rounded-full md:w-[70px] md:h-[70px] w-[60px] h-[60px] flex items-center justify-around hover:bg-white hover:text-amber-500 transition-colors">
              <a href="/" class="fa fa-phone"></a>
            </div>
            <div class="hidden md:flex flex-col text-zinc-200">
              <p>Позвони нам</p>
              <a href="tel:79495641922">+7(949)564-19-22</a>
            </div>
          </div>
          <div class="flex gap-3 items-center hover:scale-[102%] transition-all">
            <div
              class="bg-amber-500 text-blue-950 md:text-4xl text-3xl rounded-full md:w-[70px] md:h-[70px] w-[60px] h-[60px] flex items-center justify-around hover:bg-white hover:text-amber-500 transition-colors">
              <a href="/https://yandex.ru/maps/-/CHCA4-Pl" class="fa fa-map-marker-alt"></a>
            </div>
            <div class="hidden md:flex flex-col text-zinc-200">
              <p>Локация</p>
              <a href="https://yandex.ru/maps/-/CHCA4-Pl">г. Донецк, Донецкая обл</a>
            </div>
          </div>
        </div>
      </div>
      <div class="container mx-auto md:py-10 py-5">
        <div class="w-[100%] h-[1px] bg-zinc-500"></div>
      </div>
      <div class="flex items-center md:px-0 px-3">
        <div class="max-w-[500px] md:text-xl text-sm text-white flex flex-col gap-15">
          <p>Мы здесь, чтобы удовлетворить ваши потребности в основных услугах для здания вашей мечты, будь то коммерческое, жилое или промышленное здание.</p>
          <div class="flex items-center gap-5 text-white">
            <a href="" class="bg-[rgb(44,50,101)] rounded-full md:w-20 md:h-20 w-15 h-15 flex items-center justify-around md:text-3xl text-2xl hover:bg-white hover:text-[rgb(44,50,101)] hover:scale-[102%] transition-all"><i class="fab fa-vk"></i></a>
            <a href="" class="bg-[rgb(44,50,101)] rounded-full md:w-20 md:h-20 w-15 h-15 flex items-center justify-around md:text-3xl text-2xl hover:bg-white hover:text-[rgb(44,50,101)] hover:scale-[102%] transition-all"><i class="fab fa-facebook"></i></a>
            <a href="" class="bg-[rgb(44,50,101)] rounded-full md:w-20 md:h-20 w-15 h-15 flex items-center justify-around md:text-3xl text-2xl hover:bg-white hover:text-[rgb(44,50,101)] hover:scale-[102%] transition-all"><i class="fab fa-instagram"></i></a>
            <a href="" class="bg-[rgb(44,50,101)] rounded-full md:w-20 md:h-20 w-15 h-15 flex items-center justify-around md:text-3xl text-2xl hover:bg-white hover:text-[rgb(44,50,101)] hover:scale-[102%] transition-all"><i class="fab fa-twitter"></i></a>
          </div>
        </div>
        <div class="max-w-[70%] max-h-[50%] ml-auto hidden md:block">
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
