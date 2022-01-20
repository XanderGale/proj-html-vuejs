<template>
    <footer>
        <img src="../assets/images/logo_seo_1x.png" alt="Seo Logo">

        <div class="navfooter">
            <ul>
                <li v-for="(link, index) in linksArray" :key="index" @click=" activeIndex = index" :class="{ 'active' : index === activeIndex }">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </ul>
        </div>

        <span class="copyright">Copyright 2012 - 2020 | Avada theme by <a href="#">theme fusion</a> | All rights reserved | Powered by <a href="#">wordpress</a></span>
    
        <div class="socials">
            <ul>
                <li v-for="(social, index) in socials" :key="index">
                    <a :href="social.link">
                        <i :class="social.icon"></i>
                    </a>
                </li>
            </ul>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: ['linksArray', 'activeIndex'],
    data: function(){
        return{
            socials: [
                {
                    icon: 'fab fa-facebook-f',
                    link: '#',
                },
                {
                    icon: 'fab fa-instagram',
                    link: '#',
                },
                {
                    icon: 'fab fa-twitter',
                    link: '#',
                },
                {
                    icon: 'fab fa-youtube',
                    link: '#',
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

    footer{
        padding: 50px;
        background-color: $alabaster;
        color: $regentgray;

        display: flex;
        flex-flow: column nowrap;
        justify-content: center;
        align-items: center;
        .navfooter{
            text-transform: capitalize;
            margin: 50px auto;
            ul{
            list-style-type: none;
                li{
                    display: inline-block;
                    margin: auto 19px;
                    cursor: pointer;
                    &:hover,
                    &.active{
                        color: $yelloworange;
                    }
                    a{
                        text-decoration: none;
                        color: inherit;
                        text-transform: inherit;
                    }
                }
            }
        }
        .copyright{
            font-size: 0.7rem;
            a{
                text-decoration: none;
                color: black;
                text-transform: capitalize;
            }
        }
        .socials{
            margin: 35px auto;
            ul{
                list-style-type: none;
                li{
                    display: inline-block;
                    margin: auto 5px;
                    cursor: pointer;
                    &:hover,
                    &:active{
                        color: $yelloworange;
                    }
                    a{
                        text-decoration: none;
                        color: inherit;
                    }
                }
            }
        }
    }

</style>
