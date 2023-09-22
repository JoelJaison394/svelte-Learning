<script>
	let name = 'joel';
	let html = '<b>This text is bold</b><h1 class="text-2xl">Binding</h1>';
    const headingclass = 'text-4xl'
    const heading = "<h1>This is a heading </h1>"
    const heading1 = '<h1 class={headingClass}>This is a heading </h1>'
</script>

<body>
	<div class="container mx-auto p-4">
		<h1 class="text-2xl font-bold mb-4">Binding</h1>
		<p class="mb-4">Example-1 binding with a variable</p>
		<h3 class="text-3xl font-semibold mb-2">
			Hi👋, <span id="nameDisplay" class="text-blue-500">{name}</span>
		</h3>
		<p class="mb-4">Okay, now let's change the value of the variable "name" and see the magic 🪄</p>
		<label for="name" class="mb-2">Name :</label>
		<input
			type="text"
			bind:value={name}
			id="name"
			class="border rounded px-3 py-2 focus:outline-none focus:ring focus:border-blue-500 mb-4"
		/>

		<p class="mb-4">Okay, that was strange, right? Let me show something more -</p>
		<textarea
			bind:value={html}
			id="html"
			cols="30"
			rows="10"
			class="border rounded px-3 py-2 focus:outline-none focus:ring focus:border-blue-500 mb-4"
		/>
		<div class="border rounded px-3 py-2 mb-4" id="htmlOutput">{@html html}</div>
        <div class="container mx-auto p-4">
            <p class="text-lg font-bold mb-4">Okay, that's cool</p>
        
            <div class="bg-gray-200 p-4 rounded-lg shadow-lg mb-4">
                <p class="text-2xl font-semibold mb-2">{heading}</p>
                <p class="mb-2">Now, let's add the <span class="text-blue-500">{headingclass}</span> class as an attribute and show the outcome - like <span class="text-blue-500">{heading1}</span> where variable heading class = {headingclass}</p>
                <div class="bg-gray-100 p-4 rounded-lg shadow-md">
                    <p class="mb-4">Before adding:</p>
                    {@html heading}
                </div>
                <div class="bg-gray-100 p-4 rounded-lg shadow-md mt-4">
                    <p class="mb-4">After adding:</p>
                    <h1 class="{headingclass} text-4xl">This is a heading</h1>
                </div>
            </div>
        </div>
        
	</div>
</body>

<style>
</style>
