<template>
	<div class="container">
		<div class="main-container">
			Buongiorno stocazzo!
		</div>
	</div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
	name: 'profilePage',
	data() {
        return {
            user: this.$auth.user
        }
	}
})
</script>