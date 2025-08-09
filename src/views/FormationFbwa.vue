<template>
    <div class="">
        <div class="space-y-8 p-8 bg-[#0E2F51]">

            <h1 class="text-center text-5xl font-bold font-poppins uppercase text-white">Formation FBWA</h1>
            <p class="text-2xl uppercase text-white font-semibold font-poppins text-center"> mes stratégies sont <span
                    class="text-[#E02454]">{{ displayedText }}</span><span v-if="showCursor">|</span></p>
            <div class="w-full md:w-3/6 bg-[#E30065] h-[1px]"></div>
        </div>
        <div class="w-full px-4 h-[86vh] bg-[#0E2F51]">
            <div class="w-full overflow-hidden h-full rounded-3xl">

                <iframe class="w-full h-full rounded-3xl"
                    src="https://www.youtube.com/embed/NyxyB-FiQ2Y" frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen></iframe>
            </div>
        </div>
        <div class="w-full py-8 bg-black flex flex-col space-y-4 items-center justify-center">
            <p class="text-gray-400 text-sm font-poppins">Cliquez sur le bouton <span
                    class="uppercase text-lg font-semibold text-white">Rejoindre la formation</span></p>
            <div class="flex justify-center mt-8">
                <a href="https://wa.me/+237695863845"
                    class="bg-gradient-to-b to-black/60 from-[#E30065] font-poppins text-white font-bold py-2 px-4 rounded-tl-2xl rounded-br-2xl"
                    target="_blank"
                    rel="noopener noreferrer"
                    >
                    Rejoindre la formation
                </a>
            </div>
        </div>
        <DiaporamaComponent/>
        <DiapoComponent/>
        <PromoComponent/>
        <Module/>
        <TestifyComponent/>
    
    </div>
</template>

<script>
import DiaporamaComponent from '@/components/DiaporamaComponent.vue';
import DiapoComponent from '@/components/DiapoComponent.vue';
import PromoComponent from '@/components/PromoComponent.vue';
import Module from '@/components/ModuleComponent.vue'
import TestifyComponent from '@/components/TestifyComponent.vue';
export default {
    data() {
        return {
            texts: [
                'incroyables',
                'impressionantes ',
                'époustouflantes',
                'galvanisantes',
                'inimaginables',
            ],
            showCursor: true,
            displayedText: '',
            textIndex: 0,
            charIndex: 0,
            isDeleting: false,
            typeSpeed: 100,
            deleteSpeed: 50,
            pauseDelay: 1000,
        }
    },
    components:{
        DiaporamaComponent,
        DiapoComponent,
        PromoComponent,
        Module,
        TestifyComponent
    },
    methods: {
        typeWriterLoop() {
            if (this.textIndex < this.texts.length) {
                const currentText = this.texts[this.textIndex];
                if (this.charIndex < currentText.length) {
                    this.displayedText += currentText.charAt(this.charIndex);
                    this.charIndex++;
                    setTimeout(() => this.typeWriterLoop(), this.typeSpeed);
                } else {
                    setTimeout(() => {
                        this.isDeleting = true;
                        this.deleteText();
                    }, this.pauseDelay);
                }
            } else {
                this.textIndex = 0;
                this.charIndex = 0;
                this.displayedText = '';
                setTimeout(() => this.typeWriterLoop(), 2000);
            }
        },
        deleteText() {
            if (this.isDeleting) {
                if (this.charIndex > 0) {
                    this.displayedText = this.displayedText.slice(0, -1);
                    this.charIndex--;
                    setTimeout(() => this.deleteText(), this.deleteSpeed);
                } else {
                    this.isDeleting = false;
                    this.textIndex++;
                    setTimeout(() => this.typeWriterLoop(), 500);
                }
            }
        }
    },
    mounted() {
        this.typeWriterLoop();
        setInterval(() => {
            this.showCursor = !this.showCursor;
        }, 500);
    }
};
</script>

<style scoped>
.animate-pulse {
    animation: blink 1s infinite;
}

@keyframes blink {

    0%,
    100% {
        opacity: 1;
    }

    50% {
        opacity: 0;
    }
}
</style>
