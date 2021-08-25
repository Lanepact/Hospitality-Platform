<template>
    <section id="information">
    <div class="container">
        <h2>Sheraton Hotels</h2>
        <h3>AT THE HEART OF COMMUNITIES FOR OVER 80 YEARS</h3>
        <p>Bringing people together is what we’ve done since opening our first Sheraton in 1937. Now we’re deeply rooted in over 400 communities across the globe. We are proud to act as a point of connection for millions of travelers, many just like you. Welcome.</p>

    </div>
</section>
</template>

<script>
export default{
    name:'Information',
}
</script>

<style scoped>
#information{
    padding: 3% 15% 7%;
    text-align: center;
}
@media (max-width: 320px){
    #information{
        padding: 0%;
        padding-top: 40%;
        padding-bottom: 5%;
        background-color: white;
        text-align:left;
    }
}

/* tablets */
@media (max-width: 800px){
    #information{
        padding: 20%;
        padding-top: 55%;
        padding-bottom: 5%;
        background-color: white;
        text-align: left;
    }
}
</style>