<script setup lang="ts">
import Item from './components/Item.vue'

// On page load or when changing themes, best to add inline in `head` to avoid FOUC
if (localStorage.theme === 'dark') {
  document.documentElement.classList.add('dark')
} else {
  document.documentElement.classList.remove('dark')
}

// Whenever the user explicitly chooses light mode
if (localStorage.theme == null) {
  localStorage.theme = 'light'
}


function dark() {
  if (localStorage.theme === 'dark') {
    localStorage.theme = 'light'
    document.documentElement.classList.remove('dark')
  } else {
    localStorage.theme = 'dark'
    document.documentElement.classList.add('dark')
  }
}

function hey() {
  alert("bruh")
}

</script>

<template>
  <html class="">

  <body>
    <div class="absolute inset-0 antialiased text-slate-500 dark:text-slate-400 bg-white dark:bg-slate-900 transition-colors">
      <div class="px-4 sm:px-6 md:max-w-2xl md:px-4 lg:max-w-4xl lg:px-12 mx-auto">
        <div class="bg-white dark:bg-slate-800 rounded-lg px-6 py-8 ring-2 ring-slate-900/5 shadow-xl mt-6 transition-colors">
          <h3 class="text-slate-900 dark:text-white text-base font-medium tracking-tight">
            Alex Eilert
          </h3>
          <p class="text-slate-500 dark:text-slate-400 mt-2 text-sm">
            Alex Eilert
          </p>
          <button class="text-slate-900 dark:text-white" @click="dark()">Dark Mode</button>
          <p id="demo"></p>
        </div>

      </div>
      <Item />
    </div>
  </body>

  </html>
</template>
