<script setup lang="ts">
import { Icon } from '@iconify/vue'
</script>

<template>
   <div class="pl-40">
  <section id="aprendaingles">
   <div class="flex justify-center items-center pt-20 space-x-20">
      <div>
         <h1 class="text-[#FF5858] text-3xl font-bold">APRENDA INGLÊS </h1>
         <h1 class="text-[#FF5858] text-3xl font-bold">DE FORMA</h1>
         <h1 class="text-[#FF5858] text-3xl font-bold">PERSONALIZADA</h1>
         <button class="bg-[#FF5858] text-white px-16 py-3 rounded-lg mt-5 hover:bg-red-500 ease-out transition-all duration-300 hover:scale-105">
            Comece Agora!
         </button>
      </div>
       <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-96 h-60 flex justify-center items-center">
          <Icon icon="mdi:play" class="text-9xl text-white"/>
       </div>
   </div>

      <div class="flex justify-center items-center pt-20 space-x-24">
          <div class="flex flex-col items-center">
             <Icon icon="mdi:desktop-mac" class="text-9xl text-[#FF5858]" />
             <h2 class="text-[#FF5858] text-2xl mt-4 text-center underline underline-offset-8">Aulas 100% online</h2>
           </div>

           <div class="flex flex-col items-center">
             <Icon icon="mdi:clock" class="text-9xl text-[#FF5858]" />
             <h2 class="text-[#FF5858] text-2xl mt-4 text-center underline underline-offset-8">Horários Flexíveis</h2>
           </div>

           <div class="flex flex-col items-center">
             <Icon icon="mdi:book" class="text-9xl text-[#FF5858]" />
             <h2 class="text-[#FF5858] text-2xl mt-4 text-center underline underline-offset-8">Material Exclusivo</h2>
           </div>
      </div>
   </section>

   <section id="sobreocurso">
      <div class="flex flex-col items-center pt-20 space-y-10">
          <h1 class="text-[#FF5858] text-3xl font-bold underline underline-offset-8">POR QUE ESCOLHER NOSSO CURSO?</h1>
         <div class="grid grid-cols-3 gap-8">
            <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-96 h-60 flex justify-center items-center">
               <Icon icon="mdi:play" class="text-9xl text-white"/>
            </div>
            <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-96 h-60 flex justify-center items-center">
               <Icon icon="mdi:play" class="text-9xl text-white"/>
            </div>
            <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-96 h-60 flex justify-center items-center">
               <Icon icon="mdi:play" class="text-9xl text-white"/>
            </div>
         </div>
      </div>
   </section>

   <section id="avaliacoes">
      <div class="flex flex-col items-center pt-20 space-y-10">
          <h1 class="text-[#FF5858] text-3xl font-bold underline underline-offset-8">AVALIAÇÕES</h1>
         <div class="grid grid-cols-2 gap-8">
            <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-96 h-60 flex flex-col justify-start p-6">
               <span class="mb-4">
                  "As aulas de inglês superaram minhas expectativas! O material é prático, as explicações são claras e consigo aplicar o que aprendo no meu dia a dia."
               </span>
               <div class="flex items-center gap-2 mt-auto">
                  <Icon icon="mdi:circle" class="text-4xl text-[#FF5858]" />
                  <span class="font-semibold text-lg">João Silva</span>
               </div>
            </div>

            <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-96 h-60 flex flex-col justify-start p-6">
               <span class="mb-4">
                  "As aulas de inglês superaram minhas expectativas! O material é prático, as explicações são claras e consigo aplicar o que aprendo no meu dia a dia."
               </span>
               <div class="flex items-center gap-2 mt-auto">
                  <Icon icon="mdi:circle" class="text-4xl text-[#FF5858]" />
                  <span class="font-semibold text-lg">Maria Souza</span>
               </div>
            </div>
         </div>
      </div>
    </section>

    <section id="contato">
      <div class="flex flex-col items-center pt-20 space-y-10 mb-20">
          <h1 class="text-[#FF5858] text-3xl font-bold underline underline-offset-8">ENTRE EM CONTATO</h1>
         <form class="flex flex-col space-y-4 w-96">
            <input type="text" placeholder="Nome" class="border border-gray-300 hover:border-[#FF5858] ease-out transition-all duration-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#FF5858]" />
            <input type="email" placeholder="Email" class="border border-gray-300 hover:border-[#FF5858] ease-out transition-all duration-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#FF5858]" />
            <textarea placeholder="Mensagem" class="border border-gray-300 hover:border-[#FF5858] ease-out transition-all duration-300 rounded-lg px-4 py-2 h-32 resize-none focus:outline-none focus:ring-2 focus:ring-[#FF5858]"></textarea>
            <button type="submit" class="bg-[#FF5858] text-white px-16 py-3 rounded-lg mt-5 hover:bg-red-500 ease-out transition-all duration-300 hover:scale-105">
               Enviar
            </button>
         </form>
      </div>
    </section>
   </div>
</template>