<script>
	const fetchImage = (async () => {
		const response = await fetch('/schedule.ics');
    return await response.text()
	})()
</script>

GH Pages Publish

{#await fetchImage}

...waiting

{:then data}

{data}

{:catch error}

An error occurred!

{/await}
