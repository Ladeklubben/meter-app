<script lang="ts">
    import { fade } from "svelte/transition";
    export let description: string;
    export let stat: string;
    export let unit: string;
</script>

<div class="wrapper">
    <span in:fade={{ duration: 300 }} style="text-align: center;">
        {description}

        <h2>{stat}<span class="unit">{unit}</span></h2>
    </span>
</div>

<style>
    .wrapper {
        display: flex;
        flex-direction: column;
        gap: 10px;
        padding: 32px;
        align-items: center;
        border-radius: var(--border-radius);
        border: 1px solid var(--lk-blue-800);
        background: linear-gradient(
            to right,
            var(--lk-blue-400),
            var(--lk-blue-800)
        );
    }

    h2 {
        font-size: 4rem;
        font-weight: bold;
        color: var(--lk-blue-100);
        margin: 0;
        margin-bottom: -10px;
    }

    .unit {
        font-size: 1rem;
        font-weight: normal;
    }
</style>
