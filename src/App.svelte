<script>
let css = 'Input CSS Here';
$: sanitised = css.replaceAll(' ', '');
let output;
</script>
<main class = "grid-flow-col">
  <div class ="flex justify-center">
    <h1 class="text-4xl font-bold">CSS Manipulation</h1>
  </div>

  <form class="grid w-screen px-5 py-5">
    <div class="mb-4 w-full bg-gray-50 rounded-lg border border-gray-200 dark:bg-gray-700 dark:border-gray-600">
      <div class="px-4 bg-whiter rounded-t-lg dark:bg-gray-800 ">
        <label for="comment" class="sr-only">
       
        </label>
        <input bind:value={css}
          id="iput"
          rows="6"
          class="px-0 w-full text-sm text-gray-900 bg-white border-0 dark:bg-gray-800 focus:ring-0 dark:text-white dark:placeholder-gray-400"
          placeholder={css}
          >
      </div>
    </div>
  </form>

   
  <form class="grid w-screen px-5 py-5">
    
    
      <div class ="flex justify-center">
      <button type="button" class="Fflex justify-self-center focus:outline-none text-white bg-red-700 hover:bg-red-800 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sm px-5 py-2.5 mb-6 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900" on:click={output = sanitised}>Convert</button>
      </div>
    
      <div class="grid mb-4 w-full bg-gray-50 rounded-lg border border-gray-200 dark:bg-gray-700 dark:border-gray-600">
        <div class="py-2 px-4 bg-whiter rounded-t-lg dark:bg-gray-800 ">
          <label for="comment" class="sr-only">
            {sanitised}
          </label>
          <textarea
    
            id="outpt"
            rows="6"
            class="px-0 w-full text-sm text-gray-900 bg-white border-0 dark:bg-gray-800 focus:ring-0 dark:text-white dark:placeholder-gray-400"
            placeholder='{sanitised}'
          ></textarea>
        </div>
      </div>
    </form>
    
    </main>