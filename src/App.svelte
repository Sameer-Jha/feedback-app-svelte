<script>
	import Nav from './Components/Nav.svelte'
	import FeedbackDisplay from './Components/FeedbackList.svelte'

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
</script>

<main class="container">
	<Nav />
	<h1>Hello!</h1>
	<FeedbackDisplay feedbacks={feedbacks}/>
	
</main>


