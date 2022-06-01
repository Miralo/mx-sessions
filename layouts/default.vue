<template>
	<div>
		<b-navbar toggleable="lg" type="light" variant="default" fixed="top">
			<b-navbar-brand to="/">MX Sessions</b-navbar-brand>

			<b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

			<b-collapse id="nav-collapse" is-nav>
				<b-navbar-nav>
					<b-nav-item to="/">Home</b-nav-item>
					<b-nav-item href="#" disabled>Disabled</b-nav-item>
				</b-navbar-nav>

				<!-- Right aligned nav items -->
				<b-navbar-nav class="ml-auto">
					<b-nav-form>
						<b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
						<b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
					</b-nav-form>

					<b-nav-item-dropdown right v-if="user && user !== 'undefined'">
						<!-- Using 'button-content' slot -->
						<template #button-content>
							{{ user.nickname }}
						</template>
						<b-dropdown-item href="/profile/">Profile</b-dropdown-item>
						<b-dropdown-item to="/logout/">Sign Out</b-dropdown-item>
					</b-nav-item-dropdown>

					<b-nav-item to="/login/" v-if="!user || user == 'undefined'">Login</b-nav-item>

				</b-navbar-nav>
			</b-collapse>
		</b-navbar>

		<main>
			<Nuxt />
		</main>
	</div>
</template>

<style>
body, html {
	margin: 0;
	background-color: #eff2f6;
	min-height: 100vh;
}
main {
	margin-top: 60px;
}
.main-container {
	background-color: #fff;
	padding: 1rem;
}
</style>

<script>
	export default {
		data() {
			return {
				user: this.$auth.user
			}
		},
		created: function() {
			console.log(this.$auth);
		}
	}
</script>