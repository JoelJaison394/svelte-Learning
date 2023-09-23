<body>
    <!-- this is the default conent of the card-->
    <slot>
        <div class="">
            <div class="max-w-md w-full bg-white shadow-lg rounded-lg overflow-hidden">
                <img class="w-full h-auto object-cover object-center" src="https://t4.ftcdn.net/jpg/05/47/26/33/360_F_547263397_sylHi4aJQoB6eLkFT97f5UUOZVtqESQh.jpg" alt="Card Image">
                <div class="p-4">
                    <h2 class="text-xl font-semibold text-gray-800 mb-2">Card Title</h2>
                    <p class="text-gray-600">This is a simple card component using Tailwind CSS.</p>
                </div>
                <div class="p-4 bg-gray-100 border-t border-gray-200">
                    <button class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600">Learn More</button>
                </div>
            </div>
        </div>
    </slot>

</body>