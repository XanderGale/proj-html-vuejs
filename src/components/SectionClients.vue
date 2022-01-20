<template> 
    <section>
        <div class="container">
            <InnerSectionTitle 
                h2-text="what our clients say"
            />
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
            feedbacks: [
                {
                    image: '',
                    comment: '',
                    name: '',
                    industy: '',
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
    }
</style>