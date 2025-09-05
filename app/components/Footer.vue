<script setup lang="ts">
import { Icon } from '@iconify/vue'
</script>

<template>
<footer
  class="w-full h-20 mt-10 border-t border-[#FF5858] bg-white transition-colors duration-300"
>
  <div class="h-full flex justify-center items-center pl-40 gap-6">
    <NuxtLink target="_blank" to="https://www.instagram.com/teacher_nah?igsh=MXU5bHNkbGFpN3B2Mg==">
      <Icon icon="mdi:instagram" class="text-[#FF5858] text-3xl hover:text-red-500 ease-out transition-all duration-300 hover:scale-110" />
    </NuxtLink>
    <NuxtLink target="_blank" to="https://wa.me/5521996965030">
      <Icon icon="mdi:whatsapp" class="text-[#FF5858] text-3xl hover:text-red-500 ease-out transition-all duration-300 hover:scale-110" />
    </NuxtLink>
  </div>
</footer>

</template>
