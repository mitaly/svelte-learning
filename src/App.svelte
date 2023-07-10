<script>
	const name="Mitaly";
	const winAPrize = `<a href="#" onclick="alert('You have won a prize')">Win a prize</a>`;
	const headingId= 'heading';
	const disabled = true;
	const greenClass = 'green';
	const isPromoted = true;
	const promoted = false;
</script>

<main>
	<h1 id={headingId}>Hello {name}!</h1>
	<h2 class={isPromoted ? 'promoted' : ''}>Movie title class with conditional binding</h2>
	<h2 class:promoted={isPromoted}>Movie title class with directive conditional binding</h2>
	<h2 class:promoted>Movie title class with shorthand directive conditional binding</h2>
	<div>{@html winAPrize}</div>
	<button class={greenClass} disabled={disabled}>Click me</button>
	
</main>

<style>
	.promoted {
		font-style: italic;
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	.green {
		background-color: green;
	}
</style>