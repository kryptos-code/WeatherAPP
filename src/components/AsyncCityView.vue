<template>
    <div>

    </div>
</template>

<script setup>

import axios from "axios";
import { useRoute } from "vue-router";

const weatherApiKey = "6909abb863a9067ca0545a83bbb20953";
const route = useRoute();
const getWeatherData = async () => {
    try {
        const weatherData = await axios.get(`https://api.weatherstack.com/current?access_key=${weatherApiKey}&query=${route.query.lat},${route.query.lng}}`);
    } catch (error) {
        console.log(error);
    }
};
</script>
