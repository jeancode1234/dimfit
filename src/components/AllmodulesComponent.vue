<template>
    <div>
        <div class="grid grid-cols-4 lg:grid-cols-8 grid-flow-row gap-8 w-full py-12">
            <div data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000" data-aos="fade-up"
                v-for="(card, index) in cards" :key="index" class="col-span-4 ">
                <div
                    class="flex py-2 justify-center rounded-tr-[36px] items-center text-center w-44 text-base md:text-lg uppercase bg-gradient-to-b to-black from-[#c7453b]  bg-[#3B1C4C] text-white font-poppins">
                    <router-link to="/" class="underline ">{{ card.title1 }}</router-link>
                </div>
                <div class=" w-full h-auto group ">
                    <div class=" w-full h-auto duration-700 ">

                        <!-- Face avant -->
                        <div
                            class=" text-white w-full font-poppins h-auto bg-[#011B31]/60 p-6 flex flex-col  space-y-4">
                            <h2 data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000"
                                data-aos="fade-up" class="text-lg md:text-xl font-bold  uppercase">{{ card.subtitle1 }}
                            </h2>
                            <p data-aos-easing="ease-in-out" data-aos-delay="200" data-aos-duration="1000"
                                data-aos="fade-up" class="text-sm">
                                {{ card.description1 }}
                            </p>
                            <div class="py-2 w-full">
                                <router-link :to="card.lien" class="px-8 py-3 bg-[#011B31] text-white font-poppins">Voir
                                    plus</router-link>
                            </div>
                        </div>



                    </div>
                </div>
            </div>

        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            cards:
                [
                    {
                        title1: "Introduction",
                        subtitle1: "Les Audiences et Optimisations",
                        description1: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine,Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        title2: "Les Audiences et Optimisations",
                        description2: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine, Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        lien: "@/views/HomePageView.vue"
                    },
                    {
                        title1: "Modules 1",
                        subtitle1: "Les Audiences et Optimisations",
                        description1: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine,Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        title2: "Les Audiences et Optimisations",
                        description2: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine, Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        lien: "/"
                    },
                    {
                        title1: "Modules 2",
                        subtitle1: "Les Audiences et Optimisations",
                        description1: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine,Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        title2: "Les Audiences et Optimisations",
                        description2: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine, Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        lien: ""
                    },
                    {
                        title1: "Modules 3",
                        subtitle1: "Les Audiences et Optimisations",
                        description1: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine,Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        title2: "Les Audiences et Optimisations",
                        description2: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine, Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        lien: "@/views/HomePageView.vue"
                    },
                    {
                        title1: "Modules 4",
                        subtitle1: "Les Audiences et Optimisations",
                        description1: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine,Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        title2: "Les Audiences et Optimisations",
                        description2: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine, Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        lien: "@/views/HomePageView.vue"
                    },
                    {
                        title1: "Modules 5",
                        subtitle1: "Les Audiences et Optimisations",
                        description1: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine,Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        title2: "Les Audiences et Optimisations",
                        description2: "Dans l'introduction de la formation FBWA, je présente ses avantages en mettant l'accent sur la transformation de votre état d'esprit et en vous motivant. Je partage 80 idées de produits à fort potentiel et j'explique comment les commander en gros à moindre coût en Chine, Turquie et Dubaï. Je montre aussi comment appliquer les stratégies de la formation FBWA dans 90 secteurs d'activité, au-delà du commerce en ligne. Enfin, j'explique comment satisfaire vos clients pour assurer leur entière satisfaction.",
                        lien: "@/views/HomePageView.vue"
                    },

                ]
        }
    }
}
</script>
