<script>
  export let title;
  export let cards;
</script>

<style type="text/scss">
  section {
    margin: 224px auto;
    max-width: 1200px;
  }

  svg {
    width: 128px;
    height: 93px;
  }

  h2 {
    width: 520px;
    margin: 0 auto;
    text-align: center;

    &:after {
      display: block;
      content: " ";

      margin: 40px auto 0 auto;

      width: 58px;
      height: 6px;
      background: #20bf55;
      border-radius: 3px;
    }
  }

  h4 {
    margin: 32px 0 16px 0;
  }

  .skills__container {
    display: flex;
    justify-content: center;
    margin: 104px 0;
  }

  .skills__item {
    flex: 0 340px;
    margin: 0 16px;
    text-align: center;
  }
</style>

<section>
  <h2>{title}</h2>
  <div class="skills__container">
    {#each cards as card}
      <div class="skills__item">
        <svg>
          <use xlink:href="/images/sprites.svg#{card.icon}" />
        </svg>
        <h4>{card.title}</h4>
        <p>{card.description}</p>
      </div>
    {/each}
  </div>
</section>
