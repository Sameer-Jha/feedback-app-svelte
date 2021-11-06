<script>
    export let feedback;
    import Card from './Card.svelte'
</script>

<Card>
<div class="card-content">
    <div class="card-top">
        <h3 class="rating">{feedback.rating}</h3>
        <p>{feedback.text}</p>
        <button class="delete">X</button>
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
    }
</style>