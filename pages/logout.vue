<template>
	<div class="container">
		<div class="main-container">
			Logging out...
		</div>
	</div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
	name: 'LogoutPage',
	data() {
	},
    created: async function() {
        await this.$auth.logout();
    }
})
</script>