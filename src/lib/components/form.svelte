<script>
    // Initialize form values object
    let formValues = {
      textInput: '',
      numberInput: '',
      emailInput: '',
      checkboxInput: false,
      radioButton: '',
      multiSelect: [],
      textArea: '',
      dateInput: '',
    };
  
    // Function to update form values
    const updateFormValue = (field, value) => {
      formValues = { ...formValues, [field]: value };
    };
  </script>

<body class="bg-gray-200 flex justify-center items-center h-auto mt-6 p-10" >
    <div class="max-w-md w-full mx-auto bg-white p-6 rounded-lg shadow-lg">
      <h1 class="text-2xl font-semibold mb-4 text-blue-600">Form</h1>
      
      <!-- Text Input -->
      <div class="mb-4">
        <label for="textInput" class="block text-gray-600">Text Input:</label>
        <input
          type="text"
          id="textInput"
          class="border border-gray-300 p-2 rounded w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
          bind:value={formValues.textInput}
        />
      </div>
    
      <!-- Number Input -->
      <div class="mb-4">
        <label for="numberInput" class="block text-gray-600">Number Input:</label>
        <input
          type="number"
          id="numberInput"
          class="border border-gray-300 p-2 rounded w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
          bind:value={formValues.numberInput}
        />
      </div>
    
      <!-- Email Input -->
      <div class="mb-4">
        <label for="emailInput" class="block text-gray-600">Email Input:</label>
        <input
          type="email"
          id="emailInput"
          class="border border-gray-300 p-2 rounded w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
          bind:value={formValues.emailInput}
        />
      </div>
    
      <!-- Checkbox Input -->
      <div class="mb-4">
        <label class="block text-gray-600">
          <input
            type="checkbox"
            class="mr-2"
            bind:checked={formValues.checkboxInput}
          />
          Checkbox Input:
        </label>
      </div>
    
      <!-- Radio Buttons -->
      <div class="mb-4">
        <label class="block text-gray-600">Radio Buttons:</label>
        <label class="inline-flex items-center">
          <input
            type="radio"
            class="mr-2"
            name="radioButton"
            value="Option 1"
            bind:group={formValues.radioButton}
          />
          Option 1
        </label>
        <label class="inline-flex items-center">
          <input
            type="radio"
            class="mr-2"
            name="radioButton"
            value="Option 2"
            bind:group={formValues.radioButton}
          />
          Option 2
        </label>
      </div>
    
      <!-- Multi-Select Dropdown -->
      <div class="mb-4">
        <label class="block text-gray-600">Multi-Select Dropdown:</label>
        <select
          multiple
          class="border border-gray-300 p-2 rounded w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
          bind:value={formValues.multiSelect}
        >
          <option value="Option 1">Option 1</option>
          <option value="Option 2">Option 2</option>
          <option value="Option 3">Option 3</option>
        </select>
      </div>
    
      <!-- Text Area -->
      <div class="mb-4">
        <label for="textArea" class="block text-gray-600">Text Area:</label>
        <textarea
          id="textArea"
          class="border border-gray-300 p-2 rounded w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
          bind:value={formValues.textArea}
        ></textarea>
      </div>
    
      <!-- Date Input -->
      <div class="mb-4">
        <label for="dateInput" class="block text-gray-600">Date Input:</label>
        <input
          type="date"
          id="dateInput"
          class="border border-gray-300 p-2 rounded w-full focus:outline-none focus:ring-2 focus:ring-blue-500"
          bind:value={formValues.dateInput}
        />
      </div>
    
      <button
        class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600"
        on:click={() => alert(JSON.stringify(formValues, null, 2))}
      >
        Submit
      </button>
    </div>
    
    <div class="max-w-md w-full mx-auto mt-4 bg-white p-4 rounded-lg shadow-lg">
      <h2 class="text-lg font-semibold mb-2 text-blue-600">Live Preview</h2>

      <pre>{JSON.stringify(formValues, null, 2)}</pre>
    </div>
  </body>
  
  

  