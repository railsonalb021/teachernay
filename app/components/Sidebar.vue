<script setup lang="ts">
import { ref } from 'vue'
import { Icon } from '@iconify/vue'

const menuOpen = ref(false)

const menusFiltrados = [
  { label: "Início", link: "#inicio", icon: "heroicons:home" },
  { label: "Contato", link: "https://docs.google.com/forms/d/1MQrzkvxRuAcA2TR_3NyuO2fzP02nP2YsBUc1_J8o2XE/viewform?chromeless=1&edit_requested=true", icon: "heroicons:phone" },
  { label: "Portal do Aluno", link: "https://www.iorclass.com.br/login_aluno", icon: "heroicons:academic-cap" },
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

      <img src="/logonay.png" alt="Logo CBPF" class="mx-auto w-40 bg-white border-2 border-red-900 rounded-full p-2" />

      <ul class="space-y-7 pl-3 pt-10 flex-1">
  <li
    v-for="menu in menusFiltrados"
    :key="menu.label"
    :class="[
      'group flex font-bold items-center gap-2 cursor-pointer hover:scale-105 transition-all p-3 rounded-2xl',
      menu.label === 'Início'
        ? 'bg-white'
        : 'text-white'
    ]"
  >
    <Icon
      :icon="menu.icon"
      :class="[
        'text-2xl',
        menu.label === 'Início'
          ? 'text-[#ee534e]'
          : 'text-white'
      ]"
    />

    <NuxtLink
      :to="menu.link"
      :class="[
        'md:text-3xl text-xl font-bold',
        menu.label === 'Início'
          ? 'text-[#4b4b4b]'
          : 'text-white'
      ]"
      @click="menuOpen = false"
    >
      {{ menu.label }}
    </NuxtLink>
  </li>
</ul>
      <div class="flex justify-center items-center">
        <p class="text-lg text-center text-white font-semibold p-3 pt-5 italic">
          "O inglês pode mudar sua vida".
        </p>
        </div>
        <div class="flex justify-center text-center">
          <button
            class="bg-white text-[#FF5858] font-bold px-3 py-3 rounded-lg mt-5
                  ease-out transition-all duration-300
                  hover:scale-105 w-full flex items-center justify-center gap-2"
          >
            <span>Matrículas abertas!</span>

            <Icon
              icon="mdi:school"
              class="text-2xl text-[#FF5858]"
            />
          </button>
      </div>
      <div class="flex justify-center items-center gap-2 pt-5">
        <NuxtLink target="_blank" to="https://www.instagram.com/teacher_nah?igsh=MXU5bHNkbGFpN3B2Mg==">
      <Icon icon="mdi:instagram" class="text-white text-3xl hover:text-gray-300 ease-out transition-all duration-300 hover:scale-110" />
    </NuxtLink>
    <NuxtLink target="_blank" to="https://wa.me/5521975602163">
      <Icon icon="mdi:whatsapp" class="text-white text-3xl hover:text-gray-300 ease-out transition-all duration-300 hover:scale-110" />
    </NuxtLink>
      </div>
    </div>
  </Transition>

  <nav class="hidden lg:flex">
    <div class="fixed inset-y-0 left-0 w-64 bg-gradient-to-b from-[#ee534e] via-[#db2929] to-[#942b2b] border-r-2 border-gray-300 text-white p-5">
      <img src="/logonay.png" alt="Logo CBPF" class="mx-auto w-52 mb-5 bg-white border-2 border-red-900 rounded-full p-2" />
      <ul class="space-y-14 pl-3 pt-5 font-bold">
  <li
    v-for="menu in menusFiltrados"
    :key="menu.label"
    :class="[
      'group flex items-center gap-3 cursor-pointer hover:scale-105 transition-all p-4 rounded-2xl',
      menu.label === 'Início'
        ? 'bg-white'
        : 'text-white'
    ]"
  >
    <Icon
      :icon="menu.icon"
      :class="[
        'text-3xl',
        menu.label === 'Início'
          ? 'text-[#ee534e]'
          : 'text-white'
      ]"
    />

    <NuxtLink
      :to="menu.link"
      :class="[
        'text-2xl font-bold',
        menu.label === 'Início'
          ? 'text-[#4b4b4b]'
          : 'text-white'
      ]"
    >
      {{ menu.label }}
    </NuxtLink>
  </li>
</ul>
      <div class="flex justify-center items-center">
        <p class="text-lg text-center mt-10 text-white italic p-3 pt-10">
          "O inglês pode mudar sua vida".
        </p>
      </div>
      <div class="flex justify-center text-center">
          <button
            class="bg-white text-[#FF5858] font-bold px-3 py-3 rounded-lg mt-5
                  ease-out transition-all duration-300
                  hover:scale-105 w-full flex items-center justify-center gap-2"
          >
            <span>Matrículas abertas!</span>

            <Icon
              icon="mdi:school"
              class="text-2xl text-[#FF5858]"
            />
          </button>
      </div>
      <div class="flex justify-center items-center gap-2 pt-5">
        <NuxtLink target="_blank" to="https://www.instagram.com/teacher_nah?igsh=MXU5bHNkbGFpN3B2Mg==">
      <Icon icon="mdi:instagram" class="text-white text-3xl hover:text-gray-300 ease-out transition-all duration-300 hover:scale-110" />
    </NuxtLink>
    <NuxtLink target="_blank" to="https://wa.me/5521975602163">
      <Icon icon="mdi:whatsapp" class="text-white text-3xl hover:text-gray-300 ease-out transition-all duration-300 hover:scale-110" />
    </NuxtLink>
      </div>
    </div>
  </nav>
</template>