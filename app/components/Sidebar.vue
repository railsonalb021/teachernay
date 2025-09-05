<script setup lang="ts">
const menuOpen = ref(false)
</script>

<template>
  <nav>
    <div class="fixed inset-y-0 flex flex-col items-center left-0 w-64 bg-gradient-to-b from-[#ee534e] via-[#db2929] to-[#942b2b] border-r-2 border-gray-600 text-white p-5">
      <img src="/logonay.png" alt="Logo CBPF" class="mx-auto w-52 mb-5 bg-white border-2 border-red-900 rounded-full p-2" />
      <ul class="space-y-20 pt-16 font-bold">
        <li class="group flex items-center gap-2 -ml-10 cursor-pointer hover:scale-105 transition-all">
          <NuxtLink to="/" class="text-3xl text-white group-hover:text-white group-hover:font-bold">
            INÍCIO
          </NuxtLink>
        </li>
        <li class="group flex items-center gap-2 -ml-10 cursor-pointer hover:scale-105 transition-all">
          <NuxtLink to="/sobre" class="text-3xl text-white group-hover:text-white group-hover:font-bold">
            CONTATO
          </NuxtLink>
        </li>
        <li class="group flex items-center gap-2 -ml-10 cursor-pointer hover:scale-105 transition-all">
          <NuxtLink to="/contato" class="text-3xl text-white group-hover:text-white group-hover:font-bold">
            PORTAL<br>DO ALUNO
          </NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>
