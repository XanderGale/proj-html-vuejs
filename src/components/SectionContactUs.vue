<template>
    <section>
        <div class="container">
            <InnerSectionTitle 
                h2-text="start your free consultation"
                p-text="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium."
            />

            <div class="blackopacity"></div>
            
            <button class="custom-btn bg-yelloworange">Contact us</button>
        </div>
    </section>
</template>

<script>
import InnerSectionTitle from './InnerSectionTitle.vue';

export default {
    name: 'SectionContactUs',
    components: {
        InnerSectionTitle,
    },
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

    section{
        position: relative;
        padding: 50px;
        background-image: url('../assets/images/CTA-seo-1.jpg');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        color: white;
        text-align: center;
        z-index: -2;
        .blackopacity{
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: black;
            opacity: 0.5;
            z-index: -1;
        }
        button{
            padding: 10px 15px;
        }
    }
</style>