<script>
	import MyButton from "./components/MyButton.svelte";
	import Counter from "./components/Counter.svelte";
	import Counter2 from "./components/Counter2.svelte";
	import Numbers from "./components/Numbers.svelte";
	import MyHeader from "./components/MyHeader.svelte";
	import MyInfo from "./components/MyInfo.svelte";
	import LogicPractice from "./components/LogicPractice.svelte";

	let name = "world";
	// name = name.toUpperCase();
	let src = "favicon.png";
	let string = `this string contains some <strong>HTML!!!</strong>`;

	const info = {
		name: "eddie",
		age: 20,
		sex: "male",
	};
</script>

<style>
	h1 {
		color: red;
	}
</style>

<h1>Hello {name.toUpperCase()}</h1>
<img {src} alt="logo" />
<MyButton />
<p>
	{@html string}
</p>
<Counter />
<Numbers />
<Counter2 />
<MyHeader title={'Sam'} />
<!-- <MyInfo name={info.name} age={info.age} sex={info.sex}/> -->
<MyInfo {...info} />
<LogicPractice />
