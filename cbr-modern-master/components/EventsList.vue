<!-- this component returns a list of all the events (Hopefully)-->
<template>
	<div class="">
		<!-- these would show while the data loads or if an error -->
		<p v-if="$fetchState.pending">Loading events...</p>
		<p v-else-if="$fetchState.error">Error while fetching events</p>

		<ul v-else class="list-group">
			<!-- this is a for loop, it just loops through the list of events returned from the API -->
			<li v-for="event in events" :key="event.id" class="list-group-item">
				<!-- now make a link for each item -->
				<!-- <NuxtLink :to="event.slug"> -->
				<NuxtLink :to="'/events2/' + events2.slug">
					<!-- return the rendered title -->
					{{  events2.title.rendered  }}
				</NuxtLink>
				<!-- now show me the event year -->
				: {{ event.acf.year }}
			</li>
		</ul>
		<h3>this list is stored in components/EventsList.vue</h3>

	</div>
</template>


<script>
export default {
	// layout: 'home',
	async fetch() {
		this.events = await fetch('http://cm.beneb.com/wp-json/wp/v2/events/?per_page=20').then((res) =>
			res.json()
		)
	},
	data() {
		return {
			events: [],
		}
	},
}
</script>