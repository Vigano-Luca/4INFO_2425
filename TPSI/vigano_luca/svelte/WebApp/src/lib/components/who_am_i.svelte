<script>
    export let name = "Mario";
    export let surname = "Rossi";
    export let age = 20;
    export let width = 200;
    export let height = 200;
    let src = "https://ichiba-japan.com/cdn/shop/files/scream-tail-plush-paradox-pokemon-plush-pokemon-center-636679_1200x1200.jpg?v=1715439824";
</script>

<h1>Ciao io sono {name} {surname} ed ho {age} anni</h1>
<h4>Sono uno studente di informatica presso l'istituto agnelli a Torino</h4>
<img {src} alt="pokemon plush" width={width} height={height}/>

<style>
    img {
        border-radius: 50%;
    }
</style>