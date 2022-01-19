<template>
    <section>
        <div class="container">
            <SectionTitle 
                h2-text="meet the new agency SEO template from the avada team"
                p-text="sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium"
                />
            <div class="features-container">
                <div v-for="(feature, index) in templateFeatures" :key="index" class="feature">
                    <i>{{ feature.icon }}</i>
                    <h3>{{ feature.title }}</h3>
                    <p>{{ feature.paragraph }}</p>
                </div>
            </div>

            <img src="../assets/images/agency-seo-desk-front-800x380.jpg" alt="Agency SEO desk front image">
        </div>
    </section>
</template>

<script>
import SectionTitle from './SectionTitle.vue';

export default {
    name: 'SectionMeetSEO',
    components: {
        SectionTitle,
    },
    data: function() {
        return{
            templateFeatures: [
                {
                    icon: 'icon',
                    title: 'Title',
                    paragraph: 'paragraph1',
                },
                {
                    icon: 'icon',
                    title: 'title',
                    paragraph: 'paragraph2',
                },
                {
                    icon: 'icon',
                    title: 'title',
                    paragraph: 'paragraph3',
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

    section{
        padding-top: 50px;
        background-color: $alabaster;
        color: black;
        text-align: center;
        .features-container{
            display: flex;
            flex-flow: row nowrap;
            justify-content: space-around;
            align-items: center;
            .feature{
                display: flex;
                flex-flow: column nowrap;
                justify-content: space-around;
                align-items: center;

                background-color: white;
                -webkit-box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1); 
                box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1);

                min-height: 250px;
                margin: 50px 10px;
                width: calc((100% / 3) - 20px);
            }
        }
    }
</style>