<script>
  export let color;
  export let title;
  export let action;
</script>

<div style="background-color: {color};">
  <h1>{title}</h1>

  <button>{action}</button>
</div>

<style>
  div {
    display: flex;
    flex-direction: column;

    align-items: center;
    justify-content: center;

    width: 100vw;
    height: 100vh;

    padding: 0;
    margin: 0;
  }

  button {
    border-radius: 0.2em;
    padding: 0.4em 1em;
    background-color: #dddddd;
    border-style: none;
    font-weight: bold;
  }
</style>
