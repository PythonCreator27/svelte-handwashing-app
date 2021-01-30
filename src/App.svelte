<script lang="ts">
    import HowTo from './components/HowTo/HowTo.svelte';
    import Timer from './components/Timer/Timer.svelte';
</script>

<div class="container">
    <div class="row">
        <div class="tow-half column">
            <h1>Handwashing App</h1>
            <Timer />
            <HowTo />
        </div>
    </div>
</div>

<style>
    h1 {
        text-align: center;
    }
</style>
