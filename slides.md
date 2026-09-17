---
theme: default
transition: slide-left
comark: true
fonts:
  sans: Ubuntu
  mono: Ubuntu Mono
  weights: 300,400,500,700
---

<div class="text-left">

 <div class="absolute inset-0 flex flex-col items-start justify-center text-left px-16">
    <h1 class="!m-0">Технология VPN</h1>
    <h2 class="!m-0 !mt-2">Архитектура, протоколы, безопасность</h2>
  </div>

  <div class="absolute bottom-10 left-16 text-left">
    <p class="!text-sm !text-[#475569] !m-0">Выполнили студенты группы ИВТб-4302:</p>
    <p class="!text-sm !text-[#475569] !m-0 mt-1">Репин Иван Алексеевич</p>
    <p class="!text-sm !text-[#475569] !m-0">Репина Марина Андреевна</p>
  </div>

</div>

---
layout: default
---

<div class="h-full w-full flex items-center">

  <!-- Заголовок -->
  <div class="shrink-0">
    <h1 class="!m-0 !text-left">
      Что такое VPN?
    </h1>
  </div>

  <!-- Лупа -->
  <div class="flex-1 h-full flex items-center justify-center">
    <svg
      width="260"
      height="260"
      viewBox="0 0 24 24"
      fill="none"
      stroke="#1D4ED8"
      stroke-width="1.3"
      stroke-linecap="round"
      stroke-linejoin="round"
    >
      <circle cx="10.5" cy="10.5" r="6.5" />
      <path d="M15.3 15.3L21 21" />
    </svg>
  </div>

</div>

---
layout: default
---

<div class="h-full w-full flex flex-col justify-center px-6">

  <div class="max-w-5xl w-full mx-auto">

  <h1 class="!m-0 !text-left">Virtual Private Network</h1>

  <h3 v-click class="!mt-2 !mb-16 !text-left !font-normal !text-[#94A3B8] !text-xl">
      Виртуальная частная сеть
  </h3>

  <div class="grid grid-cols-3 gap-6 text-left">

  <div v-click class="!rounded-xl !p-6 !border-2 !border-[#E2E8F0]">
        <div class="!mb-3">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="#1D4ED8" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <rect x="3" y="11" width="18" height="11" rx="2" ry="2"></rect>
            <path d="M7 11V7a5 5 0 0 1 10 0v4"></path>
          </svg>
        </div>
        <h3 class="!m-0 !mb-2 !text-[#0F172A] !text-xl">Конфиденциальность</h3>
        <p class="!m-0 !text-sm !text-[#475569]">
          Трафик шифруется, данные недоступны посторонним
        </p>
      </div>

  <div v-click class="!rounded-xl !p-6 !border-2 !border-[#E2E8F0]">
        <div class="!mb-3">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="#1D4ED8" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"></path>
            <path d="M9 12l2 2 4-4"></path>
          </svg>
        </div>
        <h3 class="!m-0 !mb-2 !text-[#0F172A] !text-xl">Целостность</h3>
        <p class="!m-0 !text-sm !text-[#475569]">
          Данные нельзя незаметно изменить по пути
        </p>
      </div>

  <div v-click class="!rounded-xl !p-6 !border-2 !border-[#E2E8F0]">
        <div class="!mb-3">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="#1D4ED8" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
            <path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path>
            <path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path>
          </svg>
        </div>
        <h3 class="!m-0 !mb-2 !text-[#0F172A] !text-xl">Доступность</h3>
        <p class="!m-0 !text-sm !text-[#475569]">
          Соединение стабильно и защищено от обрывов
        </p>
      </div>

  </div>

  </div>

</div>

---
layout: default
---

<div class="h-full w-full flex items-center">

  <!-- Заголовок -->
  <div class="shrink-0">
    <h1 class="!m-0 !text-left">
      Архитектура
    </h1>
  </div>

  <!-- Иконка по центру оставшейся области -->
  <div class="flex-1 h-full flex items-center justify-center">
    <svg
      width="260"
      height="260"
      viewBox="0 0 24 24"
      fill="none"
      stroke="#1D4ED8"
      stroke-width="1.3"
      stroke-linecap="round"
      stroke-linejoin="round"
    >
      <!-- Соединения -->
      <path d="M12 5V7.3" />
      <path d="M12 16.7V19" />
      <path d="M5.6 8.6L7.6 9.7" />
      <path d="M16.4 9.7L18.4 8.6" />
      <path d="M5.6 15.4L7.6 14.3" />
      <path d="M16.4 14.3L18.4 15.4" />
      <!-- Центральный узел -->
      <rect x="8" y="8" width="8" height="8" rx="2" />
      <!-- Внешние узлы -->
      <circle cx="12" cy="3" r="2" />
      <circle cx="12" cy="21" r="2" />
      <circle cx="3.8" cy="7.5" r="2" />
      <circle cx="20.2" cy="7.5" r="2" />
      <circle cx="3.8" cy="16.5" r="2" />
      <circle cx="20.2" cy="16.5" r="2" />
      <!-- Деталь центрального узла -->
      <circle cx="12" cy="12" r="1.5" />
    </svg>
  </div>

</div>

---
layout: default
---

<div class="absolute inset-0 flex flex-col items-center justify-center text-left px-16">

  <h1 class="!m-0">
    Спасибо за внимание!
  </h1>

  <h2 class="!m-0">
    Готовы ответить на вопросы
  </h2>

</div>
