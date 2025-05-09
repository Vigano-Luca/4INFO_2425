<script>
    let contatore = 0;
    let contatore_2 = 0;
    import Counter from "../../lib/components/counter.svelte";
    import DoubleCounter from "../../lib/components/double_counter.svelte";
    import {store_counter1} from "../../lib/js/store";
    import {store_counter2} from "../../lib/js/store";
    let numeri = [1, 7, 3, 4, 5, 6, 8, 9, 10];
    function gestisci_evento(evento) {
        alert(`${evento.detail.tipo} -- ${evento.detail.valore}`);
    }
    $: doppio = contatore * 2;
</script>

<h1>
    Pagina Counter
</h1>

<h2 class={contatore < 5 ? "rosso" : "verde"}>Il valore del contatore vale: {contatore}</h2>

<h2>Il doppio vale {doppio}</h2>

<Counter bind:counter={contatore} on:contatore={gestisci_evento}/>

<h2>
    Il valore del contatore 2 vale: {contatore_2}
</h2>

<DoubleCounter bind:counter={contatore_2} />



<ul>
  {#each numeri as numero, indice}
    <li>numeri[{indice}]:{numero}</li>
  {/each}
</ul>




<style>
    .rosso {
        color: red;
    }

    .verde {
        color: green;
    }
</style>