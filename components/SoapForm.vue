<template>
	<div class="space-y-4">
		<UCard variant="outline" class="bg-pink-100 text-pink-900">
			<div class="leading-relaxed">
				<p>
					Aqui você pode calcular quantas barras de sabão podem ser feitas com óleo usado.
					Basta inserir a quantidade de litros e clicar em <strong>Calcular</strong>.
					O sistema estimará o rendimento, quantidade de soda cáustica e água.
				</p>
			</div>
		</UCard>

		<UFormField label="Óleo Usado" help="Insira a quantidade de óleo usado que você deseja calcular.">
			<UInput v-model="localLitros" type="number" min="0.1" step="0.1" placeholder="Litro de Óleo" size="xl" />
		</UFormField>

		<UButton icon="twemoji:soap" label="Calcular" trailing
			class="font-bold rounded-full bg-pink-300 disabled:bg-pink-300 hover:bg-pink-400"
			@click="$emit('update:mostrar', true)" :disabled="litros <= 0" size="xl" />
	</div>
</template>

<script setup lang="ts">
const props = defineProps<{
	litros: number
	mostrar: boolean
}>()

const emit = defineEmits<{
	(e: 'update:litros', value: number): void
	(e: 'update:mostrar', value: boolean): void
}>()

const localLitros = ref(props.litros)

watch(localLitros, (value) => {
	emit('update:litros', value)
})
</script>
