<script setup>
import Stat from './components/Stat.vue'
import CitySelect from './components/CitySelect.vue'

const data = {
	label: 'Влажность',
	stat: '90%'
}

const getCity = (city) => {
	console.log(city)
}

</script>

<template>
	<main class="main">
		<Stat v-bind="data" />
		<CitySelect @select-city="getCity" />
	</main>
</template>

<style scoped>
.main {
	padding: 60px 50px;

	background-color: var(--color-bg-main);
	border-radius: 25px;
}
</style>
