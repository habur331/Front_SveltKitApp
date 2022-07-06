<script>
    import WeatherComponent from "../lib/components/WeatherComponent.svelte";
</script>

<div id="funny-fact" class="card-section">
    <p>
        Funny fact about me - I can predict the weather in Innopolis. Don't you believe it? I'll prove it below.
    </p>

    <WeatherComponent/>

</div>

<style>
    .card-section {
        width: 80%;
        padding: 0 20px 0 20px;
        margin: 20px auto;
        font-size: large;
        border: 1px solid;
        border-radius: 10px;
        display: flex;
        justify-content: center;
    }

    .card-section p {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    #funny-fact {
        display: flex;
        flex-direction: column;
    }
</style>