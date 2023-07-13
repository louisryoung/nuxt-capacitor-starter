<template>
	<div>
		<h1>Switzerland Time</h1>
		<div>
			🕥 Current time: <b>{{ timeData.datetime }}</b>
			<a @click="$nuxt.refresh()" href="">🔄</a>
		</div>
	</div>
</template>

<script setup>
const { data: timeData } = await useFetch(
	'https://worldtimeapi.org/api/timezone/Europe/Zurich'
);
</script>
