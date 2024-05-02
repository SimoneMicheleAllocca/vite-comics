<script>
export default{
    data () {
        return{
            menu: [
                {
                    title:"Characters",
                    isActive: false,
                },
                {
                    title:"Comics",
                    isActive: true,
                },
                {
                    title:"Movies",
                    isActive: false,
                },
                {
                    title:"Tv",
                    isActive: false,
                },
                {
                    title:"Games",
                    isActive: false,
                },
                {
                    title:"Collectibles",
                    isActive: false,
                },
                {
                    title:"Videos",
                    isActive: false,
                },
                {
                    title:"Fans",
                    isActive: false,
                },
                {
                    title:"News",
                    isActive: false,
                },
                {
                    title:"Shop",
                    isActive: false,
                },

            ]
        }
    }
}</script>

<template>

    <header>
        <div class="header-box">
        <div class="header-logo">
            <img src="../assets/img/dc-logo.png" alt="logo">
        </div>
        <ul class="nav">
            <li v-for="item in menu">
            <a href="" :class="{active : item.isActive}">{{ item.title }}</a>
        </li>
          
        </ul>
    </div>
    </header>

</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header{
    .header-logo{
        margin-top: 50px;
        margin-left: 200px;
    } 
    ul {

        @include flex(row, right, right);
        list-style-type: none;
        gap: 1rem;
        margin-right: 50px;

        a{
            padding: 20px 16px;
            text-decoration:none;
            color: $text-color;
            display: inline-block;p

            &:hover{
                color: $primary-color;
            }

            &.active{
                border-bottom: 7px $primary-color solid;
            }
        }
    }   
    
}
</style>