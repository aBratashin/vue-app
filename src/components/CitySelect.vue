<script setup>
import Button from './Button.vue'
import IconLocation from '../icons/IconLocation.vue'

const emit = defineEmits({
	selectCity: (city) => city
})

const select = () => {
	emit('selectCity', 'London')
}

</script>

<template>
	<Button @click="select">
		<IconLocation />
		Изменить город
	</Button>

	<div>
		<input class="input" type="text" placeholder="Введите город" />
		<Button>Сохранить</Button>
	</div>
</template>

<style scoped>
.input {
	padding: 15px 18px;

	color: #3f4958;
	font-size: 18px;

	background-color: var(--color-bg-card);
	border: none;
	outline: none;
	border-radius: 10px;
}
</style>
