<script>
  export let type;
  export let title;
  export let description;
  export let cards;
</script>

<style type="text/scss">
  article {
    display: flex;
    margin: 144px 0 448px 0;
    min-height: 480px;

    &:nth-child(even) {
      flex-direction: row;

      aside {
        border-radius: 0 4px 35px 0;
      }

      main {
        align-items: flex-start;
      }
    }

    &:nth-child(odd) {
      flex-direction: row-reverse;

      aside {
        border-radius: 4px 0 0 35px;
      }

      main {
        align-items: flex-end;
      }
    }
  }

  aside {
    flex: 52;
    background: #20bf55;
  }

  main {
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    flex: 48;

    > div {
      float: right;
      width: 536px;
      margin: 0 136px 0 112px;
    }
  }

  h2 {
    margin-bottom: 8px;
  }

  h4 {
    margin: 8px 0 4px 0;
  }

  h5 {
    color: #818181;
    font-size: 18px;
    letter-spacing: -0.16px;
    text-transform: uppercase;
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

<article>
  <aside />
  <main>
    <div>
      <h5>{type}</h5>
      <h2>{title}</h2>
      <p>{description}</p>
    </div>
    <div class="project__cards">
      {#each cards as card}
        <div>
          <svg style="background: {card.color}33">
            <use xlink:href="/images.svg#{card.icon}" />
          </svg>
          <h4>{card.title}</h4>
          <p>{card.description}</p>
        </div>
      {/each}
    </div>
  </main>
</article>
