<template>
    <div class="text-container">
        <h2>{{ h2Text }}</h2>
        <p>{{ pText }}</p>
    </div>
</template>

<script>
export default {
    name: 'SectionTitle',
    props: ['h2Text', 'pText']
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

    .text-container{

        text-align: center;
        width: 50%;
        
        margin: 50px auto;

        h2{
            text-transform: capitalize;
        }
        p{
            margin: 15px 0;
        }
    }
</style>