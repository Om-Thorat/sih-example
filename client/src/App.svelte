<script>
  import Asdas from "./lib/Asdas.svelte";
  let rand = -1;

  function getRand() {
    fetch("./rand")
      .then(d => d.text())
      .then(d => (rand = d));
  }
</script>

<h1>Our Love is {rand}!</h1>
<button on:click={getRand}>Get a random number</button>
<Asdas />