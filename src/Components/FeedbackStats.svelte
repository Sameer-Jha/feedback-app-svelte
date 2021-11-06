<script>
    export let count;
    export let average;

    import Card from './Card.svelte'
</script>

<Card>
    <div class="feedback-stats">
        <h4>{count} Reviews</h4>
        <h4>Average: {average}</h4>
    </div>
</Card>

<style>
    .feedback-stats{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .feedback-stats h4 {
        padding: 20px;
    }
</style>

