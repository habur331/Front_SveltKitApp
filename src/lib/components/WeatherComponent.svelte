<script lang="ts">
    import {onMount} from "svelte";

    let weatherToday: string = "Predicting...";
    let weatherTomorrow: string = "Predicting...";

    async function fetchWeather() {
        try {
            const res = await fetch('https://weatherdbi.herokuapp.com/data/weather/innopolis') as Response;
            const json = await res.json();

            return {
                today: json.currentConditions,
                tomorrow: json.next_days[0],
            }

        } catch {
            weatherToday = "I have headache. Try to ask me later";
            weatherTomorrow = "I have headache. Try to ask me later";
        }

        return null;
    }

    onMount(() => {
        fetchWeather().then(weather => {
            if (weather != null) {
                weatherToday = 'Now it is ' + weather.today.temp.c + ' degrees Celsius and ' + weather.today.comment;
                weatherTomorrow = 'Tomorrow will be ' + weather.tomorrow.max_temp.c + ' degrees Celsius and ' + weather.tomorrow.comment;
            }
        });
    });
</script>

<div id="weather-section">
    <div class="weather-sub-div">
        <h4> Weather Today:</h4>
        <p class="weather-paragraph" id="weather-today">
            {weatherToday}
        </p>
    </div>
    <div class="weather-sub-div">
        <h4> Weather Tomorrow:</h4>
        <p class="weather-paragraph" id="weather-tomorrow">
            {weatherTomorrow}
        </p>
    </div>
</div>


<style>
    #weather-section {
        display: flex;
    }

    .weather-sub-div h4 {
        display: flex;
        justify-content: center;
    }

    .weather-sub-div {
        margin: auto;
    }

    .weather-paragraph {
        display: flex;
        justify-content: center;
    }
</style>