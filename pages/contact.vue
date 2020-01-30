<template>
<page>
    <navBar/>
    <div>
        <h1>Kontakta oss på email@gmail.com</h1>
        
    </div>
</page>
</template>

<script>
import navBar from '@/components/nav';
// import footerBar from '@/components/footer';
export default {
    data() {
        return {

        }
    },
    components: {
        navBar,
        // footerBar
    },
}
</script>

<style scoped>
@media (max-width: 780px) {
h1 {
    margin-top: 2em;
    text-align: center;
    font-size: 1em;
    font-weight: 500;
    color: white;
}
}
@media (min-width: 780px) {
h1 {
    margin-top: 2em;
    text-align: center;
    font-size: 1.5em;
    font-weight: 500;
    color: white;
}

}

</style>