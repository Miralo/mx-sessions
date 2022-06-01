<template>
	<div class="container">
		<div class="main-container">
			<SingleGame name="Lollo"/>
		</div>
	</div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
	name: 'IndexPage',
	data() {
		return {
			game: null
		}
	},
	async fetch() {
		//this.game = await this.$axios.$get('api/games/1649');
	},
	methods: {
		goBack() {
			return this.$router.go(-1)
		}
	}
})
</script>