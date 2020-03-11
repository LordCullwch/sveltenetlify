<script>

    export let stat = 1;
    export let statname = "";
    
    function increment() {
        if (stat < 8) {
            ++stat
        }
    }

    function decrement() {
        if (stat > 1) {
            --stat
        }
    }




</script>

<style>

    .stat {
        grid-column: auto;
        list-style-type: none;
        display: inline-flex;
        padding: 1px;
        margin: 1.5px 1px 1.5px 1px;
        font-size: 0.7rem;
        font-family: 'Alegreya', serif;
        background-color: rgba(235, 213, 179, 0.7);
        flex: 1 1 5%;
        justify-content: space-evenly;
    }

    .stat-number {
        justify-content: center;
        font-weight: bold;
        color: #7E1518;
    }


    p {
        display: inline-flex;
        margin: 0;
        padding: 0;
        justify-content: center;
    }


    .incr-decr {
        display: inline-flex;
        font-weight: bold;
        color: #7E1518;
        flex-direction: column;
    }


</style>



<label class="stat">



    <p class="incr-decr" on:click={decrement}>-</p>
    <p class="incr-decr" on:click={increment}>+</p>
    <p>|{statname}:</p><p class="stat-number"><strong>{stat}</strong></p>



</label>