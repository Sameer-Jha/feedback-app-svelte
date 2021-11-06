<script>
    export let feedbacks = [];
	import FeedbackItem from './FeedbackItem.svelte'
	import { createEventDispatcher } from 'svelte';
	const dispatch = createEventDispatcher();

	const forward = (e) =>{
		dispatch('delete-feedback-forward', e.detail);
	}
</script>

{#each feedbacks as feedback (feedback.id)}
		<FeedbackItem {feedback} on:delete-feedback={forward}/>
{/each}