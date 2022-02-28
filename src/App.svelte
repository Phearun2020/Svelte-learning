<script>
	let students = [
		{name: 'Dara', beltColour: 'yellow', age: '21', score: 89, id: 1},
		{name: 'Thara', beltColour: 'blue', age: '22', score: 35, id: 2},
		{name: 'Both', beltColour: 'black', age: '23', score: 50, id: 3},
		{name: 'Ramos', beltColour: 'green', age: '21', score: 45, id: 4},
	];

	const handleClick = (id) =>{
		// delete the person from students
		// console.log(id);
		students = students.filter((person) => person.id != id);

	}
	let num = 50;
</script>

<main>
	
	{#each students as person (person.id)}
		
		<div>
			<h4>id {person.id} {person.name}</h4>
			<p>{person.age} year old, your score totaly {person.score}, {person.beltColour} belt.</p>
			{#if num < person.score}
				<p>Congraulation</p>
				{:else if person.score == num}
				 	<p>good luck</p>
				{:else}
					<p>you are lose.</p>
			{/if}
			<button on:click={() => {handleClick(person.id)}}>Delete</button>
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