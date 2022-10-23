<script>
export let files;
$: if (files) {
  console.log(files);
}
</script>

<label for="avatar">Upload your css</label>

  <input
    accept="text/plain"
    bind:files
    id="css"
    name="css"
    type="file"
  />