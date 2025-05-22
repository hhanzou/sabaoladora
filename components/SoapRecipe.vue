<template>
	<UCard variant="outline">
		<template #header>
			<h2 class="text-lg font-semibold">📝 Como fazer sabão caseiro</h2>
		</template>

		<div class="space-y-3 text-sm leading-relaxed text-white">
			<p>Essa é uma receita básica de sabão caseiro com óleo reutilizado:</p>
			<ul class="list-disc pl-5 space-y-1">
				<li>1 litro de óleo de cozinha usado (filtrado)</li>
				<li>130g de soda cáustica (em escamas ou líquida)</li>
				<li>300ml de água (de preferência fria)</li>
			</ul>
			<p><strong>Passo a passo:</strong></p>
			<ol class="list-decimal pl-5 space-y-1">
				<li>Dissolva a soda cáustica na água com cuidado (em local ventilado).</li>
				<li>Adicione o óleo aos poucos, mexendo sempre.</li>
				<li>Misture por 20 a 40 minutos até dar ponto (massa cremosa).</li>
				<li>Despeje em formas e deixe descansar por 24–48h.</li>
				<li>Após isso, corte e deixe curar por 15–30 dias antes de usar.</li>
			</ol>
			<UAlert icon="twemoji:warning" :ui="{ icon: 'size-10' }" variant="outline" color="error" title="Atenção!"
				description="Use luvas, óculos e máscaras. Nunca inale ou toque na soda diretamente." />
		</div>
	</UCard>
</template>
