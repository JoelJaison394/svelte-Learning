<script>
    import { getContext } from "svelte";
    let data = getContext('data-context');
</script>

<body>
    <div class="flex flex-row space-x-4"> <!-- Use flex to create a row layout with spacing -->
        {#each data as product }
        <div class="bg-white p-4 rounded-lg shadow-md" key={product.id}> <!-- Apply card styling -->
            <h1 class="text-xl font-semibold">{product.productName}</h1> <!-- Style heading text -->
            <h1 class="text-lg font-medium">${product.price}</h1> <!-- Style price text -->
        </div>
        {/each}
    </div>
</body>
