<template>
    <div>
        <div class="w-full px-12 py-2 bg-black font-poppins text-white ">
             <TypeWriteComponent/>
            <div class="flex items-center justify-between w-full">

                <div>
                    <img src="/images/logo.png" width="100" height="100" alt="">
                </div>
                <nav class="flex items-center justify-center space-x-8">
                   
                        <router-link to="/" class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                            <i class="fas fa-home"></i> Formation FBWA
                        </router-link>
                        <router-link to="/plans-fbwa" class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                            plans FBWA
                        </router-link>
                         <router-link to="/temoignages" class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                             témoignages
                        </router-link>
                        <router-link to="/modules" class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                             les modules
                        </router-link>
                         <a  href="https://wa.me/+237695863845" target="_blank" class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                             contact
                         </a>
                         <router-link to="/" class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                             qui suis-je
                        </router-link>
                        <a href="https://www.youtube.com/@jeanhouafo3352" target="_blank" rel="noopener noreferrer" class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                            vidéos
                        </a>
                </nav>
            </div>
        </div>

        <router-view name="one"></router-view>
    </div>
</template>
<script>
import TypeWriteComponent from '@/components/TypeWriteComponent.vue';
export default {
    components: {
        TypeWriteComponent
    },
    data() {
        return {

        }
    },
    mounted() {
        // Any initialization logic can go here
    },
};
</script>