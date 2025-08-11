<template>
    <div class="w-full lg:p-4 bg-[#1C3045]">

        <!-- Galerie d'images -->
        <div class="grid grid-cols-2 md:grid-cols-4">
            <img v-for="(image, index) in images" :key="index" :src="image" data-aos="zoom-in" data-aos-delay="200"
                data-aos-duration="1000" data-aos-easing="ease-in-out"
                class="w-full h-80 object-cover cursor-pointer hover:opacity-80 transition" @click="openModal(index)" />
        </div>

        <!-- Modale -->
        <div v-if="isModalOpen" class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-90">
            <!-- Numérotation -->
            <div class="absolute top-4 left-6 text-white text-lg font-bold">
                {{ currentIndex + 1 }} / {{ images.length }}
            </div>

            <!-- Bouton fermer -->
            <button class="absolute top-4 right-6 text-white text-3xl font-bold hover:text-gray-400"
                @click="closeModal">
                ✕
            </button>

            <!-- Flèche gauche -->
            <button class="absolute left-4 text-white text-4xl p-2 hover:bg-white/20 rounded-full" @click="prevImage">
                ‹
            </button>

            <!-- Image affichée -->
            <transition name="fade" mode="out-in">
                <img :key="currentImage" :src="currentImage"
                    class="max-h-[80vh] w-3/6 mx-auto object-cover  shadow-lg" />
            </transition>

            <!-- Flèche droite -->
            <button class="absolute right-4 text-white text-4xl p-2 hover:bg-white/20 rounded-full" @click="nextImage">
                ›
            </button>
        </div>


    </div>
</template>

<script>
export default {
    data() {
        return {
            images: [
                "https://img.freepik.com/free-photo/mystery-vanishing-forest-path-ahead-generated-by-ai_188544-26803.jpg?semt=ais_hybrid&w=740&q=80",
                "https://st2.depositphotos.com/2435561/5260/i/450/depositphotos_52600329-stock-photo-skyline-drive-in-a-heavily.jpg",
                "https://media.istockphoto.com/id/939185044/photo/magic-forest-path.jpg?s=612x612&w=0&k=20&c=Y4oUwr1VNED84I3pgolhIlZoJMcGdq1Az1VZ7SNjg-g=",
                "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRLK9l5v8IJzh9qg2FPyVj5B0R6pc37X3WorK371cJGFJJdftNG85FSFSmquIMaz0ysR3w&usqp=CAU",
                "https://st2.depositphotos.com/1005518/7129/i/450/depositphotos_71299897-stock-photo-bus-traveling-through-a-road.jpg",
                "https://static.vecteezy.com/system/resources/thumbnails/049/396/887/small_2x/endless-road-of-travel-on-rural-highways-there-are-natural-trees-on-both-sides-of-the-road-photo.jpeg",
            ],
            currentIndex: 0,
            isModalOpen: false,
        };
    },
    computed: {
        currentImage() {
            return this.images[this.currentIndex];
        },
    },
    methods: {
        openModal(index) {
            this.currentIndex = index;
            this.isModalOpen = true;
            document.body.style.overflow = "hidden"; // désactive le scroll en arrière-plan
        },
        closeModal() {
            this.isModalOpen = false;
            document.body.style.overflow = "";
        },
        nextImage() {
            this.currentIndex =
                (this.currentIndex + 1) % this.images.length;
        },
        prevImage() {
            this.currentIndex =
                (this.currentIndex - 1 + this.images.length) %
                this.images.length;
        },
    },
};
</script>

<style>
.fade-enter-active,
.fade-leave-active {
    transition: opacity 0.4s ease;
}

.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}
</style>