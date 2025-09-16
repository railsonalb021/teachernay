<script setup lang="ts">
import { ref } from 'vue'
import { Icon } from '@iconify/vue'

const menuOpen = ref(false)

const menusFiltrados = [
  { label: "Início", link: "#inicio", icon: "heroicons:home" },
  { label: "Contato", link: "#contato", icon: "heroicons:phone" },
  { label: "Portal do Aluno", link: "/contato", icon: "heroicons:academic-cap" },
]
</script>

<template>
  <div class="fixed inset-x-0 top-0 flex items-center justify-between bg-red-500 p-4 text-white lg:hidden">
    <button @click="menuOpen = true" class="focus:outline-none">
      <Icon icon="heroicons-solid:bars-3" class="text-2xl text-white" />
    </button>
  </div>

  <Transition
    enter-active-class="transition duration-300 ease-out transform"
    enter-from-class="-translate-x-full"
    enter-to-class="translate-x-0"
    leave-active-class="transition duration-300 ease-in transform"
    leave-from-class="translate-x-0"
    leave-to-class="-translate-x-full"
  >
    <div
      v-show="menuOpen"
      class="fixed left-0 top-0 z-40 h-screen w-64 bg-gradient-to-b from-[#ee534e] via-[#db2929] to-[#942b2b] p-5 text-white lg:hidden flex flex-col"
    >
      <div class="flex justify-start">
        <button @click="menuOpen = false" class="focus:outline-none">
          <Icon icon="heroicons:x-mark" class="text-3xl text-white" />
        </button>
      </div>

      <img src="/logonay.png" alt="Logo CBPF" class="mx-auto w-40 mb-10 bg-white border-2 border-red-900 rounded-full p-2" />

      <ul class="space-y-16 pl-3 pt-10 flex-1">
        <li
          v-for="menu in menusFiltrados"
          :key="menu.label"
          class="group flex font-bold items-center gap-2 cursor-pointer hover:scale-105 transition-all"
        >
          <Icon :icon="menu.icon" class="text-2xl" />
          <NuxtLink
            :to="menu.link"
            class="text-3xl text-white group-hover:font-bold"
            @click="menuOpen = false"
          >
            {{ menu.label }}
          </NuxtLink>
        </li>
      </ul>
    </div>
  </Transition>

  <nav class="hidden lg:flex">
    <div class="fixed inset-y-0 left-0 w-64 bg-gradient-to-b from-[#ee534e] via-[#db2929] to-[#942b2b] border-r-2 border-gray-300 text-white p-5">
      <img src="/logonay.png" alt="Logo CBPF" class="mx-auto w-52 mb-5 bg-white border-2 border-red-900 rounded-full p-2" />
      <ul class="space-y-20 pl-3 pt-16 font-bold">
        <li
          v-for="menu in menusFiltrados"
          :key="menu.label"
          class="group flex font-bold items-center gap-2 cursor-pointer hover:scale-105 transition-all"
        >
          <Icon :icon="menu.icon" class="text-3xl" />
          <NuxtLink
            :to="menu.link"
            class="text-3xl text-white group-hover:font-bold"
          >
            {{ menu.label }}
          </NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>
