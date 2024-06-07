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
    <p>I always wondered what hurt the most</p>
    <p>whether it was seeing you move on or the ways you talked about me</p>
    <p>I think it was, after our 2 years, you showed nothing but resentment</p>
    <p>Since the brekaup, I heard so much about you. the shitty things you said about me </p>
    <p>all those reposts I used to once stalk, the things you told others about me, some true, some untrue</p>
    <p>I am not trying to play victim, i just had some frustrations, I know i was far from perfect, but tbf I had loved you to the ends of the earth</p>
    <p>I NEVER meant to hurt you so deeply if I did</p>
    <p>From the bottom of my heart, I am sorry</p>
    <p>the lies, everything</p>
    <p>I am not hear to pick fights or anything</p>
    <p>If money was the issue, I never meant to make you feel like I conned you out of money</p>
    <p>So if you're reading this whether it be a fluke or something itched in the back of your brain</p>
    <p>I will go ahead and pay you back for the switch, just contact me saying you read this message</p>
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
