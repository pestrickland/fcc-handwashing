<script>
  import HowTo from "./HowTo.svelte";
  import Timer from "./Timer.svelte";
  let audio;
  function timerEnds(e) {
    audio.play();
  }
</script>

<style>
  h1, h3 {
    text-align: center;
  }
</style>

<h1>Handwashing App</h1>
<Timer on:end={timerEnds}/>
<HowTo />

<h3>
<a href="http://www.who.int/gpsc/clean_hands_protection/en/">Picture Source</a>
<a href="http://freesound.org/people/metrostock99/sounds/345086/">Sound Source</a>
</h3>

<audio bind:this={audio} src="sound.mp3"></audio>
