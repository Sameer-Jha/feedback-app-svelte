<script>
    export let feedback;
    import Card from './Card.svelte'
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();

    const handleDelete = (id) => {
        dispatch('delete-feedback', id);
    }
    // import Icon from 'svelte-awesome/components/Icon';
    // import { faTimes } from "@fortawesome/free-solid-svg-icons/faTimes";
</script>

<Card>
<div class="card-content">
    <div class="card-top">
        <h3 class="rating">{feedback.rating}</h3>
        <p>{feedback.text}</p>
        <button class="delete" on:click={() => handleDelete(feedback.id)}>X</button>
    </div>
</div>
</Card>

<style>
    .card-content{
        padding: 20px 10px;
        text-align: center;
    }

    .card-content .card-top{
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    .card-content .card-top .rating{
        background-color: #f72585;
        width: 50px;
        height: 50px;
        color: white;
        border-radius: 50%;
        border: 2px solid white;
        padding: 10px;
    }

    .card-content .card-top button{
        background: none;
        border: none;
        cursor: pointer;
        color: white;
        transition: all 0.2s ease 0.5s;
    }

    .card-content .card-top button:hover{
        color: #f72585;
        transition: all 0.1s ease 0.2s;
    }
</style>