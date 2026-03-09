<script setup>
import projetos from '../projetos.json' 
</script>

<template>

  <div class="min-h-screen bg-[#0a0a0f] text-gray-300 font-mono flex flex-col scroll-smooth">

    <TheHeader />

    <main class="flex-1 flex flex-col items-center pt-10 px-4 w-full max-w-4xl mx-auto">
      <HeroProfile />
      <HeroGreeting />
      <TechBadges />

      <ActionButtons />

      <ProjectList :projetos="projetos" />

    </main>

    <TheFooter />

  </div>
</template>