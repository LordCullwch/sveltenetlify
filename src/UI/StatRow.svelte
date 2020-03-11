<script>

    import StatButton from "./StatButton.svelte";

    export let primaryStats = [

        [
            {stat:1, statname: "Strength"},
            {stat:1, statname: "Dexterity"},
            {stat:1, statname: "Stamina"}

        ],

        [

            {stat:1, statname: "Manipulation"},
            {stat:1, statname: "Charisma"},
            {stat:1, statname: "Composure"}

        ],
        [

            {stat:1, statname: "Intelligence"},
            {stat:1, statname: "Wits"},
            {stat:1, statname: "Resolve"}

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

</style>

{#each primaryStats as array}
    <div class="stat-cluster">
        {#each array as pack}
            <div class="stat">
                <StatButton stat="{pack.name}" statname="{pack.statname}" />
            </div>
        {/each}
    </div>
{/each}