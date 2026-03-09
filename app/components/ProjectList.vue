<script setup>
defineProps({
    projetos: {
        type: Array,
        required: true
    }
})
</script>

<template>
    <div id="lista-projetos" class="w-full max-w-4xl mt-16 mb-24">

        <div class="flex items-center gap-4 mb-8">
            <span class="text-green-500 font-bold">></span>
            <h2 class="text-xl md:text-2xl font-bold text-white tracking-widest uppercase">
                Projetos_Desenvolvidos
            </h2>
            <div class="flex-1 h-px bg-gray-800 ml-4"></div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

            <div v-for="projeto in projetos" :key="projeto.id"
                class="bg-[#0f1115] border border-gray-800 rounded-xl p-6 hover:border-green-500/50 transition-all duration-300 group flex flex-col shadow-lg">
                <h3 class="text-lg md:text-xl font-bold text-white mb-3 group-hover:text-green-400 transition-colors">
                    {{ projeto.titulo }}
                </h3>

                <p class="text-gray-400 text-sm mb-6 flex-1 leading-relaxed">
                    {{ projeto.descricao }}
                </p>

                <div class="flex flex-wrap gap-2 mt-auto pt-4 border-t border-gray-800/50">
                    <span v-for="(tecnologia, index) in projeto.tecnologias" :key="index"
                        class="text-[10px] font-mono text-gray-400 border border-gray-700 bg-[#12141a] px-2 py-1 rounded">
                        {{ tecnologia }}
                    </span>
                </div>

            </div>

        </div>
    </div>
</template>