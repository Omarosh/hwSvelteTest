<script>
  import HT from "./HT.svelte";
  import Timer from "./timer.svelte";
  let audio;

  function timerEnds(e) {
    console.log(e);
  }
</script>

<style>
  h1 {
    text-align: center;
  }
</style>

<head>
  <link href="https://fonts.googleapis.com/css?family=Lato" rel="stylesheet" />

</head>
<h1>Test</h1>

<Timer on:end={timerEnds} />
<HT />
<h3>picture source</h3>

<audio bind:this={audio}>
  <source src="ballon.mp3" />
</audio>
