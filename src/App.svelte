<script>
	
	let hello = 'Phearun';
	let beltColour = 'blue';
	const handleClick =()=>{
		beltColour = 'red';
	};
	const handleInput = (e) =>{
		beltColour = e.target.value;
	}
</script>

<main>
	<h1>Hello {hello}!</h1>
	<p style="color: {beltColour}">{beltColour}!</p>
	<button on:click={handleClick}>click here</button>
	<!-- <input type="text" on:input={handleInput} value={beltColour}> -->
	<input type="text" bind:value={beltColour}>
</main>

<style>
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
</style>