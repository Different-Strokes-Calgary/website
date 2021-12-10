<script>
	const fetchImage = (async () => {
		const response = await fetch('https://calendar.google.com/calendar/ical/differentstrokesyyc%40gmail.com/public/basic.ics');
    return await response.json()
	})()
</script>

{#await fetchImage}

...waiting

{:then data}

{data.message}

{:catch error}

An error occurred!

{/await}
