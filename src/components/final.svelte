<script>
    import Raquel from '../assets/Raquel.png';
    import Raquel1 from '../assets/Raquel1.png';
    import Raquel2 from '../assets/Raquel2.png';
    import Raquel3 from '../assets/Raquel3.png';
    import QR from '../assets/qr.png';
    import Source from '../assets/Inspiro.png';
    import Spotify from '../assets/Spoti.png';

    export let contador = 0;
</script>

<main>
    <div class="texto">
        <p><b>Perspectiva de Isa</b></p>
        <div class="parrafo">
            <p>
                Nerviosa y algo agitada, Isa entró a su habitación y cerró la puerta detrás de ella.
                La tenue luz que llegaba del pasillo desapareció y la estancia quedó apenas en penumbra,
                debido al brillo de la luna que entraba por su ventana.
                Se recargó sobre la puerta, cerró los ojos soltando un profundo suspiro.
            </p>
            <p>
                Lentamente los abrió, tomó la daga de su cinturón y examinó su filo con tristeza sopesando lo que tenía planeado hacer.
            </p>
        </div>
        <!-- Daga -->
        {#if contador >= 1}
            <div class="parrafo">
                <p>
                    Levantó su mirada hacia las puertas del balcón y se encaminó a correr las cortinas. 
                    Pasó frente a su espejo del tocador, y algo le llamó la atención por el rabillo del ojo. 
                    Frente a su reflejo se observó así misma con detenimiento, era ella, pero no se reconocía. 
                    Sí, sus ojos eran los mismos… ¿Eran los mismos? 
                    Por una fracción de segundo le pareció que tenían un tono rojizo, pero debió ser su imaginación, 
                    no se detuvo mucho en eso ya que le costaba mantener el contacto visual, como si se mirara con desprecio.
                </p>
            </div>
            <div class="parrafo">
                <p>
                    Tenía la daga fuertemente apretada contra su pecho, pero en un grito de frustración la levantó y la clavó astillando el tocador. 
                    Bajó la mirada y se hundió entre sus brazos.
                </p>
                <p>
                    De repente una voz rompió el silencio llamando su nombre. 
                    Isa se levantó bruscamente con la daga nuevamente en su mano y se giró hacia su habitación en pose amenazante. 
                    No había nadie, pero la voz continuó, repitiendo “No te puedes deshacer de mí,” una y otra vez.
                </p>
                <p>
                    “¿Dónde estás?” Gritó Isa, sintió un escalofrío que le recorrió la espalda, obligándola a volver la vista al espejo, 
                    donde descubrió con horror a la dueña de la voz que la observaba desde el otro lado del cristal. Era ella misma.
                </p>
            </div>
        {/if}
        <!-- Libro -->
        {#if contador >= 2}
            <div class="parrafo">
                <p>
                    Un estruendo la sacó de su estado de conmoción, el espejo se resquebrajó y la Isa del espejo desapareció, 
                    pero su voz aun inundaba el lugar. Isa supuso que sería inutil intentar atacar cuerpo a cuerpo, 
                    por lo que tomó uno de sus libros sobre maldiciones. 
                    Recorrió las páginas rápidamente, sus manos temblaban, pero sabía en dónde buscar, inmediatamente encontró la página, 
                    no obstante en ese momento el libro comenzó a arder y lo dejó caer.
                </p>
            </div>
        {/if}
        <!-- Tocador -->
        {#if contador >= 3}
            <div class="parrafo">
                <p>
                    A su alrededor se formó un torbellino de humo que la desorientó. 
                    Rostros, no, su propio rostro se formaba en las paredes de humo y volaba en su dirección atravesando su cuerpo causándole dolor. 
                    Isa trataba de golpearlos, pero era en vano.
                </p>
            </div>
            <div class="parrafo">
                <p>
                    A su lado y de la nada, se formó un brillante portal. El humo parecía ser atraído formando un pequeño vórtice, 
                    el cual también jalaba a Isa. El dolor le hizo perder el equilibrio, cayó y fue absorbida por el portal junto con el humo. 
                    Ambos desaparecieron junto con el portal y el caos que se había armado.
                </p>
            </div>
            <div class="parrafo">
                <p>
                    La habitación volvió a quedar en silencio y a penas en penumbra.
                </p>
            </div>
        {/if}
    </div>
    <div class="imagen">
        {#if contador == 0}
            <img src={Raquel} alt="MaxF">
        {:else if contador == 1}
            <img src={Raquel1} alt="MaxF">
        {:else if contador == 2}
            <img src={Raquel2} alt="MaxF">
        {:else}
            <img src={Raquel3} alt="MaxF">
        {/if}
    </div>
</main>
{#if contador >= 3}
    <div class="images">
        <img src={QR} alt="Código QR">
        <img src={Source} alt="Inspirado en...">
        <img src={Spotify} alt="Spotify">
    </div>
{/if}

<style>
    main {
        display: flex;
        flex-direction: row-reverse;
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
    .parrafo {
        margin: 20px;
    }
    .parrafo p {
        margin: 0;
    }
    .images {
        display: flex;
        flex-direction: row;
        margin: 10px;
        padding: 10px;
        align-items: center;
        justify-content: center;
    }
    .images img {
        max-width: 200px;
        margin: 5px;
    }
    @media (max-width: 700px) {
        img {
            max-width: 170px;
        }
        .images img {
            max-width: 140px;
            margin: 5px;
        }
    }
</style>