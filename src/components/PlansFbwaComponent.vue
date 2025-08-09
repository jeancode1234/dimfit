<template>
    <div class="w-full">
            <!-- Couche sombre + contenu -->
                <div
                    class="w-full font-poppins flex flex-col items-center justify-center  space-y-4">
                   
                    <div class="w-5/6 flex flex-col justify-center items-center space-y-4 ">
                        <h1 class="text-6xl text-white font-poppins font-extrabold uppercase">PRIX FORMATION FBWA</h1>
                        <h2 class="text-3xl text-white font-poppins font-bold uppercase">
                            La promotion actuelle finit
                            dans
                        </h2>
                        <div class=" flex justify-center items-center gap-4 font-bold text-white">
                            <div v-for="(value, label) in countdown" :key="label"
                                class="text-center bg-blue-700/30  rounded-br-2xl rounded-tl-2xl space-y-2 px-4 py-4">
                                <div class="text-xl bg-blue-800/20 rounded-br-2xl rounded-tl-2xl px-2 py-6">{{ value }}
                                </div>
                                <div class="text-sm uppercase tracking-wide">{{ label }}</div>
                            </div>
                        </div>
                        <p class="text-lg text-white font-poppins font-bold text-center">Dépêchez-vous !</p>
                    </div>
    
                     <p class="text-gray-300 text-lg text-center">
                       Suite aux différentes plaintes relatives à la classe sociale, la priorité d’assistance et l’exigence de certains membres, mon équipe et moi avons décidé de mettre en place 03 plans pour vous satisfaire au maximum selon votre classe sociale.
                    </p>
                 <h3 class="text-2xl font-bold text-white text-center font-poppins">Veuillez s'il vous plaît sélectionner votre plan</h3>

                </div>
           
    </div>
</template>
<script>
import img from '@/assets/images/picture1.jpeg';
import img1 from '@/assets/images/picture2.jpeg';
import img2 from '@/assets/images/picture3.jpeg';


export default {
    data() {
        return {
            countdown: {
                JOURS: "0",
                HEURES: "00",
                MINUTES: "00",
                SECONDES: "00",
            },
            targetDate: new Date("2025-08-10T23:59:59"), // 🎯 date de fin de la promo
            timer: null,
            currentIndex: 0,
            images: [img, img1, img2],
            autoPlayInterval: null,
            displayDuration: 7000, // transition toutes les 7s
        };
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
