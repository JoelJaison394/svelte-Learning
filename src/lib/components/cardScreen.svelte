<script>
	import Cardslotdefault from "./cardslotdefault.svelte";
import Cardslots from "./cardslots.svelte";
</script>

<body class="bg-gray-100 min-h-screen flex items-center justify-around">
    <Cardslots/>
    <!--now using slots lets modify the card-->
    <Cardslots>
        <h2 class="text-2xl font-semibold mb-2 text-gray-800">Now we can use slots to render this</h2>
        <p class="text-gray-600">The card -2 using slots</p>
    </Cardslots>
    <!--there is a another way to render the default content if no child compoent is passed-->
    <!--with child -->
    <Cardslotdefault>
        <h2 class="text-2xl font-semibold mb-2 text-gray-800">slots with child component</h2>
    </Cardslotdefault>
        <!--without child -->
        <Cardslotdefault>
            
        </Cardslotdefault>
</body>