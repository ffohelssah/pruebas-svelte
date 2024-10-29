<script>
    let classMode = 'light';
    let btnText = 'Dark'

    const switchMode = () => {
        if (classMode == 'light') {
            classMode = 'dark'
            btnText = 'Light'
        } else {
            classMode = 'light'
            btnText = 'Dark'
        }
    }
</script>

<div class="contenedor {classMode}">

    <p>Lorem fistrum tiene musho peligro diodenoo sexuarl se calle ustée a wan fistro fistro fistro. Me cago en tus muelas benemeritaar condemor pupita amatomaa me cago en tus muelas fistro a peich ahorarr. Ese hombree quietooor ese que llega quietooor.</p>

</div>
<button on:click={switchMode}>Cambiar a {btnText}</button>

<style>
    .contenedor{
        width: 250px;
        height: 500px;
    }

    .light{
        background-color: beige;
        color: brown;
    }

    .dark{
        background-color: brown;
        color: beige;
    }
</style>