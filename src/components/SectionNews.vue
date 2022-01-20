<template>
    <section>
        <div class="container">
            <InnerSectionTitle 
                h2-text="our news"
                p-text="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium."
            />
            <div class="features-container">
                <div v-for="(item, index) in items" :key="index" class="feature">
                    <div class="img-container">
                        <img :src="item.imgSrc" :alt="item.alt">
                    </div>
                    <h2>{{ item.title }}</h2>
                    <span class="date">{{ item.date }}</span>
                    <p>{{ item.paragraph }}</p>
                </div>
            </div>

            <button class="custom-btn bg-yelloworange">go to news</button>
        </div>
    </section>
</template>

<script>
import InnerSectionTitle from './InnerSectionTitle.vue';

export default {
    name: 'SectionNews',
    components: {
        InnerSectionTitle,
    },
    data: function() {
        return{
            items: [
                {
                    alt: 'Image 1',
                    imgSrc: require('../assets/images/related-service-2-700x441.jpg'),
                    title: 'why you need a SEO agency now',
                    date: 'November 1st, 2017',
                    paragraph: 'Alorem ipsum dolor, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque ague, at gravida mi blandit.',

                },
                {
                    alt: 'Image 2',
                    imgSrc: require('../assets/images/related-service-4-700x441.jpg'),
                    title: 'SEO tips for your startup',
                    date: 'November 1st, 2017',
                    paragraph: 'Alorem ipsum dolor, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque ague, at gravida mi blandit.',
                },
                {
                    alt: 'Image 3',
                    imgSrc: require('../assets/images/blog-post-6-700x441.jpg'),
                    title: 'image optimization for your site',
                    date: 'November 1st, 2017',
                    paragraph: 'Alorem ipsum dolor, consectetur adipiscing elit. In et scelerisque sem. Nunc molestie neque ague, at gravida mi blandit.',
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
            flex-flow: row nowrap;
            justify-content: center;
            align-items: center;
            margin: 50px 0;
            .feature{
                display: flex;
                flex-flow: column nowrap;
                justify-content: space-around;
                align-items: center;

                color: $regentgray;

                margin: 10px;
                .img-container{
                    height: auto;
                    img{
                        width: 100%;
                        height: 100%;
                    }
                }
                h2{
                    color: $yelloworange;
                    font-size: 15px;
                    text-transform: capitalize;
                    margin-top: 5px;
                    margin-bottom: 3px;
                }
                .date{
                    font-size: 0.5rem;
                }
                p{
                    font-size: 0.7rem;
                    margin: 10px 0;
                }
            }
        }
        button{
            padding: 10px 20px;
            margin: 15px;
        }
    }
</style>