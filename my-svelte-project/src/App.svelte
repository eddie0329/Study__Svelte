<script>
	import MyButton from "./components/MyButton.svelte";

	let name = "world";
	// name = name.toUpperCase();
	let src = "favicon.png";
	let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<style>
	h1 {
		color: red;
	}
</style>

<h1>Hello {name.toUpperCase()}</h1>
<img {src} alt="logo" />
<MyButton />
<p>{@html string}</p>
