<script>

    export let name = "Health";
    export let value = 12;
    export let max= 24;
    export let id= "health";

</script>

<style>
    .stat-resource {
        flex-wrap: nowrap;
        flex-grow: 1;
        display: inline-flex;
        flex-direction: column;
        padding: 1px;
        margin: 2%;
        background-color: rgba(207, 173, 116, 0.8);
    }

    .resource-progress-bar {
        display: inline-flex;
        width: 100%;
        margin: 1%;
        border: solid rgba(130, 103, 56, 0.8) 1px;
        border-radius: 5px;
        background-color: rgba(218, 177, 113, 0.7);
        overflow: hidden;
    }

    #health::-webkit-progress-bar {
        background-color: transparent;

    }

    #health::-webkit-progress-value {
        background-color: rgba(187, 0, 14, 0.8);
    }

    #health {

    }

    #congruence::-webkit-progress-bar {
        background-color: transparent;

    }

    #congruence::-webkit-progress-value {
        background-color: rgba(181, 126, 220, 0.8);
    }

    #congruence {

    }

    #armour::-webkit-progress-bar {
        background-color: transparent;

    }

    #armour::-webkit-progress-value {
        background-color: rgba(54, 69, 79, 0.8);
    }

    #armour {

    }

    #willpower::-webkit-progress-bar {
        background-color: transparent;

    }

    #willpower::-webkit-progress-value {
        background-color: rgba(78, 78, 177, 0.8);
    }

    #willpower {

    }

    /*Description & xp.*/

    .description {
        resize: none;
        background-color: rgba(218, 177, 113, 0.7);
        border: solid rgba(130, 103, 56, 0.8) 1px;
        border-radius: 5px;
        font-size: small;
        min-height: 100px;
    }

    .resource-progress-bar {
        display: inline-flex;
        width: 100%;
        margin: 1%;
        border: solid rgba(130, 103, 56, 0.8) 1px;
        border-radius: 5px;
        background-color: rgba(218, 177, 113, 0.7);
        overflow: hidden;
    }
</style>



<label>{name}</label>
<progress class="resource-progress-bar" id="{id}" value="{value}" max="{max}">{name}</progress>
