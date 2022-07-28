<template>
	<div class="logo">
		<div class="inner">
			<div class="csgo">
				Counter-Strike<br>
				Global Offensive
			</div>

			<img class="CSC" :src="require('../../../img/csc/csc-logo.png')" alt="">

			<div class="Counter-Strike Confederation">
				Counter-Strike Confederation
			</div>

			<div v-if="seriesName.length === 1 || seriesName.length === 3" class="meta">
				<div>{{ seriesName[0] }}</div>
				<div class="center">{{ seriesNumber || (seriesName.length === 1 ? seriesName[0] : seriesName[1]) }}</div>
				<div>{{ seriesName[2] }}</div>
			</div>
		</div>
	</div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
	computed: {
		...mapGetters([
			'seriesName',
			'seriesNumber',
		]),
	},
}
</script>
