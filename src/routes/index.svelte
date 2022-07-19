<script context="module">
	export const prerender = true;
</script>

<script>
	import Counter from '$lib/Counter.svelte';
	let name = 'world';
	let name2 = 'world';
	let currentValue = 1;
	let showText2 = true;
	let finalName = '';
	$: name, name2, (() => {finalName = `${name} - ${name2} !!!`;})();

	let src = 'https://scontent.fsgn5-8.fna.fbcdn.net/v/t1.6435-9/82972507_464875250857172_6844397026059223040_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=730e14&_nc_ohc=_gIa6WRtMikAX8ywdgT&_nc_ht=scontent.fsgn5-8.fna&oh=00_AT-P4MLcCv7QFoargnL3sIscteV8OjhVkhtOi2WSoc-UFQ&oe=62FD2404';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<input type=checkbox bind:checked={showText2}>
	
	<label for="customRange1" class="form-label">Example range</label>
<input type="range" class="form-range"  min="0" max="5" bind:value={currentValue} id="customRange1">
	<p>Current Value: {currentValue}</p>
	<table class="table  table-hover table-borderless">
		<thead>
		  <tr>
			<th scope="col">#</th>
			<th scope="col">First</th>
			<th scope="col">Last</th>
			<th scope="col">Handle</th>
		  </tr>
		</thead>
		<tbody>
		  <tr>
			<th scope="row">1</th>
			<td>Mark</td>
			<td>Otto</td>
			<td>@mdo</td>
		  </tr>
		  <tr>
			<th scope="row">2</th>
			<td>Jacob</td>
			<td>Thornton</td>
			<td>@fat</td>
		  </tr>
		  <tr>
			<th scope="row">3</th>
			<td colspan="2">Larry the Bird</td>
			<td>@twitter</td>
		  </tr>
		</tbody>
	  </table>


</section>
