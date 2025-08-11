<template>
    <div class="w-full">

        <div class="w-full  bg-cover bg-center  h-auto  overflow-hidden" :key="currentIndex"
            :style="{ backgroundImage: `url(${images[currentIndex]})` }">

            <!-- Couche sombre + contenu -->
            <div class=" inset-0 w-full h-full py-8 bg-gradient-to-t from-[#001224] to-[#001224]/60 bg-[#001224]/60">
                <div class="flex justify-end lg:px-8">
                    <div class="w-full sm:w-5/6 lg:w-3/6 h-[1px] bg-white"></div>
                </div>
                <div
                    class="w-full lg:w-3/6 mx-auto font-poppins flex flex-col items-center justify-center h-auto space-y-8 px-4 lg:px-0 py-6 lg:py-10">
                    <p data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-gray-300 text-sm sm:text-base lg:text-lg text-center">
                        Vous bénéficierez de 6 mois d’accompagnement 🤩 par mon équipe et moi 24h/24, 7j/7 en ligne sur
                        WhatsApp et 4 fois par semaine en présentiel ou en télé distanciel 💻 dans le but de répondre à
                        toutes vos préoccupations.
                    </p>
                    <div class="w-full lg:w-5/6 flex flex-col justify-center items-center space-y-2 pt-4 lg:pt-8">
                        <h1 data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-sm sm:text-2xl md:text-2xl text-white font-poppins font-extrabold uppercase">La
                            promotion actuelle finit
                            dans
                        </h1>
                        <div class=" flex flex-wrap justify-center items-center gap-2 sm:gap-4 font-bold text-white">
                            <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" v-for="(value, label) in countdown" :key="label"
                                class="text-center bg-blue-700/30  rounded-br-2xl rounded-tl-2xl space-y-2 px-4 py-4">
                                <div
                                    class="text-lg sm:text-xl lg:text-2xl bg-blue-800/20 rounded-br-2xl rounded-tl-2xl px-2 py-6">
                                    {{ value }}
                                </div>
                                <div class="text-sm lg:text-lg uppercase tracking-wide">{{ label }}</div>
                            </div>
                        </div>
                    </div>


                </div>
                <div class="w-full  flex flex-col py-4 space-y-4 items-center justify-center">
                    <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-gray-400 text-sm font-poppins">
                        Cliquez sur le bouton <span
                            class="uppercase text-sm sm:text-lg font-semibold text-white">Rejoindre la
                            formation</span>
                    </p>
                    <a data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" href="https://wa.me/+237695863845"
                        class="bg-gradient-to-b to-black/60 from-[#E30065] font-poppins text-white font-bold py-2 px-4 rounded-tl-2xl rounded-br-2xl"
                        target="_blank" rel="noopener noreferrer">
                        Rejoindre la formation
                    </a>
                    <div class="w-full px-4 lg:px-8 space-y-4">
                        <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="w-5/6 lg:w-3/6 h-[1px] bg-white"></div>
                        <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-center text-xs xs:text-sm sm:text-lg lg:text-xl text-white font-poppins">Ce que pensent les
                            membres de la Formation FBWA</p>
                    </div>
                </div>
            </div>

        </div>
        <div class="w-full bg-[#001224] py-4 lg:pt-4">
            <h1 data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-xl sm:text-2xl lg:text-3xl font-bold font-poppins text-white uppercase text-center">
                TÉMOIGNAGES incroyables</h1>
            <TestimonialComponent />
        </div>
    </div>
</template>
<script>
import img from '@/assets/images/picture1.jpeg';
import img1 from '@/assets/images/picture2.jpeg';
import img2 from '@/assets/images/picture3.jpeg';
import TestimonialComponent from '@/components/TestimonialComponent.vue';

export default {
    data() {
        return {
            countdown: {
                JOURS: "0",
                HEURES: "00",
                MINUTES: "00",
                SECONDES: "00",
            },
            targetDate: new Date("2025-08-13T23:59:59"), // 🎯 date de fin de la promo
            timer: null,
            currentIndex: 0,
            images: [img, img1, img2],
            autoPlayInterval: null,
            displayDuration: 7000, // transition toutes les 7s
        };
    },
    components: {
        TestimonialComponent
    },
    methods: {
        nextImage() {
            this.currentIndex = (this.currentIndex + 1) % this.images.length;
        },
        startAutoPlay() {
            this.autoPlayInterval = setInterval(this.nextImage, this.displayDuration);
        },
        stopAutoPlay() {
            clearInterval(this.autoPlayInterval);
        },
        updateCountdown() {
            const now = new Date();
            const diff = this.targetDate - now;

            if (diff <= 0) {
                clearInterval(this.timer);
                this.countdown = {
                    JOURS: "0",
                    HEURES: "00",
                    MINUTES: "00",
                    SECONDES: "00",
                };
                return; // n'oublie pas de sortir
            }

            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
            const minutes = Math.floor((diff / (1000 * 60)) % 60);
            const seconds = Math.floor((diff / 1000) % 60);

            this.countdown = {
                JOURS: days.toString(),
                HEURES: hours.toString().padStart(2, "0"),
                MINUTES: minutes.toString().padStart(2, "0"),
                SECONDES: seconds.toString().padStart(2, "0"),
            };
        }
    },
    mounted() {
        this.startAutoPlay();
        this.updateCountdown(); // initial
        this.timer = setInterval(this.updateCountdown, 1000);
    },
    beforeUnmount() {
        this.stopAutoPlay();
        clearInterval(this.timer);
    },
    updateCountdown() {
        const now = new Date();
        let diff = this.targetDate - now;

        // Si le temps est écoulé, on repart sur un nouveau cycle
        if (diff <= 0) {
            // ⏳ Nouveau cycle de 6 heures (exemple)
            this.targetDate = new Date(now.getTime() + 6 * 60 * 60 * 1000);
            diff = this.targetDate - now;
        }

        const days = Math.floor(diff / (1000 * 60 * 60 * 24));
        const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
        const minutes = Math.floor((diff / (1000 * 60)) % 60);
        const seconds = Math.floor((diff / 1000) % 60);

        this.countdown = {
            JOURS: days.toString(),
            HEURES: hours.toString().padStart(2, "0"),
            MINUTES: minutes.toString().padStart(2, "0"),
            SECONDES: seconds.toString().padStart(2, "0"),
        };
    }

};
</script>
<style scoped>
.fadezoom-enter-active,
.fadezoom-leave-active {
    transition: opacity 2s ease-in-out, transform 2s ease-in-out;
}

.fadezoom-enter-from,
.fadezoom-leave-to {
    opacity: 0;
    transform: scale(1.1);
}
</style>
