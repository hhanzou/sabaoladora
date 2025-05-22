<template>
	<UCard>
		<div class="space-y-1">
			<p><strong>Sabão:</strong> {{ sabao }} kg</p>
			<p><strong>Soda cáustica:</strong> {{ soda }} g</p>
			<p><strong>Água:</strong> {{ agua }} ml</p>
			<p><strong>Barras estimadas:</strong> {{ barras }} unidade(s) de ~200g</p>
		</div>
	</UCard>
</template>

<script setup lang="ts">
defineProps<{
	mostrar: boolean
	sabao: string
	soda: number
	agua: number
	barras: number
}>()
</script>
