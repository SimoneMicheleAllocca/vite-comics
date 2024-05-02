<script>
export default{
    data () {
        return{

        }
    }
}</script>

<template>

    <section class="backg">
        <h2>Content goes here</h2>
    </section>
    
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;

.backg{
    padding: 5rem 0;
    background-color: black;

    @include flex(row, center, center);

    h2{
        color: white;
    }
}
</style>