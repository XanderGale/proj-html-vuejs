<template>
    <header>
        <div class="container">
            <div class="inner-header-content">
                <h2>SEM Campaigns Made Simple With Avada</h2>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus eu ornare erat. Curabitur pulvinar elit.</p>
                
                <button class="custom-btn bg-yelloworange">Buy avada now</button>

                <button class="custom-btn bg-purpleheart">Contact us</button>

            </div>
        </div>
    </header>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

    header{
        background-image: url('../assets/images/1-hero-image.png');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        padding: 20px 0;
        color: white;
        .inner-header-content{
            width: 50%;
            margin: 200px 0;
            h2{
                font-size: 2.4rem;
            }
            p{
                margin: 15px 0;
            }
            button{
                margin-right: 20px;
                padding: 12px 15px;
            }
        }
    }

</style>