<script>
    import Title from '../components/title.svelte'
    import Primera from '../components/primera.svelte';
    import Find from '../components/find.svelte';
</script>

<main>
    <div class="content">
        <Title></Title>
        <div class="first">
            <Primera></Primera>
        </div>
    </div>
    <div class="game">
        <Find></Find>
    </div>
    <div class="footer">
        <h5 class="uno">Mariana Jiménez</h5>
        <h5 class="dos">Fabian Jiménez</h5>
        <br>
        <br>
        <br>
    </div>
</main>


<style>
    * {
        color: #e3e3e3;
    }
    main {
        background-color: #e3e4ff;
        background: linear-gradient(to bottom, #725285, #bf81dc);
    }
    .content {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
    .first {
        display: flex;
        align-items: center;
        justify-content: center;
        min-width: none;
    }
    .game {
        min-width: none;
    }
    .footer {
        background-color: #c8bae7;
        padding: 20px;
    }
    h5 {
        font-size: 25px;
        margin: 0px;
        font-weight: 100;
        color: #3e3e3e !important;
    }
</style>