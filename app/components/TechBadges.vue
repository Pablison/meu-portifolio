<script setup>
const tecnologias = [
    'NUXT.JS',
    'VUE.JS',
    'TAILWIND',
    'LARAVEL',
    'DOCKER',
    'TYPESCRIPT'
]
</script>

<template>
    <div class="flex flex-wrap justify-center gap-4 mb-12 w-full max-w-2xl">

        <div v-for="(tech, index) in tecnologias" :key="index"
            class="flex items-center gap-2 bg-[#0f1115] border border-gray-800 px-3 py-1.5 rounded-sm hover:border-green-500/50 transition-colors cursor-default">
            <span class="w-1.5 h-1.5 bg-gray-500"></span>

            <span class="text-green-500 text-[10px] font-mono font-bold tracking-widest">
                {{ tech }}
            </span>
        </div>

    </div>
</template>