<template>
	<Head>
		<meta type="description" content="Default keywords" head-key="description"/>
	</Head>

	<div class="main-container relative overflow-hidden flex flex-col min-h-screen">
		<div class="bg-gray-100 mb-6">
			<div class="max-w-7xl flex justify-between items-center px-6 mx-auto py-4">
				<div>
					Sanctum Test
				</div>

				<div class="flex gap-x-8">
					<i-link href="/">Home</i-link>
					<i-link href="/login">Login</i-link>
					<i-link href="/account">Account</i-link>
					<i-link v-if="user" href="/logout">Logout</i-link>
				</div>
			</div>
		</div>

		<div class="flex-grow flex">
			<slot></slot>
		</div>
	</div>
</template>

<script>

	import { Head } from "@inertiajs/vue3";

	export default {
		components: {
			Head
		},

		props: {
			user: {}
		},

		data: function() {
			return {

			}
		},

		mounted() {

		},

		methods: {

		},

		computed: {

		}
	}
</script>