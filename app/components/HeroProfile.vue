<template>
  <div class="flex flex-col items-center mt-2 mb-8">
    
    <div class="relative">
      <div class="rounded-full p-[2px] bg-gradient-to-r from-green-500 via-gray-600 to-purple-500">
        <img 
          src="/1.png" 
          alt="Foto de Perfil" 
          class="w-48 h-48 md:w-56 md:h-56 rounded-full border-4 border-[#0a0a0f] object-cover"
        />
      </div>
      
      <div class="absolute -bottom-3 left-1/2 transform -translate-x-1/2 bg-[#121212] border border-gray-700 text-green-500 text-[10px] font-bold px-3 py-1 rounded-full tracking-widest whitespace-nowrap shadow-lg">
        MID_DEVELOPER
      </div>
    </div>

    <div class="mt-10 flex flex-col items-center gap-4 text-xs font-mono font-bold">
      <div class="flex items-center gap-2 bg-[#0f1115] border border-gray-800 px-4 py-1.5 rounded-full">
        <span class="w-2 h-2 rounded-full bg-green-500 animate-pulse"></span>
        <span class="text-green-500 text-[10px] tracking-widest">PROTOCOL_ACTIVE: DISPONÍVEL PARA NOVOS PROJETOS</span>
      </div>
    </div>

  </div>
</template>