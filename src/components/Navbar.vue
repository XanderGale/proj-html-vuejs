<template>
    <nav>
        <img src="../assets/images/logo_seo_w_1x.png" alt="Seo Logo">

        <ul>
            <li v-for="(link, index) in links" :key="index" @click=" activeIndex = index" :class="{ 'active' : index === activeIndex }">
                <a :href="link.url">{{ link.text }}</a>
            </li>
        </ul>

        <button>GET IN TOUCH NOW</button>
    </nav>
</template>

<script>
export default {
    name: "Navbar",
    data: function() {
        return {
            activeIndex: 0,
            links: [
                {
                    text: 'home',
                    url: '#',
                },
                {
                    text: 'who we are',
                    url: '#',
                },
                {
                    text: 'what we do',
                    url: '#',
                },
                {
                    text: 'where we work',
                    url: '#',
                },
                {
                    text: 'careers',
                    url: '#',
                },
                {
                    text: 'news',
                    url: '#',
                },
            ]
        }
    },
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

nav{
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
        background-color: $yelloworange;
        color: white;
        font-size: 10px;
        padding: 10px;
        border-radius: 25px;
        border-style: none;
        margin-left: 12px;
        cursor: pointer;
        font-weight: 600;
    }
}
        

</style>