<script> 
    let fruit = '';
    let fruits = ["apple"];
  
    const handleInput = () => {
      console.log(fruit);
      fruits = [...fruits, fruit];
      fruit = '';
    };
  
    $: {
      // Render the fruits state after it is updated.
      fruits = [...fruits];
    }
  </script>
  
  <body class="bg-gray-100 p-4 mt-6">
    <div class="max-w-md mx-auto bg-white rounded p-4 shadow-lg ">
      <input
        type="text"
        placeholder="What's your favorite fruit"
        class="border border-gray-300 p-2 rounded w-full"
        bind:value={fruit}
      />
      <button
        on:click={handleInput}
        class="bg-blue-500 text-white px-4 py-2 mt-2 rounded hover:bg-blue-600"
      >
        Add as favorite fruit
      </button>
      <h1 class="text-xl mt-4">Your favorite fruits are listed below using each</h1>
      {#each fruits as fruit }
        <h2 class="text-lg mt-2 text-purple-400">{fruit}</h2>
      {/each}
    </div>
  </body>
  