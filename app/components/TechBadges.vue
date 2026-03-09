<script setup>
const tecnologias = [
    { nome: 'PHP', icone: 'simple-icons:php' },
    { nome: 'LARAVEL', icone: 'simple-icons:laravel' },
    { nome: 'REACT.JS', icone: 'simple-icons:react' },
    { nome: 'NEXT.JS', icone: 'simple-icons:nextdotjs'},
    { nome: 'NUXT.JS', icone: 'simple-icons:nuxtdotjs' },
    { nome: 'VUE.JS', icone: 'simple-icons:vuedotjs' },
    { nome: 'DOCKER', icone: 'simple-icons:docker' },
    { nome: 'API REST', icone: 'simple-icons:restapi'},
    { nome: 'GIT', icone: 'simple-icons:git' },
    { nome: 'ADVPL', icone: 'simple-icons:protheus'},
    { nome: 'PROTHEUS', icone: 'simple-icons:protheus'},
    { nome: 'TYPESCRIPT', icone: 'simple-icons:typescript' }
]
</script>

<template>
    <div class="flex flex-wrap justify-center gap-4 mb-12 w-full max-w-2xl">

        <div v-for="(tech, index) in tecnologias" :key="index"
            class="flex items-center gap-2 bg-[#0f1115] border border-gray-800 px-3 py-1.5 rounded-sm hover:border-green-500/50 transition-colors cursor-default group">
            <Icon :name="tech.icone" class="w-3.5 h-3.5 text-gray-500 group-hover:text-green-500 transition-colors" />

            <span class="text-green-500 text-[10px] font-mono font-bold tracking-widest">
                {{ tech.nome }}
            </span>
        </div>

    </div>
</template>