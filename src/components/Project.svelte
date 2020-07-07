<script>
  export let type;
  export let title;
  export let description;
  export let cards;
</script>

<style type="text/scss">
  section {
    display: flex;
    margin: 448px 0;
    min-height: 480px;

    &:nth-child(even) {
      flex-direction: row;

      aside {
        border-radius: 0 4px 35px 0;
      }
    }

    &:nth-child(odd) {
      flex-direction: row-reverse;

      aside {
        border-radius: 4px 0 0 35px;
      }
    }
  }

  aside {
    flex: 52;
    background: #20bf55;
  }

  article {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    flex: 48;

    > * {
      float: right;
      width: 536px;
      margin: 0 136px 0 112px;
    }
  }

  h2 {
    margin-bottom: 8px;
  }

  h5 {
    color: #818181;
    font-size: 18px;
    letter-spacing: -0.16px;
    text-transform: uppercase;
  }

  h4 {
    margin: 8px 0 4px 0;
  }

  svg {
    width: 48px;
    height: 48px;
    padding: 11px;
    border-radius: 35px;
  }

  .project__cards {
    display: flex;
  }
</style>

<section>
  <aside />
  <article>
    <main>
      <h5>{type}</h5>
      <h2>{title}</h2>
      <p>{description}</p>
    </main>
    <div class="project__cards">
      {#each cards as card}
        <div class="project__card">
          <svg style="background: {card.color}33">
            <use xlink:href="/images.svg#{card.icon}" />
          </svg>
          <h4>{card.title}</h4>
          <p>{card.description}</p>
        </div>
      {/each}
    </div>
  </article>
</section>
