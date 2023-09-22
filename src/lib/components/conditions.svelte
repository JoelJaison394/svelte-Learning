<script>
    let age = 24;
</script>
<body>
    <label >Enter your age</label>
    <input type="text" bind:value={age} placeholder="age">
    {#if age > 28}
    <h1 class="text-3xl font-bold text-green-600">Hey everyone, I'm an adult now</h1>
{:else if age > 18 && age < 28}
    <h1 class="text-3xl font-bold text-yellow-500">Hey everyone, I'm a teenager now</h1>
{:else}
    <h1 class="text-3xl font-bold text-red-600">I'm still young</h1>
{/if}
</body>