<script>

    export let visible = false;

</script>

<style>

    .navigation-bar-sticky {
        position: fixed;
        left: 0;
        width: 100%;
        background-color: rgba(235, 213, 179, 0.8);
        margin: 0;
        border-bottom: solid #776b5b;
        z-index: 2;
    }

    .navigation-unordered-list {
        display: flex;
        flex-wrap: nowrap;
        flex-grow: 1;
        flex-direction: row;
        text-align: center;
        justify-content: space-evenly;
        padding: 0;
        margin: 0;
    }

    .navbar-list-item {
        list-style-type: none;
        color: #7E1518;
        flex-grow: 1;
        font-family: 'Kalam', cursive;
        font-size: 2rem;
        font-weight: bold;
        display: flex;
    }

</style>

<div class="navigation-bar-sticky">

    <ul class="navigation-unordered-list">
        <li class="navbar-list-item">Character</li>
        <li class="navbar-list-item">Maps</li>
        <li class="navbar-list-item">Journal</li>
        <li class="navbar-list-item">Gallery</li>
        <li class="navbar-list-item">Bestiary</li>
        <li class="navbar-list-item">Settings</li>
        <li class="navbar-list-item">Account</li>
    </ul>

</div>