<template>
    <div class="container">
        <nav>
            <img src="../assets/images/logo_seo_w_1x.png" alt="Seo Logo">

            <ul>
                <li v-for="(link, index) in linksArray" :key="index" @click=" activeIndex = index" :class="{ 'active' : index === activeIndex }">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </ul>

            <button class="custom-btn bg-yelloworange">Get in touch now</button>
        </nav>
    </div>
</template>

<script>
export default {
    name: "Navbar",
    props: ['linksArray', 'activeIndex']
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

nav{
    position: absolute;
    top: 10px;
    left: 15%;

    width: 70%;

    display: flex;
    flex-flow: row nowrap;
    justify-content: flex-start;
    align-items: center;

    color: white;
    font-size: 12px;
    text-transform: capitalize;
    font-weight: 400;
    img{
        height: 30px;
        }
    ul{
        margin-left: auto;
        list-style-type: none;
        li{
            display: inline-block;
            margin: auto 12px;
            border-bottom: 3px solid transparent;
            cursor: pointer;
            &:hover,
            &.active{
            color: $yelloworange;
            }
            a{
                text-decoration: none;
                color: inherit;
                text-transform: inherit;
                line-height: inherit;
            }
        }
    }
    button{
        margin-left: 12px;
        padding: 10px;
    }
}
        

</style>