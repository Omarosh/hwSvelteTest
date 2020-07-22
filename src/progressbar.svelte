<script>
  export let width = 10;

  function addwidth() {
    width += 15;
  }
</script>

<style>
  .progress-container {
    margin: 20px 0;
    border: solid #414040;
  }
  .progress-bar {
    height: 30px;
    background-color: rgb(77, 199, 55);
  }
</style>

<div bp="grid">
  <div bp="offset-5@md 4@md 12@sm" class="progress-container">
    <div class="progress-bar" style="width:{width}%;">
      <span class="sr-only">{width}%</span>
    </div>
  </div>
</div>
>
