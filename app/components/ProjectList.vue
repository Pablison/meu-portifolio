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

        <div class="flex items-center gap-4 mb-10">
            <span class="text-green-500 font-bold"></span>
            <h2 class="text-xl md:text-2xl font-bold text-white tracking-widest uppercase">
                Projetos_Desenvolvidos
            </h2>
            <div class="flex-1 h-px bg-gray-800 ml-4"></div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">

            <div v-for="projeto in projetos" :key="projeto.id"
                class="bg-[#0f1115] border border-gray-800 rounded-2xl overflow-hidden hover:border-green-500/50 transition-all duration-300 group flex flex-col shadow-[0_0_20px_rgba(34,197,94,0.1)] hover:shadow-[0_0_30px_rgba(34,197,94,0.3)]">

                <div class="w-full h-48 overflow-hidden">
                    <img :src="projeto.imagem" :alt="'Preview do projeto ' + projeto.titulo"
                        class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500" />
                </div>

                <div class="p-6 flex flex-col flex-1">
                    <h3
                        class="text-lg md:text-xl font-bold text-white mb-3 group-hover:text-green-400 transition-colors uppercase">
                        {{ projeto.titulo }}
                    </h3>

                    <p class="text-gray-400 text-sm mb-6 flex-1 leading-relaxed">
                        {{ projeto.descricao }}
                    </p>

                    <div class="flex flex-wrap gap-2 pt-4 border-t border-gray-800/50">
                        <span v-for="(tecnologia, index) in projeto.tecnologias" :key="index"
                            class="text-[10px] font-mono text-gray-400 border border-gray-700 bg-[#12141a] px-2 py-1 rounded">
                            {{ tecnologia }}
                        </span>
                    </div>
                </div>

                <div class="grid grid-cols-2 gap-2 p-3 bg-[#12141a] border-t border-gray-800">

                    <a :href="projeto.url_vercel" target="_blank"
                        class="flex items-center justify-center gap-2.5 bg-green-500 hover:bg-green-400 text-[#050505] font-bold py-2.5 px-4 rounded-xl text-[10px] tracking-widest transition-all duration-300">
                        <Icon name="mdi:web" class="w-4 h-4" />
                        PREVIEW
                    </a>

                    <a :href="projeto.url_github" target="_blank"
                        class="flex items-center justify-center gap-2.5 bg-[#0a0a0f] hover:bg-[#1a1d24] border border-gray-700 hover:border-green-500 text-gray-300 hover:text-white font-bold py-2.5 px-4 rounded-xl text-[10px] tracking-widest transition-all duration-300">
                        <Icon name="simple-icons:github" class="w-4 h-4" />
                        GITHUB
                    </a>
                </div>

            </div>

        </div>
    </div>
</template>