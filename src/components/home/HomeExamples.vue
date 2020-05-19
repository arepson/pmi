<template>
	<Section dots="true">
		<h2 class="container text-center">
      7 Prinsip Dasar 
    </h2>
    <p class="lead text-center container-md">
    	Palang Merah dan Bulan Sabit Merah Internasional
    </p>

		<div class="home-examples mb-x2">
			<Examples />
		</div>

    <p class="home-links text-center ">
      <g-link  to="/laman/" class="button primary button--large">
        Indeks Laman
      </g-link>
    </p>
	</Section>
</template>

<script>
import Examples from '~/components/Examples.vue'
export default {
	components: {
		Examples
	}
}
</script>

<style>
.home-examples {
	margin: 0 auto;
	max-width: 960px;
}
</style>
