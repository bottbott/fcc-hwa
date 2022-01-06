<script>
    import Timer from './Timer.svelte'
    import HowTo from './HowTo.svelte';
    let audio;

    function timerEnds(e) {
        console.log(e)
        audio.play();
    }
</script>

<style>
    h1, h3 { 
        text-align: center;
    }
</style>

<h1>Hand Washing App</h1>
<Timer on:end={timerEnds}/>
<HowTo/>
<h3><a href="https://www.who.int/gpsc/clean_hands_protection/en">Picture Source</a> <a href="https://freesound.org/people/metrostock99/sounds/345086/">Sound Attribution</a></h3>
<audio bind:this={audio}>
    <source src="345086__metrostock99__oh-yeah-low-4.wav">
</audio>