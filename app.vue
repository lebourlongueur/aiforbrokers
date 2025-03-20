<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-[#FEF3DD] text-[#3F5072]">
    <header class="text-center mb-8">
      <h1 class="text-4xl font-bold" style="font-family: Inter, sans-serif; color: #003092;">Mon Prototype</h1>
      <p class="text-lg italic" style="font-family: 'Libre Baskerville', serif;">Découvrez mon projet interactif</p>
    </header>
    
    <iframe
      :src="figmaEmbedUrl"
      class="w-full max-w-4xl h-[600px] border rounded-lg shadow-lg"
      allowfullscreen>
    </iframe>
  </div>
</template>

<script setup>
const figmaEmbedUrl = 'https://www.figma.com/embed?embed_host=nuxt&url=TON_URL_FIGMA';
</script>

<style>
body {
  font-family: Inter, sans-serif;
}
</style>
