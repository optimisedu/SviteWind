<script>
    let css = 'David';
  $: capitalLetters = css.replaceAll('a', '');
  </script>
  
  <h1>Hello {css}!</h1>
  <input bind:value={css} />
  <p>
      Your css in capital letters: {capitalLetters}
  </p>