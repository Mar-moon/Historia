<script>
    import TheRoom from '../assets/LaHabitación.jpg';
    import Daga from '../assets/daga.png';
    import Libro from '../assets/libro2.png';
    import Tocador from '../assets/tocador.png';
    import Final from './final.svelte';

    let obj_daga = false;
    let obj_libro = false;
    let obj_tocador = false;
    let contador = 0;

    function handleClick(element) {
        console.log(contador + 1);
        if(element === 1 && !obj_daga){
            contador += 1;
            obj_daga = true;
            return;
        }
        if(element === 2 && !obj_libro){
            contador += 1;
            obj_libro = true;
            return;
        }
        if(element === 3 && !obj_tocador){
            contador += 1;
            obj_tocador = true;
        }      
    }
</script>

<main>
    <div class="texto">
        <p><em>¿Qué le pudo haber sucedido?</em></p>
        <br>
        <br>
        <p>Busca los siguientes objetos para descubrir lo que sucedió: El arma de Isa, libro peculiar y el cristal roto.</p>
    </div>
    <div class="middle">
        <div class="hidden-obj">
            <div class="imagen">
                <div class="relativo">
                    <img class="background" src={TheRoom} alt="La habitación">
                    <img class="obj1" src={Daga} alt="Daga" on:click={() => handleClick(1)}>
                    <img class="obj2" src={Libro} alt="Libro" on:click={() => handleClick(2)}>
                    <img class="obj3" src={Tocador} alt="Cristal roto" on:click={() => handleClick(3)}>
                </div>
            </div>
        </div>
        <span class="contador-section">
            <p class="contador">{contador} / 3</p>
            <p class="fd">Fragmentos desbloqueados</p>
        </span>
    </div>
    
    <Final contador={contador}/>
</main>

<style>
    .texto {
        display: flex;
        max-width: 70%;
        flex-direction: column;
        padding: 30px;
        padding-bottom: 0px;
    }
    p {
        text-align: justify;
        font-size: 20px;
    }

    .hidden-obj {
        width: 80%;
    }
    .imagen {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 10px;
        padding-top: 0px;
    }
    .relativo {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 80%;
    }

    .background {
        width: 100%;
        border-radius: 50px;
    }
    .obj1 {
        position: absolute;
        width: 9.2%;
        top: 87.25%;
        left: 26.1%;
        z-index: 1;
        cursor: pointer;
    }
    .obj2 {
        position: absolute;
        width: 11.5%;
        top: 75%;
        left: 68.3%;
        z-index: 1;
        cursor: pointer;
    }
    .obj3 {
        position: absolute;
        width: 19.4%;
        top: 12.1%;
        left: 27.4%;
        z-index: 1;
        cursor: pointer;
    }

    .middle {
        display: flex;
        align-items: center;
        flex-direction: row;
    }
    

    .contador-section {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        width: 20%;
    }
    .contador {
        font-weight: bold;
        padding: 20px;
        background-color: #4d0a8c;
        border-radius: 20px;
        color: #f8f8f8;
    }
    .fd {
        font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
        text-align: center;
        font-family: 'Cinzel Decorative', cursive;
    }

    @media (max-width: 800px) {
        .middle {
            flex-direction: column;
        }
        .hidden-obj {
            width: 90%;
        }
        .relativo {
            width: 100%;
        }
    } 
</style>