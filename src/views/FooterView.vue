<template>
    <div>
        <div class="bg-black text-white py-8">
            <div class="container mx-auto px-4">
                <div class="grid grid-cols-1 md:grid-cols-3 xl:grid-cols-4 gap-8 font-poppins">
                    <div
                        class="space-y-4 font-poppins text-white flex flex-col items-center md:ite justify-center md:justify-normal">
                        <img src="/images/logo.png" width="200" height="200" alt="">
                    </div>
                    <div
                        class="space-y-4 font-poppins text-white flex flex-col items-center md:items-start justify-center md:justify-normal">
                        <h2 class="text-xl font-bold mb-4">ADRESSE</h2>
                        <p>CAMEROUN :</p>
                        <p>DOUALA, BALI EN FACE ENTRELAC</p>
                        <p>APPEL OU WHATSAPP :</p>
                        <p>(+237)674491694/695368645</p>
                        <p>Email: <a href="mailto:dimitridanmen65@gmail.com"
                                class="underline">dimitridanmen65@gmail.com</a></p>

                    </div>
                    <div
                        class="space-y-4 font-poppins text-white flex flex-col items-center md:items-start justify-center md:justify-normal">
                        <h2 class="text-xl font-bold uppercase">Nos Liens</h2>
                        <router-link to="/" class="text-base font-semibold hover:text-red-700">Formation
                            FBWA</router-link>
                        <router-link to="/plans-fbwa" class="text-base font-semibold hover:text-red-700">PLAN
                            FBWA</router-link>
                        <router-link to="/" class="text-base font-semibold hover:text-red-700">témoignages</router-link>
                        <router-link to="/" class="text-base font-semibold hover:text-red-700">les modules</router-link>
                        <router-link to="/" class="text-base font-semibold hover:text-red-700">contact</router-link>
                        <router-link to="/" class="text-base font-semibold hover:text-red-700">Qui suis-je</router-link>
                    </div>
                    <div
                        class="space-y-4 font-poppins text-white flex flex-col items-center md:items-start justify-center md:justify-normal">
                        <h2 class="text-xl font-bold uppercase">Nos Reseaux</h2>
                        <a href="https://www.facebook.com/Dimfitness" target="_blank" rel="noopener noreferrer"> <i
                                class="fab fa-facebook"></i> Dimfitness</a>
                        <router-link to="/plans-fbwa" class="text-base font-semibold"><i class="fab fa-whatsapp"></i>
                            +(237)674491694/695368645</router-link>
                        <p><i class="fab fa-tiktok"></i> TikTok: <a href="https://www.tiktok.com/Dim_fitness"
                                target="_blank" rel="noopener noreferrer" class="">Dim_fitness</a></p>
                        <p><i class="fab fa-facebook"></i> Facebook: <a href="https://www.facebook.com/Dimfitness"
                                target="_blank" rel="noopener noreferrer" class="">Dimfitness</a></p>
                        <p><i class="fab fa-youtube"></i> YouTube: <a href="https://www.youtube.com/@jeanhouafo3352"
                                target="_blank" rel="noopener noreferrer" class="">Dimfitness</a></p>
                        <p><i class="fab fa-instagram"></i> Instagram: <a href="https://www.instagram.com/dimfitness"
                                target="_blank" rel="noopener noreferrer" class="">dimfitness</a></p>
                    </div>
                </div>
                <div class="text-center mt-8">
                    <p class="text-sm">&copy; {{ new Date().getFullYear() }} Coach Dimitri. Tous droits réservés.</p>
                </div>
            </div>
        </div>
        <div class="relative">
            <!-- Contenu très long pour pouvoir scroller -->
            <!-- Bouton scroll-to-top -->
            <button v-show="showButton" @click="scrollToTop"
                class="fixed bottom-6 right-6 transition duration-300">
                <img src="../assets/images/icons8-rocket-96.png" alt="animée" class="w-12 h-12 animate-bounce rounded-full ">
            </button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppFooter', // Nom du composant modifié
    data() {
        return {
            newYear: new Date().getFullYear(),
            showButton: false
        };
    },
    beforeUnmount() {
        window.removeEventListener('scroll', this.checkScroll);
    },
    methods: {
        scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        },
        checkScroll() {
            this.showButton = window.scrollY > 200;
        }
    },
    mounted() {
        window.addEventListener('scroll', this.checkScroll);
    }
};
</script>

<style>
/* Ajoutez ici des styles personnalisés si nécessaire */
</style>
