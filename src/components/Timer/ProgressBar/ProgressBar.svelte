<script lang="ts">
    export let progress = 100;
</script>

<div class="container">
    <div class="row progress-container">
        <div class="progress-bar" style="width: {progress}%">
            <div class="sr-only">{progress}%</div>
        </div>
    </div>
</div>

<style>
    .progress-container {
        margin: 20px 0;
        border: solid #c2c2c2 1px;
    }

    .progress-bar {
        height: 30px;
        background-color: #4dc737;
    }
</style>
