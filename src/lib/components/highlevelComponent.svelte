<script>
    import NestedComponents from "./NestedComponents.svelte";
</script>

<!-- Apply Tailwind CSS classes to style your components -->
<div class=" p-4">
    <h1 class="text-2xl font-bold mb-4">This shows the use of Context API in Svelte</h1>
    <h1 class="text-xl font-semibold">This is component level -1</h1>
    <NestedComponents />
</div>