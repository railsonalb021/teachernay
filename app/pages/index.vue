<script setup lang="ts">
import { Icon } from '@iconify/vue'

const nome = ref("")
const email = ref("")
const mensagem = ref("")

const enviarWhatsApp = () => {
  const telefone = "5521975602163"
  const texto = `Olá, meu nome é ${nome.value}%0AEmail: ${email.value}%0AMensagem: ${mensagem.value}`
  const url = `https://wa.me/${telefone}?text=${texto}`

  window.open(url, "_blank")
}
</script>

<template>
  <div class="lg:pl-60"> 
    <div class="flex justify-center items-center gap-6 lg:pt-10 pt-32 bg-white">
      <img 
        src="/logoinicial.png" 
        alt="Logo" 
        class="md:w-full md:max-w-7xl w-80 rounded-2xl object-cover"
      />
    </div>

    <div class="flex justify-center items-center gap-4 mt-10">
      <Icon icon="mdi:star" class="text-2xl text-[#FF5858] hidden md:flex" />
      <h1 class="text-[#FF5858] md:text-3xl text-sm font-bold text-center">
        O MELHOR CURSO DE INGLÊS ONLINE PARA VOCÊ!
      </h1>
      <Icon icon="mdi:star" class="text-2xl hidden md:flex text-[#FF5858]" />
    </div>

    <section id="inicio">
      <div
  class="md:w-3/5 w-80 mx-auto mt-20 bg-[#FFF8F6] border border-[#F3D9D4] rounded-3xl p-6 lg:p-8 shadow-lg"
>
  <div class="flex flex-col lg:flex-row items-center">
    <div class="flex-1">
      <Icon
        icon="mdi:format-quote-open"
        class="text-7xl text-[#FF5858]"
      />

      <h2 class="text-2xl font-semibold text-gray-800 leading-relaxed">
        Metodologia exclusiva
        <br />
        para transformar
        <br />
        seu <span class="text-[#FF5858] font-bold">inglês!</span>
      </h2>

      <div class="mt-6 items-center flex justify-center md:justify-start">
        <img
          src="/logonay.png"
          alt="Teacher Nay"
          class="w-24"
        />
      </div>
    </div>

    <div class="flex-1 w-full">
      <video src="/video1.mp4" controls class="w-full rounded-2xl shadow-lg" />
    </div>
  </div>
</div>

      <div class="flex flex-col items-center pt-40 text-center px-4">
        <h1 class="text-[#FF5858] lg:text-3xl text-2xl font-bold underline underline-offset-8">POR QUE ESCOLHER NOSSO CURSO?</h1>
      </div>
      <div class="flex flex-col lg:flex-row justify-center items-center pt-20 gap-16">
        <div class="relative flex flex-col items-center text-center p-10 rounded-2xl border-[#FF5858] border-2 overflow-hidden">
          <img
            src="/fundoplayer.png"
            alt="Fundo"
            class="absolute inset-0 w-full h-full object-cover"
          />

          <div class="relative z-10 flex flex-col items-center text-center">
            <Icon icon="mdi:desktop-mac" class="text-9xl text-[#FF5858]" />

            <h2 class="text-[#FF5858] font-bold text-2xl mt-4">
              Aulas 100% online
            </h2>

            <p class="text-black font-semibold pt-2">
              Estude de onde <br />
              estiver, quando quiser.
            </p>
          </div>
        </div>

        <div class="relative flex flex-col items-center text-center p-10 rounded-2xl border-[#FF5858] border-2 overflow-hidden">
          <img
            src="/fundoplayer.png"
            alt="Fundo"
            class="absolute inset-0 w-full h-full object-cover"
          />

          <div class="relative z-10 flex flex-col items-center text-center">
            <Icon icon="mdi:clock" class="text-9xl text-[#FF5858]" />

            <h2 class="text-[#FF5858] font-bold text-2xl mt-4">
              Horários Flexíveis
            </h2>

            <p class="text-black font-semibold pt-2">
              Você escolhe o melhor <br> horário para aprender.
            </p>
          </div>
        </div>

        <div class="relative flex flex-col items-center text-center p-10 rounded-2xl border-[#FF5858] border-2 overflow-hidden">
          <img
            src="/fundoplayer.png"
            alt="Fundo"
            class="absolute inset-0 w-full h-full object-cover"
          />

          <div class="relative z-10 flex flex-col items-center text-center">
            <Icon icon="mdi:book" class="text-9xl text-[#FF5858]" />

            <h2 class="text-[#FF5858] font-bold text-2xl mt-4">
              Material Exclusivo
            </h2>

            <p class="text-black font-semibold pt-2">
              Conteúdo preparado com <br> cuidado para você.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="sobreocurso">
      <div class="flex flex-col items-center pt-20 space-y-10 px-4">
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
          <div class="relative border-2 border-[#FF5858] rounded-2xl w-80 lg:w-96 h-60 overflow-hidden mx-auto cursor-pointer group">
            <img
                src="/fundoplayer.png"
                alt="Video"
                class="absolute inset-0 w-full h-full object-cover"
              />


            <div class="absolute inset-0 flex items-center justify-center">
              <Icon
                icon="mdi:play-circle"
                class="text-7xl lg:text-8xl text-[#FF5858] transition-transform duration-300 group-hover:scale-110"
              />
            </div>
          </div>
          <div class="relative border-2 border-[#FF5858] rounded-2xl w-80 lg:w-96 h-60 overflow-hidden mx-auto cursor-pointer group">
            <img
                src="/fundoplayer.png"
                alt="Video"
                class="absolute inset-0 w-full h-full object-cover"
              />

            <div class="absolute inset-0 flex items-center justify-center">
              <Icon
                icon="mdi:play-circle"
                class="text-7xl lg:text-8xl text-[#FF5858] transition-transform duration-300 group-hover:scale-110"
              />
            </div>
          </div>
          <div class="relative border-2 border-[#FF5858] rounded-2xl w-80 lg:w-96 h-60 overflow-hidden mx-auto cursor-pointer group">
            <img
                src="/fundoplayer.png"
                alt="Video"
                class="absolute inset-0 w-full h-full object-cover"
              />

            <div class="absolute inset-0 flex items-center justify-center">
              <Icon
                icon="mdi:play-circle"
                class="text-7xl lg:text-8xl text-[#FF5858] transition-transform duration-300 group-hover:scale-110"
              />
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="avaliacoes-contato" class="py-20">
  <div class="max-w-6xl mx-auto grid grid-cols-1 lg:grid-cols-2">

    <div class="px-8 border-r border-gray-200">
      <div class="flex items-center justify-center gap-2 mb-8">
        <Icon icon="mdi:heart-outline" class="text-3xl text-[#FF5858]" />
        <h2 class="text-[#FF5858] font-bold text-3xl">
          FEED BACK
        </h2>
      </div>

      <div class="flex flex-col lg:flex-row justify-center items-center gap-6">
        <div
          class="bg-white border border-[#F6C8C8] rounded-3xl p-5 w-64 shadow-sm"
        >
          <div class="flex gap-1 text-[#FF5858] mb-4">
            <Icon icon="mdi:star" v-for="i in 5" :key="i" />
          </div>

          <h3 class="font-bold text-lg mb-3">
            Rodrigo Aguiar
          </h3>

          <p class="text-gray-700">
            "Teacher Nani, amei o aplicativo de atividades.
            Já estou organizando a minha semana!"
          </p>

          <img
            src="/teacher-feedback.png"
            class="w-32 ml-auto mt-4"
          />
        </div>

        <div
          class="bg-white border border-[#F6C8C8] rounded-3xl p-5 w-64 shadow-sm"
        >
          <div class="flex gap-1 text-[#FF5858] mb-4">
            <Icon icon="mdi:star" v-for="i in 5" :key="i" />
          </div>

          <h3 class="font-bold text-lg mb-3">
            Victoria Karolline
          </h3>

          <p class="text-gray-700">
            "Omg teacher, acabei de acordar do meu cochilinho e lembrei que sonhei conversando em Inglês"
          </p>

          <img
            src="/teacher-feedback.png"
            class="w-32 ml-auto mt-4"
          />
        </div>

      </div>
    </div>

    <div class="px-8 mt-16 lg:mt-0">
      <div class="flex items-center justify-center gap-2 mb-8">
        <Icon icon="mdi:send-outline" class="text-3xl text-[#FF5858]" />
        <h2 class="text-[#FF5858] font-bold text-3xl">
          CONTATO
        </h2>
      </div>

      <form
        class="max-w-md mx-auto space-y-4"
        @submit.prevent="enviarWhatsApp"
      >
        <input
          type="text"
          v-model="nome"
          placeholder="Nome"
          class="w-full rounded-xl border border-gray-200 p-3 focus:outline-none focus:border-[#FF5858]"
        />

        <input
          type="email"
          v-model="email"
          placeholder="Email"
          class="w-full rounded-xl border border-gray-200 p-3 focus:outline-none focus:border-[#FF5858]"
        />

        <textarea
          v-model="mensagem"
          placeholder="Mensagem"
          class="w-full h-40 rounded-xl border border-gray-200 p-3 resize-none focus:outline-none focus:border-[#FF5858]"
        ></textarea>

        <button
          type="submit"
          class="w-full bg-[#FF5858] text-white font-bold py-4 rounded-xl hover:bg-red-500 transition-all duration-300"
        >
          <div class="flex items-center justify-center gap-2">
            <span>Enviar mensagem</span>
            <Icon icon="mdi:send-outline" />
          </div>
        </button>
      </form>
    </div>

  </div>
</section>
  </div>
</template>
