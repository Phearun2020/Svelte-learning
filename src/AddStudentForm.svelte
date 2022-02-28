<script>
    let name;
    let beltColour;
    let age;

    // let php = false;
    // let java = false;
    // let laravel = false;
    let skills = [];

    const handleSubmit = () => {
        console.log(name, beltColour, age, skills);
    };
</script>
<!-- preventDefault is prevent the page from refreshing -->
<form on:submit|preventDefault={handleSubmit}>
    <input type="text" placeholder="name" bind:value={name}>
    <input type="number" placeholder="age" bind:value={age}>
    <label>Skills:</label>
    <!-- <input type="checkbox" bind:checked={php}>PHP<br>
    <input type="checkbox" bind:checked={java}>JAVA<br>
    <input type="checkbox" bind:checked={laravel}>LARAVEL<br> -->
    <input type="checkbox" bind:group={skills} value="php">PHP<br>
    <input type="checkbox" bind:group={skills} value="java">JAVA<br>
    <input type="checkbox" bind:group={skills} value="laravel">LARAVEL<br> 
    <label>Belt Colour</label>
    <select bind:value={beltColour}>
        <option value="black">Black</option>
        <option value="white">White</option>
        <option value="green">Green</option>
        <option value="blue">Blue</option>
        <option value="gray">Gray</option>
        <option value="red">Red</option>
    </select>

    <button>Add new student</button>
</form>