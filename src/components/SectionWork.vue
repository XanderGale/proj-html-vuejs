<template>
    <section>
        <div class="container">
            <InnerSectionTitle 
                h2-text="our work"
                p-text="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium."
            />
            <div class="features-container">
                <div v-for="(image, index) in images" :key="index" class="feature">
                    <img :src="image.imgSrc" :alt="image.alt">
                </div>
            </div>

            <button class="custom-btn bg-yelloworange">view our work</button>
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
            images: [
                {
                    alt: 'Image 1',
                    imgSrc: require('../assets/images/case-study-gallery-3-1.jpg'),
                },
                {
                    alt: 'Image 2',
                    imgSrc: require('../assets/images/case-study-gallery-2.jpg'),
                },
                {
                    alt: 'Image 3',
                    imgSrc: require('../assets/images/case-study-gallery-1-1.jpg'),
                },
                {
                    alt: 'Image 4',
                    imgSrc: require('../assets/images/case-study-gallery-4-1.jpg'),
                },
                {
                    alt: 'Image 5',
                    imgSrc: require('../assets/images/case-study-gallery-5-1.jpg'),
                },
                {
                    alt: 'Image 6',
                    imgSrc: require('../assets/images/case-study-gallery-6-1.jpg'),
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
        background-color: $alabaster;
        color: black;
        text-align: center;
        .features-container{
            display: flex;
            flex-flow: row wrap;
            justify-content: flex-start;
            align-items: flex-start;
            .feature{
                display: flex;
                flex-flow: column nowrap;
                justify-content: space-evenly;
                align-items: center;

                -webkit-box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1); 
                box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1);

                width: calc((100% / 3) - 10px );
                height: 250px;
                margin: 5px;
                img{
                    width: 100%;
                    height: 100%;
                }
            }
        }
        button{
            width: 150px;
            padding: 10px;
            margin: 50px;
        }
    }
</style>