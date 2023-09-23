<script>
    import { createEventDispatcher } from "svelte";
    const dispatcher = createEventDispatcher();
</script>

<body>
    <div class="p-4 bg-gray-100 rounded-lg shadow-md text-center">
        <h2 class="text-2xl font-semibold mb-4">Hey, this is an inner component nested inside the outer component</h2>
        <button
            class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
            on:click={() => {
                dispatcher('greet');
            }}
        >
            Greet me!!
        </button>
    </div>
</body>
