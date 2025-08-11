<template>
    <div class="w-full">
        <div class="w-full bg-contain bg-center bg-repeat h-auto  overflow-hidden" :key="currentIndex"
            :style="{ backgroundImage: `url(${images[currentIndex]})` }">

            <!-- Couche sombre + contenu -->
            <div
                class=" inset-0 w-full py-8 lg:py-12 flex items-center justify-center h-full bg-gradient-to-b from-black/80 to-[#0E2F51]/50 bg-[#0E2F51]/60">
                <div class="w-full lg:w-5/6 h-auto space-y-4 px-4">
                    <h1 data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-2xl sm:text-4xl xl:text-6xl text-white font-extrabold text-center  font-poppins">TÉMOIGNAGES
                    </h1>
                    <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-right" class="w-5/6 md:w-3/6 h-[1px] bg-red-600"></div>
                    <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-center text-gray-400 font-poppins">Ce que pensent les membres de la Formation FBWA
                    </p>
                    <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="zoom-in" class="text-center text-gray-400 font-poppins text-sm md:text-lg">Cliquez sur le bouton <strong
                            class="uppercase text-white font-bold "> Rejoindre la formation</strong></p>
                    <div class="w-full flex justify-center">
                        <a data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="zoom-in" href="https://wa.me/+237695863845"
                            class="bg-gradient-to-b to-black/60 from-[#E30065] font-poppins text-white font-bold py-2 px-4 rounded-tl-2xl rounded-br-2xl"
                            target="_blank" rel="noopener noreferrer">
                            Rejoindre la formation
                        </a>
                    </div>
                </div>


            </div>


        </div>
        <div class="w-full bg-black/80">
            <div class="w-full lg:w-5/6 lg:mx-auto flex flex-col justify-center items-center space-y-2 pt-4 lg:pt-8">
                <h1 class="text-sm sm:text-2xl md:text-2xl text-white font-poppins font-extrabold uppercase">La
                    promotion actuelle finit
                    dans
                </h1>
                <div class=" flex flex-wrap justify-center items-center gap-2 sm:gap-4 font-bold text-white">
                    <div v-for="(value, label) in countdown" :key="label"
                        class="text-center bg-blue-700/30  rounded-br-2xl rounded-tl-2xl space-y-2 px-4 py-4">
                        <div
                            class="text-lg sm:text-xl lg:text-2xl bg-blue-800/20 rounded-br-2xl rounded-tl-2xl px-2 py-6">
                            {{ value }}
                        </div>
                        <div class="text-sm lg:text-lg uppercase tracking-wide">{{ label }}</div>
                    </div>
                </div>
            </div>

            <!-- Galerie d'images -->
            <div class="grid grid-cols-2 md:grid-cols-4 py-4 lg:p-6 gap-2">
                <img v-for="(imag, index) in image" :key="index" :src="imag" data-aos="zoom-in" data-aos-delay="200"
                    data-aos-duration="1000" data-aos-easing="ease-in-out"
                    class="w-full h-80 object-cover cursor-pointer hover:opacity-80 transition"
                    @click="openModal(index)" />
            </div>

            <!-- Modale -->
            <div v-if="isModalOpen" class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-90">
                <!-- Numérotation -->
                <div class="absolute top-4 left-6 text-white text-lg font-bold">
                    {{ recentIndex + 1 }} / {{ image.length }}
                </div>

                <!-- Bouton fermer -->
                <button class="absolute top-4 right-6 text-white text-3xl font-bold hover:text-gray-400"
                    @click="closeModal">
                    ✕
                </button>

                <!-- Flèche gauche -->
                <button class="absolute left-4 text-white text-4xl p-2 hover:bg-white/20 rounded-full" @click="prev">
                    ‹
                </button>

                <!-- Image affichée -->
                <transition name="fade" mode="out-in">
                    <img :key="recentIndex" :src="currentImage"
                        class="max-h-[80vh] w-3/6 mx-auto object-cover  shadow-lg" />
                </transition>

                <!-- Flèche droite -->
                <button class="absolute right-4 text-white text-4xl p-2 hover:bg-white/20 rounded-full" @click="next">
                    ›
                </button>
            </div>

        </div>
        <Footer />
    </div>
</template>

<script>
import img from '@/assets/images/picture1.jpeg';
import img1 from '@/assets/images/picture2.jpeg';
import img2 from '@/assets/images/picture3.jpeg';
import Footer from './FooterView.vue';

export default {
    data() {
        return {
            image: [
                "https://img.freepik.com/free-photo/mystery-vanishing-forest-path-ahead-generated-by-ai_188544-26803.jpg?semt=ais_hybrid&w=740&q=80",
                "https://st2.depositphotos.com/2435561/5260/i/450/depositphotos_52600329-stock-photo-skyline-drive-in-a-heavily.jpg",
                "https://media.istockphoto.com/id/939185044/photo/magic-forest-path.jpg?s=612x612&w=0&k=20&c=Y4oUwr1VNED84I3pgolhIlZoJMcGdq1Az1VZ7SNjg-g=",
                "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRLK9l5v8IJzh9qg2FPyVj5B0R6pc37X3WorK371cJGFJJdftNG85FSFSmquIMaz0ysR3w&usqp=CAU",
                "https://st2.depositphotos.com/1005518/7129/i/450/depositphotos_71299897-stock-photo-bus-traveling-through-a-road.jpg",
                "https://static.vecteezy.com/system/resources/thumbnails/049/396/887/small_2x/endless-road-of-travel-on-rural-highways-there-are-natural-trees-on-both-sides-of-the-road-photo.jpeg",
            ],
            recentIndex: 0,
            isModalOpen: false,
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
        Footer
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
        },
        openModal(index) {
            this.recentIndex = index;
            this.isModalOpen = true;
            document.body.style.overflow = "hidden"; // désactive le scroll en arrière-plan
        },
        closeModal() {
            this.isModalOpen = false;
            document.body.style.overflow = "";
        },

        next() {
            this.recentIndex =
                (this.recentIndex + 1) % this.images.length;
        },
        prev() {
            this.recentIndex =
                (this.recentIndex - 1 + this.images.length) %
                this.images.length;
        },
    },
    computed: {
        currentImage() {
            return this.images[this.recentIndex];
        },
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
        const diff = this.targetDate - now;

        if (diff <= 0) {
            clearInterval(this.timer);
            this.countdown = {
                JOURS: "0",
                HEURES: "00",
                MINUTES: "00",
                SECONDES: "00",
            }
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
