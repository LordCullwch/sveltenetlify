<script>

    import StatButton from "./StatButton.svelte";

    export let secondaryStats = [

        [
            {stat:1, statname: "Alertness"},
            {stat:1, statname: "Athletics"},
            {stat:1, statname: "Awareness"},
            {stat:1, statname: "Pugilism"},
            {stat:1, statname: "Empathy"},
            {stat:1, statname: "Expression"},
            {stat:1, statname: "Intimidation"},
            {stat:1, statname: "Leadership"},
            {stat:1, statname: "Streetwise"},
            {stat:1, statname: "Subterfuge"}

        ],

        [

            {stat:1, statname: "Animal Ken"},
            {stat:1, statname: "Crafts"},
            {stat:1, statname: "Drive"},
            {stat:1, statname: "Etiquette"},
            {stat:1, statname: "Firearms"},
            {stat:1, statname: "Larceny"},
            {stat:1, statname: "Melee"},
            {stat:1, statname: "Performance"},
            {stat:1, statname: "Stealth"},
            {stat:1, statname: "Survival"}

        ],
        [

            {stat:1, statname: "Academics"},
            {stat:1, statname: "Computer"},
            {stat:1, statname: "Finance"},
            {stat:1, statname: "Investigation"},
            {stat:1, statname: "Law"},
            {stat:1, statname: "Medicine"},
            {stat:1, statname: "Occult"},
            {stat:1, statname: "Politics"},
            {stat:1, statname: "Science"},
            {stat:1, statname: "Technology"}

        ]

    ];

</script>


<style>



    .stat-cluster {
        flex-wrap: wrap;
        flex: 1 1 20%;
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


</style>

        {#each secondaryStats as array}
        <div class="stat-cluster">
            {#each array as pack}
                <div class="stat">
                    <StatButton stat="{pack.name}" statname="{pack.statname}" />
                </div>
            {/each}
        </div>
        {/each}