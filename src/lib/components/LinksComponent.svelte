<div id="links">
    <h1 style="grid-row-start: 1; grid-column-start: 2" class="links-header">Links</h1>

    <a style="grid-row-start: 2; grid-column-start: 1" href=https://github.com/habur331>
        <img alt="github.com" class="icon" src="./git-refactor.png">
    </a>

    <a style="grid-row-start: 2; grid-column-start: 3" href=https://vk.com/haburg>
        <img alt="vk.com" class="icon" src="./vk-icon.png">
    </a>
</div>

<style>
    #links {
        margin: 20px;
        display: grid;
        align-items: center;
        justify-items: center;
        grid-template-rows: 2fr 3fr;
        grid-template-columns: 1fr 1fr 1fr;
    }

    .icon {
        width: 100px;
        height: 100px;
        margin: auto;
        display: block;
    }

    .icon:hover {
        width: 105px;
        height: 105px;
    }
</style>