<template>
    <section>
        <div class="container">
            <InnerSectionTitle 
                h2-text="see our top notch services"
                p-text="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium."
            />
            <div class="features-container">
                <div v-for="(feature, index) in features" :key="index" class="feature">
                    <i :class="feature.icon"></i>
                    <h3>{{ feature.title }}</h3>
                    <p>{{ feature.paragraph }}</p>
                    <a href="#">Read more ></a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import InnerSectionTitle from './InnerSectionTitle.vue';

export default {
    name: 'SectionServices',
    components: {
        InnerSectionTitle,
    },
    data: function() {
        return{
            features: [
                {
                    icon: 'fab fa-google',
                    title: 'google SEO',
                    paragraph: 'Vestibulum scelirisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.',
                },
                {
                    icon: 'fas fa-cog',
                    title: 'brand strategy',
                    paragraph: 'Vestibulum scelirisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.',
                },
                {
                    icon: 'fas fa-building',
                    title: 'local SEO',
                    paragraph: 'Vestibulum scelirisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.',
                },
                {
                    icon: 'fas fa-chart-bar',
                    title: 'SEO analysis',
                    paragraph: 'Vestibulum scelirisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.',
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

    section{
        padding: 50px;
        background-color: $deepcove;
        background-image: url('../assets/images/pattern_background.png');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        color: white;
        text-align: center;
        .features-container{
            display: flex;
            flex-flow: row nowrap;
            justify-content: space-around;
            align-items: center;
            .feature{
                display: flex;
                flex-flow: column nowrap;
                justify-content: space-evenly;
                align-items: center;

                background-color: $luckypoint;
                -webkit-box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1); 
                box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1);

                min-height: 350px;
                margin: 50px 10px;
                padding: 30px;
                i{
                    color: $yelloworange;
                    font-size: 30px;
                    &.margin-correct{
                        margin-top: -10px;
                    }
                }
                h3{
                    text-transform: capitalize;
                }
                p{
                    font-size: 0.9rem;
                    font-weight: lighter;
                }
                a{
                    text-decoration: none;
                    color: $yelloworange;
                    font-size: 0.7rem;
                }
            }
        }
        img{
            width: 100%;
        }
    }
</style>