<script>
  import Block from "./lib/Block.svelte";

  let color;
  let title;
  let action;

  let index = -1;
  const handler = () => {
    index += 1;
    index = index % 3;

    switch (index) {
      case 0:
        color = "red";
        title = "Red";

        action = "I have written a test to drive implementation";
        break;
      case 1:
        color = "green";
        title = "Green";

        action = "I have written minimal implementation code";
        break;
      case 2:
        color = "blue";
        title = "Refactor";

        action = "I have refactored implementation and test code";
        break;
      default:
        console.error("unreachable code");
    }
  };

  handler();
</script>

<main on:click={handler}>
  <Block {color} {title} {action} />
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }
</style>
