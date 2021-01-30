<script>
    import ProgressBar from './ProgressBar/ProgressBar.svelte';
</script>

<div class="container">
    <p class="h2">Seconds Left:</p>
    <ProgressBar />
    <button class="button-primary" style="width: 100%">Start</button>
</div>

<style>
    .container {
        margin-bottom: 3rem;
    }
</style>
