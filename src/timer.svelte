<script>
  import Progressbar from "./progressbar.svelte";
  const totalSeconds = 11;
  let secondsleft = totalSeconds;
  let isRunning = false;
  $: progress = (totalSeconds - secondsleft) * (100 / totalSeconds);
  function startTimer() {
    if (isRunning == false) {
      let timer = setInterval(() => {
        secondsleft -= 1;
        if (secondsleft == 0) {
          clearInterval(timer);
          isRunning = false;
          secondsleft = totalSeconds;
        }
      }, 1000);
      isRunning = true;
    }
  }
</script>

<style>
  h2 {
    margin: 0;
  }
  .start {
    background-color: rgb(154, 73, 12);
    width: 100%;
    margin: 10px 0;
    color: aliceblue;
  }
  .start[disabled] {
    background-color: gray;
    cursor: not-allowed;
  }
</style>

<div bp="grid">
  <h2 bp="offset-5@md 4@md 12@sm">Seconds Left: {secondsleft}</h2>

</div>

<Progressbar width={progress} />
<div bp="grid">
  <button
    disabled={isRunning}
    on:click={startTimer}
    bp="offset-5@md 4@md 12@sm"
    class="start">
    Start
  </button>
</div>
