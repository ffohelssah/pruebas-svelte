<script>
    const personajes = ["Nico", "Chopper", "Franky", "Monkey", "Nami"];
    let displayEstilo = "none";
    const modal = document.getElementById("myModal");
    const img = document.getElementById("myImage");
    const modalImg = document.getElementById("modalImage");
    const captionText = document.getElementById("caption");
    const closeModal = document.getElementById("closeModal");

    img.onclick = function () {
        modal.style.display = "block";
    };

    // Cuando el usuario hace clic en <span> (x), cerrar la modal
    closeModal.onclick = function () {
        modal.style.display = "none";
    };
</script>

<div class="contenedorImg">
    {#each personajes as personaje}
        <img src="../../public/img/foto{personaje}.png" alt={personaje} />
    {/each}
</div>

<div id="myModal" class="modal" style="display: {displayEstilo};">
    <span class="close" id="closeModal">&times;</span>
    <img class="modal-content" id="modalImage" alt="fotoPersonaje" />
    <div id="caption"></div>
</div>

<style>
    .contenedorImg {
        width: 100vw;
        display: flex;
        gap: 20px;
        align-items: center;
        justify-content: center;
    }

    img {
        width: 15%;
        cursor: pointer;
    }

    .modal {
        position: fixed;
        z-index: 1; /* Enfrente de otros elementos */
        left: 0;
        top: 0;
        width: 100%; /* Pantalla completa */
        height: 100%; /* Pantalla completa */
        overflow: auto; /* Habilitar scroll si es necesario */
        background-color: rgba(0, 0, 0, 0.8); /* Fondo oscuro */
    }

    .modal-content {
        margin: auto;
        display: block;
        max-width: 80%; /* Ajustar el tamaño máximo de la imagen */
    }

    .close {
        position: absolute;
        top: 10px;
        right: 25px;
        color: white;
        font-size: 35px;
        font-weight: bold;
        cursor: pointer;
    }
</style>
