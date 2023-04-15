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
        if(!obj_tocador){
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

    .imagen {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 20px;
        padding-top: 0px;
    }
    .relativo {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 85%;
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
    }
    .obj2 {
        position: absolute;
        width: 11.5%;
        top: 75%;
        left: 68.3%;
        z-index: 1;
    }
    .obj3 {
        position: absolute;
        width: 19.4%;
        top: 12.1%;
        left: 27.4%;
        z-index: 1;
    }
</style>