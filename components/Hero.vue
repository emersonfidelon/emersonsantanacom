<script setup>
import { Linkedin, Instagram, Mail } from 'lucide-vue-next'
</script>

<template>
  <div class="inline-flex justify-center itens-center bg-transparent h-full w-full absolute shadow-sm text-white z-10">
    <div class="container inline-flex flex-col-reverse md:flex-row md:gap-20 gap-10 w-3/4 h-full py-10">
      <div class="inline-flex flex-col justify-center md:my-0 max-w-3xl">
        <h4 class="my-name font-[Kalam] text-4xl md:text-6xl">Emerson Santana</h4>
        <span class=" text-neutral-100 text-sm mb-5 md:text-2xl font-medium font-['Heebo'] leading-loose">
          Desenvolvedor FullStack a +13 anos | CTO
        </span>
        <p class=" text-neutral-400 text-base font-normal font-['Heebo'] leading-normal">
          Atuo como desenvolvedor full-stack a mais de 13 anos, com experiência em diversas tecnologias, linguagens e projetos como Sites, Apps iOS, Apps Android, Sistemas Web, DevOps, Testes Automatizados, Gestão de times ágeis, Gestão de projetos, Big Data, Marketing Digital, UX, UI.
        </p>
        <p class="inline-flex justify-start items-center mt-3">
          <Mail class="w-4 h-4 mr-2" />
          <a href="mailto:contato@emersonsantana.com">
            contato@emersonsantana.com
          </a>
        </p>
        <div class="flex space-x-4 mt-5">
          <a href="https://linkedin.com/in/emerson-as" target="_blank" title="LilnkedIn Emerson Santana" class="h-14 px-6 py-4 bg-gray-600 hover:bg-gray-700 rounded-lg justify-center items-center gap-2 inline-flex">
            <Linkedin class="w-6 h-6" /> 
          </a>

          <a href="https://instagram.com/oemersantana" target="_blank" title="Instagram Emerson Santana" class="h-14 px-6 py-6 bg-purple-800 hover:bg-purple-900 rounded-lg justify-center items-center gap-2 inline-flex">
            <Instagram class="w-6 h-6" />
          </a>

        </div>
      </div>
      <div class="inline-flex justify-center items-center md:justify-end w-full">
        <img 
          src="https://avatars.githubusercontent.com/emersonfidelon" 
          alt="Emerson Santana" class="rounded-3xl w-full sm:w-[90%] md:w-80" 
        />
      </div>
    </div>
  </div>
  <div class="area bg-[#171023]">
    <div class="glowing">
      <span style="--i:1;"></span>
      <span style="--i:2;"></span>
      <span style="--i:3;"></span>
    </div>
    
    <div class="glowing">
      <span style="--i:1;"></span>
      <span style="--i:2;"></span>
      <span style="--i:3;"></span>
    </div>
    
    <div class="glowing">
      <span style="--i:1;"></span>
      <span style="--i:2;"></span>
      <span style="--i:3;"></span>
    </div>
    
    <div class="glowing">
      <span style="--i:1;"></span>
      <span style="--i:2;"></span>
      <span style="--i:3;"></span>
    </div>
  </div>
</template>

<style scoped>
.area {
  overflow: hidden;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
}
.my-name {
  background: linear-gradient(90deg, #9955E8 0%, #7BFFAF 100%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

  .glowing {
    position: relative;
    min-width: 700px;
    height: 100%;
    margin: -150px;
    transform-origin: right;
    animation: colorChange 5s linear infinite;
  }

  .glowing:nth-child(even) {
    transform-origin: left;
  }

  @keyframes colorChange {
    0% {
      filter: hue-rotate(0deg);
      transform: rotate(0deg);
    }
    100% {
      filter: hue-rotate(360deg);
      transform: rotate(360deg);
    }
  }

  .glowing span {
    position: absolute;
    top: calc(80px * var(--i));
    left: calc(80px * var(--i));
    bottom: calc(80px * var(--i));
    right: calc(80px * var(--i));
  }

  .glowing span::before {
    content: "";
    position: absolute;
    top: 50%;
    left: -8px;
    width: 15px;
    height: 15px;
    background: #9955E8;
    border-radius: 50%;
  }

  .glowing span:nth-child(3n + 1)::before {
    background: rgb(82, 202, 49);
    box-shadow: 0 0 20px rgba(134,255,0,1),
      0 0 40px rgba(134,255,0,1),
      0 0 60px rgba(134,255,0,1),
      0 0 80px rgba(134,255,0,1),
      0 0 0 8px rgba(134,255,0,.1);
  }

  .glowing span:nth-child(3n + 2)::before {
    background: rgba(255,214,0,1);
    box-shadow: 0 0 20px rgba(255,214,0,1),
      0 0 40px rgba(255,214,0,1),
      0 0 60px rgba(255,214,0,1),
      0 0 80px rgba(255,214,0,1),
      0 0 0 8px rgba(255,214,0,.1);
  }

  .glowing span:nth-child(3n + 3)::before {
    background: rgb(0, 238, 255);
    box-shadow: 0 0 20px rgba(0,226,255,1),
      0 0 40px rgba(0,226,255,1),
      0 0 60px rgba(0,226,255,1),
      0 0 80px rgba(0,226,255,1),
      0 0 0 8px rgba(0,226,255,.1);
  }

  .glowing span:nth-child(3n + 1) {
    animation: animate 10s alternate infinite;
  }

  .glowing span:nth-child(3n + 2) {
    animation: animate-reverse 3s alternate infinite;
  }

  .glowing span:nth-child(3n + 3) {
    animation: animate 8s alternate infinite; 
  }

  @keyframes animate {
    0% {
      transform: rotate(180deg);
    }
    50% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }

  @keyframes animate-reverse {
    0% {
      transform: rotate(360deg);
    }
    
    50% {
      transform: rotate(180deg);
    }
    
    100% {
      transform: rotate(0deg);
    }
  }



@keyframes animate {

0%{
    transform: translateY(0) rotate(0deg);
    opacity: 1;
    border-radius: 0;
}

100%{
    transform: translateY(-1000px) rotate(720deg);
    opacity: 0;
    border-radius: 50%;
}

}
</style>