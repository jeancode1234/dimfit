<template>
    <div>
        <div class="w-full hidden lg:flex flex-col px-12 py-2 bg-black font-poppins text-white ">
            <TypeWriteComponent />
            <div class="flex items-center justify-between w-full">

                <div>
                    <img src="/images/logo.png" width="100" height="100" alt="logo">
                </div>
                <nav class="flex items-center justify-center space-x-8">

                    <router-link to="/"
                        class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                        <i class="fas fa-home"></i> Formation FBWA
                    </router-link>
                    <router-link to="/plans-fbwa"
                        class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                        plans FBWA
                    </router-link>
                    <router-link to="/temoignages"
                        class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                        témoignages
                    </router-link>
                    <router-link to="/modules"
                        class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                        les modules
                    </router-link>
                    <a href="https://wa.me/+237695863845" target="_blank"
                        class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                        contact
                    </a>
                    <router-link to="/"
                        class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                        qui suis-je
                    </router-link>
                    <a href="https://www.youtube.com/@jeanhouafo3352" target="_blank" rel="noopener noreferrer"
                        class="block text-sm font-semibold font-poppins uppercase text-white hover:text-[#E30065] duration-200 focus:outline-none">
                        vidéos
                    </a>
                </nav>
            </div>
        </div>
        <div :class="(showMobile == true ? 'hidden' : 'flex')"
            class="w-full flex items-center justify-between bg-black lg:hidden p-4">
            <div>
                <img src="/images/logo.png" width="100" height="100" alt="logo">
            </div>
            <svg @click="openNav" xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="60" height="60"
                viewBox="0,0,256,256">
                <g fill="#ffffff" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt"
                    stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0"
                    font-family="none" font-weight="none" font-size="none" text-anchor="none"
                    style="mix-blend-mode: normal">
                    <g transform="scale(3.55556,3.55556)">
                        <path
                            d="M56,48c2.209,0 4,1.791 4,4c0,2.209 -1.791,4 -4,4c-1.202,0 -38.798,0 -40,0c-2.209,0 -4,-1.791 -4,-4c0,-2.209 1.791,-4 4,-4c1.202,0 38.798,0 40,0zM56,32c2.209,0 4,1.791 4,4c0,2.209 -1.791,4 -4,4c-1.202,0 -38.798,0 -40,0c-2.209,0 -4,-1.791 -4,-4c0,-2.209 1.791,-4 4,-4c1.202,0 38.798,0 40,0zM56,16c2.209,0 4,1.791 4,4c0,2.209 -1.791,4 -4,4c-1.202,0 -38.798,0 -40,0c-2.209,0 -4,-1.791 -4,-4c0,-2.209 1.791,-4 4,-4c1.202,0 38.798,0 40,0z">
                        </path>
                    </g>
                </g>
            </svg>
        </div>
        <div v-if="showMobile" class="w-full min-h-screen fixed z-30 bg-black block lg:hidden">
            <div class="flex items-center justify-between p-4">
                <img src="/images/logo.png" width="100" height="100" alt="logo">
                <svg @click="closeNav" xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="60" height="60" viewBox="0,0,256,256">
                    <g fill="#ffffff" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt"
                        stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0"
                        font-family="none" font-weight="none" font-size="none" text-anchor="none"
                        style="mix-blend-mode: normal">
                        <g transform="scale(3.55556,3.55556)">
                            <path
                                d="M19,15c-1.023,0 -2.04812,0.39087 -2.82812,1.17188c-1.562,1.562 -1.562,4.09425 0,5.65625l14.17188,14.17188l-14.17187,14.17188c-1.562,1.562 -1.562,4.09425 0,5.65625c0.78,0.78 1.80513,1.17188 2.82813,1.17188c1.023,0 2.04812,-0.39088 2.82813,-1.17187l14.17188,-14.17187l14.17188,14.17188c1.56,1.562 4.09525,1.562 5.65625,0c1.563,-1.563 1.563,-4.09325 0,-5.65625l-14.17187,-14.17187l14.17188,-14.17187c1.562,-1.562 1.562,-4.09425 0,-5.65625c-1.56,-1.561 -4.09625,-1.562 -5.65625,0l-14.17187,14.17188l-14.17187,-14.17187c-0.78,-0.78 -1.80513,-1.17187 -2.82812,-1.17187z">
                            </path>
                        </g>
                    </g>
                </svg>
            </div>
            <!-- Bouton fermer -->
            <div class="py-4 w-full flex flex-col space-y-4 ">
                <div class="w-full border-b  border-red-800  duration-200 ">
                    <router-link to="/" class=" p-4 font-poppins block hover:text-red-600 text-white text-lg uppercase">Formation
                        fbwa</router-link>
                </div>
                <div class="w-full border-b border-red-800">
                    <router-link to="/plans-fbwa" class="p-4 font-poppins block hover:text-red-600 text-white text-lg uppercase">Plans fbwa</router-link>
                </div>
                <div class="w-full border-b border-red-800">
                    <router-link to="/temoignages" class="p-4 font-poppins block hover:text-red-600 text-white text-lg uppercase">témoignages</router-link>
                </div>
                <div class="w-full border-b border-red-800">
                    <router-link to="/modules" class="p-4 font-poppins block hover:text-red-600 text-white text-lg uppercase">modules</router-link>
                </div>
                <div class="w-full border-b border-red-800">
                    <router-link to="/" class="p-4 font-poppins block hover:text-red-600 text-white text-lg uppercase">qui suis-je</router-link>
                </div>
                <div class="w-full border-b border-red-800 py-2">
                    <router-link to="/" class="p-4 font-poppins block hover:text-red-600 text-white text-lg uppercase">vidéos</router-link>
                </div>
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
            showMobile: false,
        }
    },
    methods: {
        openNav() {
            this.showMobile = true
            // document.body.style.overflow = "hidden";
        },
        closeNav() {
            this.showMobile = false
        }
    },
    mounted() {
        // Any initialization logic can go here
    },
};
</script>