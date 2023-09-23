<script>
	import { setContext } from 'svelte';
	import Binding from '../lib/components/binding.svelte';
	import '../app.postcss';
	import Conditions from '../lib/components/conditions.svelte';
	import List from '../lib/components/list.svelte';
	import Form from '../lib/components/form.svelte';
	import HighlevelComponent from '../lib/components/highlevelComponent.svelte';
	import Outer from '../lib/components/outer.svelte';
	import CardScreen from '../lib/components/cardScreen.svelte';
	let data = [
		{
			id: 1,
			productName: 'phone',
			price: '24000'
		},
		{
			id: 2,
			productName: 'TV',
			price: '75000'
		},
		{
			id: 3,
			productName: 'Fridge',
			price: '12000'
		},
		{
			id: 4,
			productName: 'Laptop',
			price: '142000'
		},
		{
			id: 5,
			productName: 'Speaker',
			price: '8000'
		}
	];
	setContext('data-context', data);
</script>

<body>
	<div class="container p-5">
		<Binding />
		<Conditions />
		<List />
		<Form />
		<HighlevelComponent />
		<Outer
			on:greet={() => {
				alert('Namsthe');
			}}
		/>
		<CardScreen />
	</div>
</body>
