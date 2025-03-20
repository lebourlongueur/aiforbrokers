<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-[#FEF3DD] text-[#3F5072] p-6">
    <header class="text-center mb-8 animate-fade-in">
      <h1 class="text-5xl font-bold" style="font-family: Inter, sans-serif; color: #003092;">Mon Prototype</h1>
      <p class="text-lg italic mt-2" style="font-family: 'Libre Baskerville', serif;">Découvrez mon projet interactif</p>
    </header>
    
    <div class="w-full flex justify-center">
      <ClientOnly>
        <iframe
          :src="figmaEmbedUrl"
          class="w-full max-w-md md:max-w-lg lg:max-w-xl h-[700px] md:h-[800px] lg:h-[900px] border rounded-xl shadow-xl transition-transform duration-300 hover:scale-105"
          allowfullscreen>
        </iframe>
      </ClientOnly>
    </div>
    
    <footer class="text-center mt-8 text-sm opacity-80">
      <p>© 2025 - Créé avec ❤️ et Nuxt</p>
    </footer>
  </div>
</template>

<script setup>
import { useHead } from '#imports';

const figmaEmbedUrl = 'https://embed.figma.com/proto/RUvuKWqfWyOfsKl41w3URn/Ai-For-Broker?page-id=0%3A1&node-id=2-581&viewport=-3006%2C120%2C0.53&scaling=scale-down&content-scaling=fixed&starting-point-node-id=2%3A644&embed-host=share';

useHead({
  title: 'Mon Prototype Figma',
  meta: [
    { name: 'description', content: 'Découvrez mon projet interactif Figma' },
    { property: 'og:image', content: 'URL_DU_VISUEL' }
  ]
});
</script>

<style>
body {
  font-family: Inter, sans-serif;
}

@keyframes fade-in {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-fade-in {
  animation: fade-in 1s ease-out;
}
</style>
