<script>
  export let type;
  export let title;
  export let description;
  export let cards;
</script>

<style type="text/scss">
  section {
    display: flex;
    flex-direction: row-reverse;

    margin: 224px 0;
    min-height: 480px;
  }

  aside {
    flex: 52;
    background: #20bf55;
    border-top-left-radius: 4px;
    border-bottom-left-radius: 35px;
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

    background: rgba(255, 204, 50, 0.2);
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
          <svg>
            <use xlink:href="/images.svg#{card.icon}" />
          </svg>
          <h4>{card.title}</h4>
          <p>{card.description}</p>
        </div>
      {/each}
    </div>
  </article>
</section>
