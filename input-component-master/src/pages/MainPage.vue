<script setup>
import MyLogo from '@/components/Mylogo.vue'
import SubTitle from '@/components/SubTitle.vue'
import InputLayout from '@/layouts/InputLayout.vue'
import WrapperLayout from '@/layouts/WrapperLayout.vue'
</script>
<template>
	<wrapper-layout>
		<template #logo><my-logo /></template>
		<template #title><sub-title /></template>
		<template #body><input-layout /></template>
	</wrapper-layout>
</template>
<style scoped></style>
