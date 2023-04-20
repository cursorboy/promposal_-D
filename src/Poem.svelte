<script>
  import { Article } from 'spaper';

  const alphabet = 'abcdefghijklmnopqrstuvwxyz';
  const urlname = new URLSearchParams(window.location.search)
    .get('mn') ?? 'Blf'; // default to You
  const name = [...urlname]
    .map(c => {
      const nc = alphabet[alphabet.length - 1 - alphabet.indexOf(c.toLowerCase())];
      return c.toLowerCase() != c ? nc.toUpperCase() : nc;
    })
    .join('');
</script>

<div class="poem-container">
  <Article
    title="To {name}"
    border
  >
    <p>I spent too much time coding this</p>
    <p>But there's one thing I cannot miss</p>
    <p>And it's taking you to the prom</p>
    <p>and im so glad for our comms</p>
    <p>Oh god, im a nerd</p>
    <p>but i know thats what u wouldve preferrede</p>
    <p>pls lmk if its a yes</p>
    <p>And if it is im excited to see ur dress</p>
    <p>If you would like to say no</p>
    <p>Just tell me so (you can't)</p>
  </Article>
</div>

<style>
  .poem-container {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
  }

  p {
    margin: 0.5rem 0;
  }

  .poem-container :global(h1) {
    font-size: 2rem;
  }
</style>
