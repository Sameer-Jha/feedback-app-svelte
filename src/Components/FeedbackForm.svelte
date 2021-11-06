<script>
    import Card from './Card.svelte'
    import Button from './Button.svelte'

    let text = ''
    let rating = 10
    let btnDisabled = true
    let min = 10
    let message
</script>

<form>
    <Card>
    <div class="input-group">
        <input type="text" placeholder="Tell us about your experience...">
        <Button>Send</Button>
    </div>
</Card>
</form>

<style>
     header {
    max-width: 400px;
    margin: auto;
  }
  header h2 {
    font-size: 22px;
    font-weight: 600;
    text-align: center;
  }
  .input-group {
    display: flex;
    flex-direction: row;
    border: 1px solid #ccc;
    padding: 15px 25px;
    border-radius: 8px;
    margin-top: 15px;
  }
  input {
    flex-grow: 2;
    border: none;
    font-size: 16px;
  }
  input:focus {
    outline: none;
  }
  .message{
    padding-top: 10px;
    text-align: center;
    color: rebeccapurple;
  }
</style>