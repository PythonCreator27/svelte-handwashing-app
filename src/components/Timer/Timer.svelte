<script>
    import ProgressBar from './ProgressBar/ProgressBar.svelte';

    const totalSeconds = 20;
    let secondsLeft = totalSeconds;
    let isRunning = false;
    $: progress = ((totalSeconds - secondsLeft) / totalSeconds) * 100;
    const onStart = () => {
        isRunning = true;
        const interval = setInterval(() => {
            secondsLeft--;
            if (secondsLeft === 0) {
                isRunning = false;
                clearInterval(interval);
                secondsLeft = totalSeconds;
            }
        }, 1000);
    };
</script>

<div class="container">
    <p class="h2">Seconds Left: {secondsLeft}</p>
    <ProgressBar {progress} />
    <button
        class="button-primary"
        style="width: 80%"
        on:click={onStart}
        disabled={isRunning}>Start</button
    >
</div>

<style>
    .container {
        margin-bottom: 3rem;
    }

    button:disabled {
        background-color: #83d2eb;
        cursor: not-allowed;
    }
</style>
