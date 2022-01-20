<template> 
    <section>
        <div class="container">
            <InnerSectionTitle 
                h2-text="what our clients say"
            />
            <div class="feedbacks">
                <img :src="feedbacks[activeIndex].image" :alt="feedbacks[activeIndex].name + ' image'">
                <h2>{{ feedbacks[activeIndex].comment }}</h2>
                <div class="name-industry">
                    <span>{{ feedbacks[activeIndex].name + ', ' }}</span>
                    <span>{{ feedbacks[activeIndex].industry }}</span>
                </div>
                
            </div>
        </div>
    </section>
</template>

<script>
import InnerSectionTitle from './InnerSectionTitle.vue';

export default {

    name: "SectionClients",
    components: {
        InnerSectionTitle,
    },
    data: function(){
        return{
            activeIndex: 0,
            feedbacks: [
                {
                    image: require('../assets/images/testimonials-2.jpg'),
                    comment: 'Ability proceeds with a fusion of skills, knowledge, understanding and imagination, consolidated by experience.',
                    name: 'Luis Desalvo',
                    industry: 'Creo tech',
                },
                {
                    image: require('../assets/images/testimonials-1.jpg'),
                    comment: 'Ability proceeds with a fusion of skills, knowledge, understanding and imagination, consolidated by experience.',
                    name: 'Luis Desalvo',
                    industry: 'Creo tech',
                },
            ],
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

    section{
        padding: 50px;
        color: black;
        background-color: white;
        text-align: center;
        .feedbacks{
            display: flex;
            flex-flow: column nowrap;
            justify-content: center;
            align-items: center;
            width: 70%;
            margin: auto;
            img{
                border-radius: 50%;
                height: 250px;
                width: 250px;

                -webkit-box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1); 
                box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1);
            }
            h2{
                margin: 20px auto;
                font-size: 1.1rem;
                font-style: italic;
            }
            .name-industry{
                margin: 10px auto;
            }
        }
    }
</style>