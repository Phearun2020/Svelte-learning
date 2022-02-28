<script>
	let students = [
		// {name: 'Dara', beltColour: 'yellow', age: '21', id: 1},
		// {name: 'Thara', beltColour: 'blue', age: '22', id: 2},
		// {name: 'Both', beltColour: 'black', age: '23', id: 3},
		// {name: 'Ramos', beltColour: 'green', age: '21', id: 4},
	];
</script>

<main>
	{#each students as person (person.id)}
		<div>
			<h4>id {person.id} {person.name}</h4>
			<p>{person.age} year old, {person.beltColour} belt.</p>
		</div>
		{:else}
			<p>There are no students to show ...</p>
		
	{/each}
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