<template>
	<div class="container">
		<SiteNavigation />
		
		

		<div class="building">
			<h2>Buildings</h2>
			<!-- The building list is over in the components folder -->
			<h4>The Top 20 Mid and Late Century Modern Buildings.</h4>
			<!-- the code below loads the component here so we can use it again -->
			<BuildingsList />

			<!-- this is a really useful line of code that will just output what the API call returns -->
			<!-- <pre>{{ $data }}</pre> -->
		</div>
	</div>
</template>

<script>
// in this API call, we go get a specific building, filtered by the ID in the URL
// we access what is in the URL by using the params object
export default {
	async asyncData({ params }) {
		const building = await fetch(
			`http://cm.beneb.com/wp-json/wp/v2/buildings/`
		).then((res) => {
			if (res.ok) {
				return res.json()
			}
			throw new Error(res.status)
		})
		return { building }
	},
}
</script>


<style>
	
</style>