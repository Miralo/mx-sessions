<template>
	<div class="container">
		<div class="main-container">
			Logging...
		</div>
	</div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
	name: 'LoginPage',
	data() {
	},
    created: function() {
        this.$auth.loginWith('auth0');
    }
})
</script>