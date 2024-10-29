<script>
    let contador = 0;

    const incrementar = () => {
        contador++;
    }
    const decrementar = () => {
        contador--;
    }


</script>

<h1>{contador}</h1>

<button on:click={incrementar}>Incrementar</button>
<button on:click={decrementar}>Decrementar</button>