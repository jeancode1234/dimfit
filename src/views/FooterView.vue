<template>
    <div>
        <div class="bg-black text-white py-8">
            <div class="container mx-auto px-4">
                <div class="grid grid-cols-1 md:grid-cols-3 xl:grid-cols-4 gap-8 font-poppins">
                    <div class="space-y-4 font-poppins text-white flex flex-col items-center md:ite justify-center md:justify-normal">
                        <img src="/images/logo.png" width="200" height="200" alt="">
                    </div>
                    <div class="space-y-4 font-poppins text-white flex flex-col items-center md:ite justify-center md:justify-normal">
                        <h2 class="text-xl font-bold mb-4">ADRESSE</h2>
                        <p>CAMEROUN :</p>
                        <p>DOUALA, BALI EN FACE ENTRELAC</p>
                        <p>APPEL OU WHATSAPP :</p>
                        <p>(+237)674491694/695368645</p>
                        <p>Email: <a href="mailto:jerry@jerrykamgang.com" class="underline">dimfitness@gmail.com</a></p>
                        <p>Instagram: <a href="https://www.instagram.com/jerrykamgang" class="underline">@dimfitness</a>
                        </p>
                    </div>
                    <div class="space-y-4 font-poppins text-white flex flex-col items-center md:ite justify-center md:justify-normal">
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
                    <div class="space-y-4 font-poppins text-white flex flex-col items-center md:ite justify-center md:justify-normal">
                        <h2 class="text-xl font-bold uppercase">Nos Reseaux</h2>
                        <a href="https://www.facebook.com/nomDuCompte" target="_blank" rel="noopener noreferrer"> <i
                                class="fab fa-facebook"></i> Dimfitness</a>
                        <router-link to="/plans-fbwa" class="text-base font-semibold"><i class="fab fa-whatsapp"></i>
                            +(237)674491694/695368645</router-link>
                        <router-link to="/" class="text-base font-semibold hover:text-red-700"><i
                                class="fab fa-instagram"></i> @Dimfitness</router-link>
                        <router-link to="/" class="text-base font-semibold hover:text-red-700"><i
                                class="fab fa-tiktok"></i> Dimfitness</router-link>
                        <a href="https://www.youtube.com/@jeanhouafo3352" target="_blank" rel="noopener noreferrer"
                            class="text-base font-semibold hover:text-red-700"><i class="fab fa-youtube"></i>
                            @Dimfitness</a>
                    </div>
                </div>
                <div class="text-center mt-8">
                    <p class="text-sm">&copy; {{ new Date().getFullYear() }} Jerry Kamgang. Tous droits réservés.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'AppFooter', // Nom du composant modifié
    data() {
        return {
            newYear: new Date().getFullYear(),
        };
    },
};
</script>

<style>
/* Ajoutez ici des styles personnalisés si nécessaire */
</style>