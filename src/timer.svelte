<script>
  import Progressbar from "./progressbar.svelte";
</script>

<style>
  h2 {
    margin: 0;
  }
  .start {
    background-color: rgb(154, 73, 12);
  }
</style>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">Seconds Left:</h2>

</div>

<Progressbar />

<button class="start">Start</button>
