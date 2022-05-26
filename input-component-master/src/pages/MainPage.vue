<script setup>
import MainFooter from '@/components/MainFooter.vue'
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
		<template #footer><main-footer /></template>
	</wrapper-layout>
</template>
