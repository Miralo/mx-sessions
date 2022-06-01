<template>
	<div>
		<b-navbar toggleable="lg" type="dark" variant="success">
			<b-navbar-brand href="#">MX Sessions</b-navbar-brand>

			<b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

			<b-collapse id="nav-collapse" is-nav>
				<b-navbar-nav>
					<b-nav-item href="#">Link</b-nav-item>
					<b-nav-item href="#" disabled>Disabled</b-nav-item>
				</b-navbar-nav>

				<!-- Right aligned nav items -->
				<b-navbar-nav class="ml-auto">
					<b-nav-form>
						<b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
						<b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
					</b-nav-form>

					<b-nav-item-dropdown right>
						<!-- Using 'button-content' slot -->
						<template #button-content>
							User
						</template>
						<b-dropdown-item href="#">Profile</b-dropdown-item>
						<b-dropdown-item href="#">Sign Out</b-dropdown-item>
					</b-nav-item-dropdown>
				</b-navbar-nav>
			</b-collapse>
		</b-navbar>

		<main>
			<Nuxt />
		</main>
	</div>
</template>

<style>
body {
	margin: 0;
}
main {
	margin: 0 auto;
	padding: 0 1rem;
	margin-top: 100px;
	max-width: 1280px;
	text-align: center;
}
</style>
