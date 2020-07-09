<script>
  export let title;
  export let description;
  export let action;
  export let links;
</script>

<style type="text/scss">
  footer {
    background: #20bf55;
  }

  aside {
    display: flex;
    justify-content: space-between;
    align-items: center;

    margin: 56px auto 0 auto;
    padding: 45px 72px;
    transform: translateY(-56px);

    width: calc(100% - 192px);
    max-width: 1200px;

    background: #fff;
    border-radius: 16px;
    box-shadow: 0 8px 16px rgba(#000, 0.16);

    svg {
      fill: #363636;
      width: 80px;
      height: 80px;
    }

    div {
      flex: 1;
      margin: 0 40px;
    }

    p {
      margin-top: 12px;
    }
  }

  main {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 32px 0 72px 0;
  }

  .footer__logo {
    fill: #fff;
    width: 108px;
    height: 50px;
  }

  .footer__buttons {
    display: flex;
    margin: 48px 0;

    a {
      margin: 0 16px;

      svg {
        fill: #fff;
        width: 48px;
        height: 48px;
      }
    }
  }

  .footer__copyright {
    color: #fff;
    font-size: 16px;
    opacity: 75%;

    span {
      font: normal bold 16px "Poppins", Arial, Helvetica, sans-serif;
    }
  }

  .footer__built-with-svelte {
    display: flex;
    align-items: center;

    font-size: 14px;
    letter-spacing: -0.44px;
    margin-top: 16px;

    opacity: 75%;
    transition: opacity 250ms ease-in-out;

    svg {
      width: 20px;
      height: 24px;
      margin-left: 4px;
    }

    &:hover {
      opacity: 100%;
    }
  }
</style>

<footer>
  <aside>
    <svg>
      <use xlink:href="/images/sprites.svg#footer-envelope" />
    </svg>
    <div>
      <h3>{title}</h3>
      <p>{description}</p>
    </div>
    <a class="global__button" href={action.href}>{action.label}</a>
  </aside>
  <main>
    <a href="https://ryanwirth.ca">
      <svg class="footer__logo">
        <use xlink:href="/images/sprites.svg#icon-logo" />
      </svg>
    </a>
    <div class="footer__buttons">
      {#each links as link}
        <a href={link.href}>
          <svg>
            <use xlink:href="/images/sprites.svg#{link.icon}" />
          </svg>
        </a>
      {/each}
    </div>
    <p class="footer__copyright">
      Handcrafted by me
      <span>©</span>
      twentytwenty
    </p>
    <a class="footer__built-with-svelte" href="https://svelte.dev">
      Built with
      <svg>
        <use xlink:href="/images/sprites.svg#footer-svelte" />
      </svg>
    </a>
  </main>
</footer>
