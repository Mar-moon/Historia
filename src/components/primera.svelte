<script>
    import MaxF from '../assets/MaxF.png'
</script>

<main>
    <div class="texto">
        <p><b>Perspectiva de Adam</b></p>
        <p>
            Muy adentrada la noche, Adam despertó sobresaltado de una pesadilla, no pudo recordar de qué trataba, pero solo sabía que Isa estaba en ella.
             El silencio inundaba su cuarto, pero los latidos de su corazón retumbaban en sus oídos.
        </p>
        <p>
            Se levantó agitado de su cama, guiándose a través de la habitación gracias a la luz que entraba por la cristalera del balcón.
             Abrió sus puertas, el frío aire nocturno acarició su rostro y su mirada fue instintivamente hacia la torre contigua donde se encontraba la habitación de Isa.
        </p>
        <p>
            La noche era tranquila, soltó un largo suspiro y justo cuando estaba a punto de regresar al interior,
             un haz brillante de luz rojiza salió del interior de la habitación de su amiga.
        </p>
        <p>
            “Isa,” murmuró preocupado. Salió de su habitación con paso apresurado, su corazón latía aún con más fuerza.
        </p>
        <p>
            Cruzó los pasillos a oscuras, pero sabía perfectamente el camino.
        </p>
        <p>
            Se detuvo frente al dormitorio y tocó la puerta impacientemente, pero nadie respondió.
        </p>
        <p>
            “¡Isa! ¡Isa!,” Llamó su nombre tocando nuevamente, pero seguía sin haber respuesta.
        </p>
        <p>
            Desesperado, le advirtió que iba a entrar.
             Al hacer el intentó se percató de que la puerta estaba bloqueada desde adentro, no solo con el pestillo, el cual deshizo con un encantamiento sencillo, también había una estantería obstruyendo el paso.
        </p>
        <p>
            Al entrar descubrió que la habitación estaba hecha un caos, libros y papeles esparcidos por el suelo.
             Había cristales rotos dispersos por la habitación, algunos pertenecientes a cuadros y otros de botellas de pociones.
              Parecía como si hubiera habido una pelea, pero sin rastro de Isa, solo un <b>espejo roto</b>, un <b>libro</b>, que a diferencia del
               resto estaba quemado en el centro, y su <b>daga</b>, sin ninguna señal de haber sido usada.
        </p>
    </div>
    <div class="imagen">
        <img src={MaxF} alt="MaxF">
    </div>
</main>

<style>
    main {
        display: flex;
        flex-direction: row;
    }
    .texto {
        display: flex;
        flex-direction: column;
        padding: 30px;
    }
    p {
        text-align: justify;
        font-size: 20px;
    }
    .imagen {
        padding: 30px;
    }
    img {
        max-width: 350px;
    }

    @media (max-width: 700px) {
        img {
            max-width: 170px;
        }
    }
</style>