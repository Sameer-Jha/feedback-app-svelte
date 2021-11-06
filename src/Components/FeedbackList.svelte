<script>
    export let feedbacks = [];
	import FeedbackItem from './FeedbackItem.svelte'
</script>

{#each feedbacks as feedback (feedback.id)}
		<FeedbackItem {feedback}/>
{/each}