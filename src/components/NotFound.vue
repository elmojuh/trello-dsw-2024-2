<template>
  <div>
    <div class="grid h-screen bg-white background">
      <div
        class="place-self-center"
        data-cy="404"
      >
        <span class="block mb-4 text-8xl font-bold text-center text-gray-200">404</span>
        <p class="block mb-4 text-center text-gray-400">
          Descukpe, este quadro não existe
        </p>
        <router-link
          to="/"
          class="block font-semibold text-center text-blue7"
        >
          Voltar para a página inicial
        </router-link>
      </div>
    </div>
  </div>
</template>
