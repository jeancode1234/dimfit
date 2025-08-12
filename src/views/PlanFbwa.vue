<template>
    <div class="w-full">
        <div class="w-full bg-contain bg-center bg-repeat h-auto  overflow-hidden" :key="currentIndex"
            :style="{ backgroundImage: `url(${images[currentIndex]})` }">

            <!-- Couche sombre + contenu -->
            <div class=" inset-0 w-full  py-12 bg-gradient-to-b from-black/80 to-[#0E2F51]/50 bg-[#0E2F51]/60">
                <div class="w-full lg:w-5/6 mx-auto font-poppins h-auto space-y-4 lg:space-y-8 sm:px-4">
                    <h1 data-aos="zoom-in"
                        class="uppercase text-2xl lg:text-4xl xl:text-5xl text-white text-center font-poppins font-extrabold">
                        Plans fbwa</h1>
                    <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="zoom-in"
                        class="text-gray-300  md:text-lg text-center">
                        La <strong> Formation FBWA</strong> à été mise à jour avec les meilleures stratégies de 2025 qui
                        vous permettront d’augmenter massivement vos ventes.
                    </p>
                    <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="zoom-in"
                        class="text-gray-300 md:text-lg text-center">
                        Je l’ai améliorée pour pallier à tous les obstacles qu’ont rencontré les précédents membres
                        malgré
                        l’énorme succès de mes anciennes stratégies, cette nouvelle version 2025 est beaucoup plus
                        améliorée
                        et pédagogique.
                    </p>
                    <PlansFbwaComponent />
                </div>
                <div class="w-full h-12"></div>
                <div class="w-full">
                    <div class="grid grid-cols-4 lg:grid-cols-8 xl:grid-cols-12 gap-8 xl:w-5/6 mx-auto px-8 lg:px-4">
                        <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000"
                            data-aos="zoom-in"
                            class="col-span-4 bg-blue-800/60 transform -translate-y-8 relative rounded-2xl overflow-hidden">
                            <div
                                class="absolute font-bold font-poppins text-white bg-pink-600/80 py-2 text-base right-0 top-10 transform translate-x-12 rotate-45 w-52 flex justify-center">
                                Plus sollicité</div>
                            <div class="w-full bg-blue-900/80 space-y-2 text-white p-2">
                                <h2 class="text-center uppercase text-2xl font-poppins font-bold">FBWA start 2025</h2>
                                <p class="text-center font-poppins font-bold text-white uppercase">Plan 1 - De 0 à 10
                                    millions
                                    de ca / mois</p>
                            </div>
                            <div class="w-full  bg-blue-800/40 p-4 ">
                                <div class="flex justify-center space-x-4">

                                    <p
                                        class="text-red-800 uppercase text-2xl line-through decoration-red-500 font-bold font-poppins">
                                        990000 <span class="text-white">FCFA</span></p>
                                    <p class="uppercase text-2xl text-white font-bold font-poppins">199000 FCFA</p>
                                </div>
                                <p class="text-white text-sm italic text-center">Paiement en tranches possible, cliquez
                                    sur
                                    le
                                    bouton "REJOINDRE FBWA START" en bas de cette page.</p>
                            </div>
                            <div class="text-white space-y-4 text-sm bg-blue-800/20 p-4 font-poppins">
                                <p>Accès à la Formation FBWA 2025 ➜ Marketing Digital | Publicité Facebook et Instagram,
                                    plus
                                    détaillée et 10 fois plus avancée en stratégies par rapport à la FBWA 2022.</p>
                                <div class="w-full space-y-4">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>6 Mois d'accès au groupe Start Facebook.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>6 Mois d'accès au groupe Start WhatsApp.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>Votre numéro sera enregistré comme membre <strong>FBWA START</strong> pour vous
                                        différencier des numéros inconnus.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-5/6 mx-auto h-[1px] bg-white"></div>
                                    <p> 6 Mois d'accompagnement sur WhatsApp.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 6 Mois d'assistance en présentiel ou en télé distanciel possible par mon équipe
                                        4
                                        fois
                                        par semaine.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 6 Mois de live Facebook avec moi 2 fois par semaine.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>Délai de réponse "Normal" car je reçois plus de 9 000 messages par jour.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 80 idées de produits et approvisionnement local,
                                        ainsi qu'en Chine, pour démarrer facilement la vente en ligne.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 90 secteurs d'activité où la formation peut s'implémenter..</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> Accès et assistance par mon équipe
                                        Pro au système de facturation Excel pour l'établissement des Factures Pro des
                                        ventes.
                                    </p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> Accès et assistance
                                        par mon équipe Pro au système de facturation Excel pour l'établissement des
                                        Factures
                                        Pro
                                        des ventes.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> Lecture des vidéos de la Formation FBWA 2025 en ligne depuis un téléphone ou un
                                        ordinateur.</p>
                                </div>

                            </div>
                            <div class="w-full py-8 bg-red-800/20 flex flex-col items-center">
                                <router-link to="/"
                                    class="text-white uppercase font-poppins text-base underline p-2 rounded-full bg-red-900/60">rejoindre
                                    fbwa start 2025</router-link>
                            </div>
                        </div>
                        <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000"
                            data-aos="zoom-in"
                            class="col-span-4 bg-[#0A8263]/60 transform -translate-y-8 relative rounded-2xl overflow-hidden">
                            <div
                                class="absolute font-bold font-poppins text-white bg-[#0A8263]/80 py-2 text-base right-0 top-10 transform translate-x-12 rotate-45 w-52 flex justify-center uppercase">
                                recommandé</div>
                            <div class="w-full space-y-2 text-white p-3">
                                <h2 class="text-center uppercase text-2xl font-poppins font-bold">FBWA PRO 2025</h2>
                                <p class="text-center font-poppins font-bold text-white uppercase">Plan 3 - De 0 à 100
                                    millions
                                    de ca / mois</p>
                            </div>
                            <div class="w-full bg-[#0A8263]/80 py-3">
                                <div class="flex flex-wrap justify-center space-x-4 text-center">

                                    <p
                                        class="text-gray-900 uppercase text-2xl line-through decoration-black font-bold font-poppins">
                                        3680000FCFA<span class="text-white">FCFA</span></p>
                                    <p class="uppercase text-2xl text-white font-bold font-poppins">1 469 000FCFA</p>
                                </div>
                                <p class="text-white text-sm italic text-center">Paiement en tranches possible, cliquez
                                    sur
                                    le bouton "REJOINDRE FBWA PRO" en bas de cette page.</p>
                            </div>
                            <div class="text-white space-y-4 text-sm p-4 font-poppins">
                                <p>Accès complet à la Formation FBWA GOLD 2025, avec 2 fois plus de stratégies top
                                    secrètes,
                                    réservées aux experts exclusivement, par rapport à la FBWA PRO 2025.</p>
                                <div class="w-full space-y-4">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 12 Mois d'accès au groupe Gold Facebook.
                                    </p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>12 Mois d'accès au groupe Gold WhatsApp.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>Votre numéro sera enregistré avec 03 étoiles ✨✨✨ comme membre FBWA GOLD pour vous
                                        différencier des membres FBWA PRO et ainsi vous mettre en priorité principale.
                                    </p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-5/6 mx-auto h-[1px] bg-white"></div>
                                    <p>12 Mois d'accompagnement Gold sur WhatsApp.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>12 Mois d'assistance en présentiel ou en télé distanciel par moi en fonction de
                                        votre
                                        disponibilité.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 12 Mois de live Facebook avec moi 4 fois par semaine.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> Délai de réponse "Plus Rapide" car vous êtes notre priorité principale.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 20 Idées de produits Gold et approvisionnement local, ainsi qu'en Chine, pour
                                        démarrer
                                        facilement la vente en ligne.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>90 secteurs d'activité où la formation peut s'implémenter.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> Accès et assistance par moi au système de facturation Excel pour l'établissement
                                        des
                                        Factures Pro des ventes.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>Accès et assistance par moi au système de comptabilité Excel pour une
                                        comptabilité
                                        automatique des Factures Pro des ventes.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>Lecture des vidéos de la Formation FBWA GOLD 2025 en ligne depuis un téléphone ou
                                        un
                                        ordinateur.</p>
                                </div>

                            </div>
                            <div class="w-full py-6 space-y-2 font-poppins flex flex-col items-center">
                                <router-link to="/"
                                    class="text-white uppercase text-sm underline p-2 rounded-full bg-gradient-to-b to-black from-green-800">rejoindre
                                    fbwa Gold 2025</router-link>
                                <p class="text-sm text-white text-center">Satisfait ou remboursé sur 48 heures.</p>
                            </div>
                        </div>
                        <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000"
                            data-aos="zoom-in"
                            class="col-span-4 bg-[#7F7143]/60 transform -translate-y-8 relative rounded-2xl overflow-hidden">
                            <div
                                class="absolute font-bold font-poppins text-white bg-[#7F7143]/80 py-2 text-base right-0 top-10 transform translate-x-12 rotate-45 w-52 flex justify-center uppercase">
                                Allez plus vite</div>
                            <div class="w-full space-y-2 text-white p-3">
                                <h2 class="text-center uppercase text-2xl font-poppins font-bold">FBWA Gold 2025</h2>
                                <p class="text-center font-poppins font-bold text-white uppercase">Plan 3 - De 0 à 100
                                    millions
                                    de ca / mois</p>
                            </div>
                            <div class="w-full bg-[#7F7143]/80 py-3">
                                <div class="flex flex-wrap justify-center space-x-4 text-center">

                                    <p
                                        class="text-gray-900 uppercase text-2xl line-through decoration-black font-bold font-poppins">
                                        9990000<span class="text-white">FCFA</span></p>
                                    <p class="uppercase text-2xl text-white font-bold font-poppins">3960000FCFA</p>
                                </div>
                                <p class="text-white text-sm italic text-center">Paiement en tranches possible, cliquez
                                    sur
                                    le
                                    bouton "REJOINDRE FBWA GOLD" en bas de cette page.</p>
                            </div>
                            <div class="text-white space-y-4 text-sm p-4 font-poppins">
                                <p>Accès complet à la Formation FBWA GOLD 2025, avec 2 fois plus de stratégies top
                                    secrètes,
                                    réservées aux experts exclusivement, par rapport à la FBWA PRO 2025.</p>
                                <div class="w-full space-y-4">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 12 Mois d'accès au groupe Gold Facebook.
                                    </p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>12 Mois d'accès au groupe Gold WhatsApp.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>Votre numéro sera enregistré avec 03 étoiles ✨✨✨ comme membre FBWA GOLD pour vous
                                        différencier des membres FBWA PRO et ainsi vous mettre en priorité principale.
                                    </p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-5/6 mx-auto h-[1px] bg-white"></div>
                                    <p>12 Mois d'accompagnement Gold sur WhatsApp.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>12 Mois d'assistance en présentiel ou en télé distanciel par moi en fonction de
                                        votre
                                        disponibilité.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 12 Mois de live Facebook avec moi 4 fois par semaine.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> Délai de réponse "Plus Rapide" car vous êtes notre priorité principale.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> 20 Idées de produits Gold et approvisionnement local, ainsi qu'en Chine, pour
                                        démarrer
                                        facilement la vente en ligne.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>90 secteurs d'activité où la formation peut s'implémenter.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p> Accès et assistance par moi au système de facturation Excel pour l'établissement
                                        des
                                        Factures Pro des ventes.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>Accès et assistance par moi au système de comptabilité Excel pour une
                                        comptabilité
                                        automatique des Factures Pro des ventes.</p>
                                </div>
                                <div class="w-full space-y-4 ">
                                    <div class="w-full h-[1px] bg-white"></div>
                                    <p>Lecture des vidéos de la Formation FBWA GOLD 2025 en ligne depuis un téléphone ou
                                        un
                                        ordinateur.</p>
                                </div>

                            </div>
                            <div class="w-full py-6 space-y-2 font-poppins flex flex-col items-center">
                                <router-link to="/"
                                    class="text-white uppercase text-sm underline p-2 rounded-full bg-gradient-to-b to-black from-[#7F7143]">rejoindre
                                    fbwa Gold 2025</router-link>
                                <p class="text-sm text-white text-center">Satisfait ou remboursé sur 48 heures.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>


        </div>
        <PlbwaComponent />
        <Footer />
    </div>
</template>
<script>
import img from '@/assets/images/picture1.jpeg';
import img1 from '@/assets/images/picture2.jpeg';
import img2 from '@/assets/images/picture3.jpeg';
import PlbwaComponent from '@/components/PlbwaComponent.vue';
import PlansFbwaComponent from '@/components/PlansFbwaComponent.vue';
import Footer from './FooterView.vue';
export default {
    data() {
        return {
            currentIndex: 0,
            images: [img, img1, img2],
            autoPlayInterval: null,
            displayDuration: 7000, // transition toutes les 7s
        };
    },
    components: {
        PlbwaComponent,
        PlansFbwaComponent,
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
    },
    mounted() {
        this.startAutoPlay();
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
</style>
