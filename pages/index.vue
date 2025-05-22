<script setup lang="ts">
import { ref, computed } from 'vue'
import SoapForm from '~/components/SoapForm.vue'
import SoapResult from '~/components/SoapResult.vue'
import SoapBenefits from '~/components/SoapBenefits.vue'
import SoapRecipe from '~/components/SoapRecipe.vue'

const litros = ref(1)
const mostrar = ref(false)

const sabao = computed(() => (litros.value * 1.1).toFixed(2))
const soda = computed(() => Math.round(litros.value * 130))
const agua = computed(() => Math.round(litros.value * 300))
const barras = computed(() => Math.floor((litros.value * 1.1 * 1000) / 200))
</script>

<template>
	<div class="p-6 space-y-8">
		<UCard variant="outline">
			<template #header>
				<h1 class="text-xl font-bold">🧼 Calculadora de Sabão Caseiro</h1>
			</template>

			<div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-start">
				<SoapBenefits />
				<div class="space-y-4">
					<SoapForm :litros="litros" :mostrar="mostrar" @update:litros="litros = $event"
						@update:mostrar="mostrar = $event" />
					<SoapResult :mostrar="mostrar" :sabao="sabao" :soda="soda" :agua="agua" :barras="barras" />
				</div>
			</div>
		</UCard>

		<SoapRecipe />
	</div>
</template>
