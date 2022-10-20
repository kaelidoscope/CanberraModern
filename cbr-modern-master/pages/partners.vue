<template>
	<div class="container">
		
		<SiteNavigation />
		<div class="page">
			<!-- the data returns an array with one item in it, so need to reference it below -->
			<h2>{{  page[0].title.rendered  }}</h2>

			<!-- create a div to hold the renderedContent variable holding the data we've retrieved below -->
			<!-- if we don't use the v-html tag it will render it as a string -->
			<div v-html="renderedContent"></div>

			<!-- this will show all the data returned from the API, use it for troubleshooting -->
			<!-- <pre>{{ $data }}</pre> -->
		</div>
	</div>
</template>

<script>
	// in this API call, we load a page based off the URL paramter
	// we access what is in the URL by using the params object
	export default {
		async asyncData({ params }) {
			const page = await fetch(
				// `http://cm.beneb.com/wp-json/wp/v2/pages/?slug=${params.slug}`
				// `http://cm.beneb.com/wp-json/wp/v2/pages/157`
				`http://cm.beneb.com/wp-json/wp/v2/pages/?slug=partners`
			).then((res) => {
				if (res.ok) {
					return res.json()
				}
				throw new Error(res.status)
			})

			let renderedContent = page[0].content.rendered;
			return { renderedContent, page }
		},
	}
	</script>
