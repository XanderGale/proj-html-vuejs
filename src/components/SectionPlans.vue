<template>
    <section>
        <div class="container">
            <InnerSectionTitle 
                h2-text="our plans"
                p-text="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium."
            />
            <div class="features-container">
                <div v-for="(plan, index) in plans" :key="index" class="feature">
                    <h3>{{ plan.name }}</h3>
                    <div class="price-container">
                        <span class="money-sign">$</span>
                        <span class="price">{{ plan.price }}</span>
                        <span class="price-cents">99</span>
                        <span class="time">monthly</span>
                    </div>
                    <p>{{ plan.projects }}</p>
                    <p>{{ plan.space }}</p>
                    <p>{{ plan.users }}</p>
                    <button class="custom-btn bg-alabaster">Start Today</button>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import InnerSectionTitle from './InnerSectionTitle.vue';

export default {
    name: 'SectionPlans',
    components: {
        InnerSectionTitle,
    },
    data: function() {
        return{
            plans: [
                {
                    name: 'standard',
                    price: '19',
                    projects: '5 Projects',
                    space: '5 GB Storage',
                    users: 'Unlimited Users',
                },
                {
                    name: 'premium',
                    price: '29',
                    projects: '10 Projects',
                    space: '15 GB Storage',
                    users: 'Unlimited Users',
                },
                {
                    name: 'professional',
                    price: '39',
                    projects: '15 Projects',
                    space: '30 GB Storage',
                    users: 'Unlimited Users',
                },
                {
                    name: 'extreme',
                    price: '59',
                    projects: 'Unlimited Projects',
                    space: 'Unlimited Storage',
                    users: 'Unlimited Users',
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
        background-color: transparent;
        background-image: url('../assets/images/background1.jpg');
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
                justify-content: space-between;
                align-items: center;

                color: black;

                background-color: $alabaster;
                -webkit-box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1); 
                box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1);

                min-height: 400px;
                margin: 5px;
                padding: 25px;

                width: calc((100% / 4) - 10px);
                h2{
                    text-transform: capitalize;
                    font-weight: bolder;
                }
                h3{
                    text-transform: capitalize;
                }
                .price-container{
                    position: relative;
                    .money-sign{
                        position: absolute;
                        font-size: 0.9rem;
                        top: 10px;
                        left: -9px;
                    }
                    .price{
                        font-weight: 600;
                        font-size: 45px;
                        color: $purpleheart,
                    }
                    .price-cents{
                        color: $purpleheart;
                        position: absolute;
                        top: 10px;
                        right: -20px;
                        font-weight: bold;
                    }
                    .time{
                        position: absolute;
                        font-size: 0.5rem;
                        bottom: 10px;
                        right: -30px;
                    }
                }
                p{
                    font-size: 0.9rem;
                    font-weight: lighter;
                }
                button{
                    padding: 15px;
                    &:hover{
                        background-color: $yelloworange;
                        color: white;
                        border: 1px solid transparent;
                    }
                }
            }
        }
        img{
            width: 100%;
        }
    }
</style>