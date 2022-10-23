<script>
// import { Lowdash } from "lowdash";
import "./app.postcss";
let input;
let output
let error = "still not working";

const handleInput = (input, output, error) => {
  input = document.getElementById("iput");
  output = document.getElementById("output");
  try {
    output = JSON.stringify(JSON.parse(input), null, 2);
  } catch (e) {
    error = e;
  }
};

const toggle = () => {true ? false : true};
</script>

<main class = "grid-flow-col">

  <div class ="flex justify-center">
    <h1 class="text-4xl font-bold">Vite + Svelte CSS</h1>
  </div>

<form class="grid w-screen px-5 py-5">
  <div class="mb-4 w-full bg-gray-50 rounded-lg border border-gray-200 dark:bg-gray-700 dark:border-gray-600">
    <div class="pt-2 px-4 bg-whiter rounded-t-lg dark:bg-gray-800 ">
      <label for="comment" class="sr-only">
        {input}
      </label>
      <textarea 
        bind:value={input}
        id="iput"
        rows="6"
        class="px-0 w-full text-sm text-gray-900 bg-white border-0 dark:bg-gray-800 focus:ring-0 dark:text-white dark:placeholder-gray-400"
        placeholder="{input}"
        ></textarea>
    </div>
  </div>
</form>
<form class="w-screen px -inset-5 px-5" >


  <div class ="flex justify-center">
  <button type="button" class="Fflex justify-self-center focus:outline-none text-white bg-red-700 hover:bg-red-800 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sm px-5 py-2.5 mb-6 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900">convert</button>
  </div>

  <div class="grid mb-4 w-full bg-gray-50 rounded-lg border border-gray-200 dark:bg-gray-700 dark:border-gray-600">
    <div class="py-2 px-4 bg-whiter rounded-t-lg dark:bg-gray-800 ">
      <label for="comment" class="sr-only">
        {output}
      </label>
      <textarea
      bind:value={input}
        id="iput"
        rows="6"
        class="px-0 w-full text-sm text-gray-900 bg-white border-0 dark:bg-gray-800 focus:ring-0 dark:text-white dark:placeholder-gray-400"
        placeholder='{output}'
        disabled = true
      ></textarea>
    </div>
  </div>
</form>

</main>