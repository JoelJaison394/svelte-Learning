<script>
    import Binding from '../lib/components/binding.svelte';
    import '../app.postcss';
	import Conditions from '../lib/components/conditions.svelte';
	import List from '../lib/components/list.svelte';
</script>

<body>
    <div class="container p-5">
        <Binding/>
        <Conditions/>
        <List/>
    </div>

</body>
