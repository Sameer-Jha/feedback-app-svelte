<script>
	import Nav from './Components/Nav.svelte'
	import FeedbackDisplay from './Components/FeedbackList.svelte'
	import FeedbackStats from './Components/FeedbackStats.svelte'

	let feedbacks = [
		{
			id: 1,
			rating: 8,
			text: "I really like the product and definately recommend it."
		},
		{
			id: 2,
			rating: 9,
			text: "I really like the product and definately recommend it."
		},
		{
			id: 3,
			rating: 10,
			text: "I really like the product and definately recommend it."
		}
	]

	const handleDeletion = (e) => {
		let itemId = e.detail;
		feedbacks = feedbacks.filter((item) => item.id != itemId);
	} 

	$: count = feedbacks.length;
	$: average = feedbacks.reduce((a, {rating}) => a+rating, 0) / feedbacks.length;

</script>

<main class="container">
	<Nav />
	<FeedbackStats {count} {average} />
	<FeedbackDisplay feedbacks={feedbacks} on:delete-feedback-forward={handleDeletion}/>
	
	
</main>


