<template>
    <div>
        <div class="w-full " id="container" :key="currentIndex"
            :style="{ backgroundImage: `url(${images[currentIndex]})` }">
            <div class="w-full bg-black/80 space-y-8 py-8 xl:py-12 h-full">
                <div class="w-full md:w-5/6 mx-auto space-y-4 lg:space-y-8">
                    <h1 data-aos="zoom-in"
                        class="uppercase text-2xl lg:text-4xl xl:text-5xl text-white text-center font-poppins font-extrabold">
                        Qui suis-je ?</h1>
                    <div data-aos="fade-up" data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" class="w-5/6 lg:w-3/6 h-[1px] bg-red-600"></div>
                </div>
                <div class="w-full lg:w-5/6 mx-auto pt-8 lg:pt-12 xl:pt-20">
                    <p class="text-lg lg:text-2xl uppercase text-white font-bold font-poppins text-center"> Je suis <span class="text-red-600">{{ displayedText }}</span><span v-if="showCursor">|</span>
                        dans mes actions</p>
                </div>
                <div class="w-full px-4 md:px-0 lg:w-5/6 xl:w-4/6 mx-auto sm:pt-8 lg:pt-12 xl:pt-20 space-y-4">
                    <p data-aos="fade-up" data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" class="text-white md:text-center font-poppins">Je suis <strong class="uppercase">coach
                            Dimi</strong>, fondateur du programme
                        <strong class=" uppercase">DIMfitness</strong>. Ma mission est simple: <strong>aider les
                            femmes à retrouver confiance, énergie et forme</strong>, même après des grossesses, des
                        années
                        d’inactivité ou des échecs avec d’autres méthodes.
                    </p>
                    <p data-aos="fade-up" data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" class="text-white md:text-center font-poppins">Depuis plusieurs années, j’accompagne des femmes de
                        différents pays d’Afrique (Cameroun, Côte d’Ivoire, Gabon, RD Congo…) à <strong> perdre du poids
                            durablement</strong>, à se sentir belles dans leur corps et à reprendre le contrôle de leur
                        santé <strong> sans
                            régime extrême ni salle de sport.</strong>

                    </p>
                    <p data-aos="fade-up" data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" class="md:text-center text-white font-poppins">
                        Avec mon équipe, nous avons conçu un programme <strong>100% en
                            ligne</strong>, basé sur une méthode simple, humaine et efficace, qui tient compte de
                        <strong>votre réalité</strong>, <strong>vos emplois du temps et vos habitudes</strong>.

                    </p>
                    <p data-aos="fade-up" data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" class="md:text-center text-white font-poppins">Rejoindre <strong
                            class="text-red-600 uppercase">DIMfitness</strong>, ce n’est pas juste s’entraîner…
                        C’est rejoindre <strong> une famille où vous serez soutenue, écouté, encouragé peu importe
                        d’où vous partez.</strong></p>
                    <div class="w-full py-4 lg:py-8 flex flex-col space-y-4 items-center justify-center">
                        <p data-aos="fade-up" data-aos-delay="200" data-aos-duration="1000"
                            class="text-gray-400 text-sm font-poppins">Cliquez sur le bouton <span
                                class="uppercase text-sm lg:text-lg font-semibold text-white">Rejoindre la
                                formation</span></p>
                        <div class="flex justify-center mt-8">
                            <a data-aos="fade-up" data-aos-delay="200" data-aos-duration="1000"
                                href="https://wa.me/+237695863845"
                                class="bg-gradient-to-b to-black/60 from-red-600 font-poppins text-white font-bold py-2 px-4 rounded-tl-2xl rounded-br-2xl"
                                target="_blank" rel="noopener noreferrer">
                                Rejoindre la formation
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="w-full h-screen py-8 bg-black">
            <div class="w-full lg:w-5/6 mx-auto space-y-4">
                <h2 data-aos="fade-up" data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000"
                    class="text-lg text-center sm:text-xl md:text-2xl xl:text-3xl font-poppins uppercase font-extrabold text-white">
                    Adresse Local</h2>
                <div data-aos="fade-up" data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" class="w-5/6 lg:w-3/6 h-[1px] bg-red-600"></div>
                <div class="w-5/6 lg:w-3/6 mx-auto">
                    <p data-aos="fade-up" data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" class="text-center text-white font-poppins">Coach Dimi, nyalla Douala, Cameroun
                        Immeuble carrelé Noir Gris.
                        En face ENTRELEC dernière la station MRS</p>
                        <div class="flex space-x-4 justify-center py-4">
                            <div class="w-12 h-12 rounded-full flex items-center justify-center">
                                <a href="" class="text-white text-2xl">
                                    <i class="fab fa-facebook"></i>
                                </a>
                            </div>
                            <div class="w-12 h-12 rounded-full flex items-center justify-center">
                                <a href="" class="text-white text-2xl">
                                    <i class="fab fa-whatsapp"></i>
                                </a>
                            </div>
                             <div class="w-12 h-12 rounded-full flex items-center justify-center">
                                <a href="" class="text-white text-2xl">
                                    <i class="fab fa-tiktok"></i>
                                </a>
                            </div>
                        </div>
                </div>
            </div>
            <div class="overflow-hidden w-full h-[340px] lg:h-[400px]">
                <iframe
                     class="w-full h-full"
                    src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d15957.013300691116!2d9.7288192!3d4.0534016!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNMKwMzQyJzUwLjAiTiA5wrAwNTAyJzIxLjAiVw!5e0!3m2!1sfr!2s!4v1652187227168!5m2!1sfr!2s"
                    width="0" height="0" style="border:0;" allowfullscreen="" loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade">
                </iframe>
            </div>
            <div class="w-full h-44"></div>

        </div>
        <FooterView />
    </div>
</template>

<script>
import img from '@/assets/images/dim.jpg';
import img1 from '@/assets/images/dim1.jpg';
import img2 from '@/assets/images/coach-4.jpg';
import FooterView from './FooterView.vue';
export default {
    data() {
        return {
            texts: [
                'génereux',
                'passionné ',
                'déterminé',
                'motivé',
                'audacieux',
            ],
            showCursor: true,
            displayedText: '',
            textIndex: 0,
            charIndex: 0,
            isDeleting: false,
            typeSpeed: 100,
            deleteSpeed: 50,
            pauseDelay: 1000,
            currentIndex: 0,
            images: [img, img1, img2],
            autoPlayInterval: null,
            displayDuration: 7000, // transition toutes les 7s
        };
    },
    components: {
        FooterView,
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
        this.startAutoPlay();
        this.typeWriterLoop();
        setInterval(() => {
            this.showCursor = !this.showCursor;
        }, 500);
    },
    beforeUnmount() {
        this.stopAutoPlay();
    },
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

#container {
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}
</style>
