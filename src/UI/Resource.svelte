<script>

    export let name = "placeholder";
    export let max = "100";
    export let value = "25";
    export let abbr = "placeholder";
    export let id = "placeholder";

</script>
<style>

    #corpus::-webkit-progress-bar {
        background-color: transparent;
        border-radius: 5%;
    }

    #animus::-webkit-progress-bar {
        background-color: transparent;
        border-radius: 5%;
    }

    #spiritus::-webkit-progress-bar {
        background-color: transparent;
        border-radius: 5%;
    }

    #corpus::-webkit-progress-value {
        border: 0;
        height: 50px;
        width: 50px;
        background-color: #186A3B;
    }

    #animus::-webkit-progress-value {
        border: 0;
        height: 50px;
        width: 50px;
        background-color: #641E16;
    }

    #spiritus::-webkit-progress-value {
        border: 0;
        height: 50px;
        width: 50px;
        background-color: #9B59B6;
    }

    .magic-resource-progress-bar {
        transform: rotate(270deg);
        border: 0;
        border-radius: 100%;
        height: 40px;
        width: 40px;
        background-color: rgba(119,136,170,0.7);
        overflow: hidden;
    }

    #corpus {
        background: url("build/ossuary-original.jpg");
    }

    #animus {
        background: url("build/ossuary-original.jpg");
    }

    #spiritus {
        background: url("build/ossuary-original.jpg");
    }

    .stat-caster {
        list-style-type: none;
        display: inline-flex;
        padding: 1px;
        margin: 1.5px 1px 1.5px 1px;
        font-size: 0.7rem;
        font-family: 'Alegreya', serif;
        background-color: rgba(235, 213, 179, 0.7);
        flex: 1 1 5%;
    }

    .stat-caster-secondary {
        list-style-type: none;
        display: inline-flex;
        padding: 1px;
        margin: 1.5px 1px 1.5px 1px;
        font-size: 0.7rem;
        font-family: 'Alegreya', serif;
        background-color: rgba(235, 213, 179, 0.7);
        flex: 1 1 5%;
        border: solid #DAB171 2.5px;
    }

    .stat-caster-container {
        display: inline-flex;
        flex-direction: column;
        padding: 1px;
        margin: 1px;
        background-color: rgba(218, 177, 113, 0.9);
    }



    .stat-caster {
        list-style-type: none;
        display: inline-flex;
        padding: 1px;
        margin: 1.5px 1px 1.5px 1px;
        font-size: 0.7rem;
        font-family: 'Alegreya', serif;
        background-color: rgba(235, 213, 179, 0.7);
        flex: 1 1 5%;
    }

    .stat-caster-secondary {
        display: inline-flex;
        padding: 1px;
        margin: 1.5px 1px 1.5px 1px;
        font-size: 0.7rem;
        font-family: 'Alegreya', serif;
        background-color: rgba(235, 213, 179, 0.7);
        flex: 1 1 auto;
        border: solid #DAB171 2.5px;
    }

    .stat-caster-container {
        display: inline-flex;
        flex-direction: column;
        padding: 1px;
        margin: 1px;
        background-color: rgba(218, 177, 113, 0.9);
    }


    .magic-resource-progress-bar {
        transform: rotate(270deg);
        border: 0;
        border-radius: 100%;
        height: 40px;
        width: 40px;
        background-color: rgba(119,136,170,0.7);
        overflow: hidden;
    }





</style>





    <ul class="stat-caster-container">
        <li class="stat-caster">{name}</li>
        <li class="stat-caster-secondary"><progress value="{value}" max="{max}" id="{id}" class="magic-resource-progress-bar"></progress></li>
        <li class="stat-caster">{abbr}</li>
    </ul>


