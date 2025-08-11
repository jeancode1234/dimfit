<template>
    <div>
         <div class="w-full h-auto py-24" id="module">
             <div class="w-full lg:w-5/6 mx-auto space-y-4">
                   <h1 data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-lg sm:text-2xl md:text-4xl text-white font-extrabold font-poppins uppercase text-center">LES MODULES de La formation FBWA</h1>
                   <div class="w-full xl:w-4/5 mx-auto p-4 space-y-6">
                       <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-center text-white text-sm font-poppins">L’objectif de cette formation est de vous permettre d’avoir une grosse visibilité sur Facebook et décupler vos ventes. Vous saurez comment
                         avoir des clients en automatique grâce à la publicité Facebook peu importe votre secteur d’activité.</p>
                         <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="text-center text-white text-sm font-poppins">En appliquant mes stratégies depuis chez vous, vous ferez plus de ventes que d’habitude d’ici quelques jours ou semaines. 
                            Vous économiserez votre budget publicitaire en ayant de forts résultats (des millions de francs par mois).</p>
                   </div>
             </div>
             <div class="w-full space-y-4 py-4">
               <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up" class="w-5/6 md:w-3/6 h-[1px] bg-red-600"></div>
               <div class="w-full lg:w-3/6 mx-auto">
                    <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="zoom-in" class="text-center text-white text-sm font-poppins">18 heures de Formation pour vous apprendre à créer 
                        un véritable business en ligne et générer du trafic qui convertir grâce à Facebook et Instagram</p>
               </div>
             </div>
             <AllmodulesComponent/>
             <div class="w-full  flex flex-col space-y-4 items-center justify-center">
                <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="zoom-in" class="text-gray-400 text-sm font-poppins">
                    Cliquez sur le bouton <span class="uppercase md:text-lg font-semibold text-white">Rejoindre la
                        formation</span>
                </p>
                <a data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="zoom-in" href="https://wa.me/+237695863845"
                    class="bg-gradient-to-b to-black/60 from-red-700 font-poppins text-white font-bold py-2 px-4 rounded-tl-2xl rounded-br-2xl"
                    target="_blank" rel="noopener noreferrer">
                    Rejoindre la formation
                </a>
                <div class="w-full space-y-4">
                    <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="zoom-in" class="w-5/6 md:w-3/6 h-[1px] bg-red-600"></div>
                </div>
            </div>
         </div>
         <FooterView/>
    </div>
</template>

<script>
import FooterView from './FooterView.vue';
import AllmodulesComponent from '@/components/AllmodulesComponent.vue';
export default{
    data(){
        return{

        }
    },

    components:{
        AllmodulesComponent,
        FooterView
    }
}
</script>
<style>
#module {
    background-image: linear-gradient(rgba(40, 39, 128, 0.8), rgba(40, 39, 128, 0.8)), url('@/assets/images/background.jpg');
    background-position: center;
    background-size: contain;
    background-repeat: repeat;
}
</style>