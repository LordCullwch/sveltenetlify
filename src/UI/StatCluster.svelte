<script>

    import StatButton from "./StatButton.svelte";

    export let magicStats = [

        {
            statname:"Create",
            stat: 1
        },

        {
            statname:"Analyse",
            stat: 1
        },

        {
            statname:"Destroy",
            stat: 1
        },

        {
            statname:"Admix",
            stat: 1
        },

        {
            statname:"Transform",
            stat: 1
        },

    ]

</script>

<style>

    .stat-cluster {
        flex-wrap: nowrap;
        flex-grow: 1;
        display: inline-flex;
        flex-direction: column;
        padding: 1px;
        margin: 1px;
        background-color: rgba(218, 177, 113, 0.9);
    }

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
    }

    .plus-minus {
        background-color: transparent;
        border: 0;
        padding: 0;
        margin: 0 2px;
        -webkit-appearance: push-button;
        height: 10%;
        width: 10%;
    }

    .description {
        resize: none;
        background-color: rgba(218, 177, 113, 0.7);
        border: solid rgba(130, 103, 56, 0.8) 1px;
        border-radius: 5px;
        font-size: small;
        min-height: 100px;
    }


</style>


<ul class="stat-cluster">
    {#each magicStats as array}
        <li class="stat"><StatButton stat="{array.stat}" statname="{array.statname}" /></li>
    {/each}
</ul>