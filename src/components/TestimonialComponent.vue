<template>
    <div class="w-full py-10 px-4 lg:px-8">
        <div class="w-full grid grid-cols-4 md:grid-cols-8 lg:grid-cols-12 gap-4">
            <div v-for="(video, index) in videos" :key="index" data-aos="zoom-in" data-aos-delay="200"
                data-aos-duration="1000" data-aos-easing="ease-in-out"
                class="col-span-4 lg:col-span-3 h-[480px] shadow-2xl shadow-gray-800 overflow-hidden rounded-sm">
                <iframe class="w-full h-full object-cover object-center" :src="video.embedUrl" frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen></iframe>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            videos: [
                {
                    embedUrl: "https://www.youtube.com/embed/1enBmLGAS2Q?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/ZpLR67bcnGQ?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/tZePPfB2Ew8?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/1enBmLGAS2Q?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/ZpLR67bcnGQ?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/tZePPfB2Ew8?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/1enBmLGAS2Q?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/ZpLR67bcnGQ?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/tZePPfB2Ew8?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/1enBmLGAS2Q?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/ZpLR67bcnGQ?autoplay=0",
                },
                {
                    embedUrl: "https://www.youtube.com/embed/tZePPfB2Ew8?autoplay=0",
                },
            ],
        };
    },
};
</script>
