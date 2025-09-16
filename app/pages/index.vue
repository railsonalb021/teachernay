<script setup lang="ts">
import { Icon } from '@iconify/vue'

const nome = ref("")
const email = ref("")
const mensagem = ref("")

const enviarWhatsApp = () => {
  const telefone = "5521975602163" // número do WhatsApp (com DDI +55 e DDD)
  const texto = `Olá, meu nome é ${nome.value}%0AEmail: ${email.value}%0AMensagem: ${mensagem.value}`
  const url = `https://wa.me/${telefone}?text=${texto}`

  window.open(url, "_blank")
}
</script>

<template>
  <div class="lg:pl-40"> 
    <div class="flex flex-col lg:flex-row justify-center items-center gap-6 lg:pt-10 pt-32 bg-white p-8">
      <img 
        src="/imageprincipal.jpg" 
        alt="Logo" 
        class="w-full max-w-3xl h-[300px] lg:w-[600px] lg:h-[520px] border-2 border-[#FF5858] rounded-2xl object-cover"
      />
      <img 
        src="/imageprincipal2.jpg" 
        alt="Logo" 
        class="w-full max-w-3xl h-[300px] lg:w-[600px] lg:h-[520px] border-2 border-[#FF5858] rounded-2xl object-cover mt-6 lg:mt-0"
      />
    </div>

    <section id="inicio">
      <div class="flex flex-col lg:flex-row justify-center items-center lg:pt-40 pt-20 gap-10 lg:gap-20 text-center lg:text-left">
        <div>
          <h1 class="text-[#FF5858] text-3xl font-bold">APRENDA INGLÊS </h1>
          <h1 class="text-[#FF5858] text-3xl font-bold">DE FORMA</h1>
          <h1 class="text-[#FF5858] text-3xl font-bold">PERSONALIZADA</h1>
          <button class="bg-[#FF5858] text-white px-10 py-3 rounded-lg mt-5 hover:bg-red-500 ease-out transition-all duration-300 hover:scale-105">
            Comece Agora!
          </button>
        </div>
        <div class="rounded-2xl pt-32 lg:pt-0 w-full max-w-sm lg:max-w-md h-60 flex justify-center items-center">
          <video 
            src="/video1.mp4" 
            controls 
            muted 
            class="w-full rounded-2xl shadow-lg"
          />
        </div>
      </div>

      <div class="flex flex-col items-center pt-40 text-center px-4">
        <h1 class="text-[#FF5858] lg:text-3xl text-2xl font-bold underline underline-offset-8">POR QUE ESCOLHER NOSSO CURSO?</h1>
      </div>
      <div class="flex flex-col lg:flex-row justify-center items-center pt-20 gap-16">
        <div class="flex flex-col items-center text-center">
          <Icon icon="mdi:desktop-mac" class="text-9xl text-[#FF5858]" />
          <h2 class="text-[#FF5858] font-bold text-2xl mt-4 underline underline-offset-8">Aulas 100% online</h2>
        </div>

        <div class="flex flex-col items-center text-center">
          <Icon icon="mdi:clock" class="text-9xl text-[#FF5858]" />
          <h2 class="text-[#FF5858] font-bold text-2xl mt-4 underline underline-offset-8">Horários Flexíveis</h2>
        </div>

        <div class="flex flex-col items-center text-center">
          <Icon icon="mdi:book" class="text-9xl text-[#FF5858]" />
          <h2 class="text-[#FF5858] font-bold text-2xl mt-4 underline underline-offset-8">Material Exclusivo</h2>
        </div>
      </div>
    </section>

    <section id="sobreocurso">
      <div class="flex flex-col items-center pt-20 space-y-10 px-4">
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
          <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-80 lg:w-96 h-60 flex justify-center items-center mx-auto">
            <Icon icon="mdi:play" class="text-9xl text-[#FF5858]"/>
          </div>
          <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-80 lg:w-96 h-60 flex justify-center items-center mx-auto">
            <Icon icon="mdi:play" class="text-9xl text-[#FF5858]"/>
          </div>
          <div class="bg-gray-200 border-2 border-[#FF5858] rounded-2xl w-80 lg:w-96 h-60 flex justify-center items-center mx-auto">
            <Icon icon="mdi:play" class="text-9xl text-[#FF5858]"/>
          </div>
        </div>
      </div>
    </section>

    <section id="avaliacoes">
      <div class="flex flex-col items-center pt-20 space-y-10 px-4">
        <h1 class="text-[#FF5858] text-3xl font-bold underline underline-offset-8">FEED BACK</h1>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
          <img src="/1.jpg" alt="Avaliação 1" class="w-full max-w-md h-96 object-cover rounded-2xl border-2 border-[#FF5858] mx-auto" />
          <img src="/2.jpg" alt="Avaliação 2" class="w-full max-w-md h-96 object-cover rounded-2xl border-2 border-[#FF5858] mx-auto" />
        </div>
      </div>
    </section>

    <section id="contato">
    <div class="flex flex-col items-center pt-20 space-y-10 mb-20 px-4">
      <h1 class="text-[#FF5858] text-3xl font-bold underline underline-offset-8">
        ENTRE EM CONTATO
      </h1>

      <form
        class="flex flex-col space-y-4 w-full max-w-md"
        @submit.prevent="enviarWhatsApp"
      >
        <input
          type="text"
          v-model="nome"
          placeholder="Nome"
          class="border border-gray-300 hover:border-[#FF5858] ease-out transition-all duration-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#FF5858]"
        />
        <input
          type="email"
          v-model="email"
          placeholder="Email"
          class="border border-gray-300 hover:border-[#FF5858] ease-out transition-all duration-300 rounded-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-[#FF5858]"
        />
        <textarea
          v-model="mensagem"
          placeholder="Mensagem"
          class="border border-gray-300 hover:border-[#FF5858] ease-out transition-all duration-300 rounded-lg px-4 py-2 h-32 resize-none focus:outline-none focus:ring-2 focus:ring-[#FF5858]"
        ></textarea>
        <button
          type="submit"
          class="bg-[#FF5858] text-white px-10 py-3 rounded-lg mt-5 hover:bg-red-500 ease-out transition-all duration-300 hover:scale-105"
        >
          Enviar
        </button>
      </form>
    </div>
  </section>
  </div>
</template>
