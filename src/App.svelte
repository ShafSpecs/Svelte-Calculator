<script lang="ts">
  import logo from "./assets/svelte.png";
  import Screen from "./lib/Screen.svelte";
  import Key from "./lib/Key.svelte";

  let calculatorValue = 0

  function displayClicked () {
    console.log("display clicked");
  }
</script>

<header>
  <img src={logo} alt="Svelte" />&nbsp;Svelte Calculator
</header>
<main class="calculator">
  <Screen value={calculatorValue}/>
  <table>
    <tr>
      <Key />
      <Key />
      <Key />
      <Key />
    </tr>
    <tr>
      <Key />
      <Key />
      <Key />
      <Key />
    </tr>
    <tr>
      <Key />
      <Key />
      <Key />
      <Key />
    </tr>
    <tr>
      <Key />
      <Key />
      <Key />
      <Key />
    </tr>
  </table>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  header {
    background: #222;
    color: #fff;
    padding: 0.825rem;
    font-size: 1.5rem;
    font-weight: 500;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    width: auto;
  }

  main {
    text-align: center;
    padding: 0.325rem;
    margin: calc(50vh - 15rem) auto 0 auto;
    border: 1px solid #222;
    width: 45%;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    border-spacing: 0;
    font-size: 1.5rem;
    user-select: none;
  }

  tr {
    border-bottom: 1px solid #222;
  }

  img {
    width: 1.625rem;
    height: 1.625rem;
  }
</style>
