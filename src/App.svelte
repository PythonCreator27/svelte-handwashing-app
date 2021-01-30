<script lang="ts">
    import HowTo from './components/HowTo/HowTo.svelte';
    import Timer from './components/Timer/Timer.svelte';

    let audio: HTMLAudioElement;

    const timerEnded = () => {
        audio.play();
    };
</script>

<div class="container">
    <div class="row">
        <div class="tow-half column">
            <h1>Handwashing App</h1>
            <Timer on:timer-end={timerEnded} />
            <HowTo />
        </div>
    </div>
</div>

<!-- svelte-ignore a11y-media-has-caption -->
<audio bind:this={audio}>
    <source src="/sound.wav" />
</audio>

<style>
    h1 {
        text-align: center;
    }
</style>
