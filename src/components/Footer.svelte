<style type="text/scss">
  footer {
    background: #20bf55;
  }

  aside {
    display: flex;
    justify-content: space-between;
    align-items: center;

    margin: 0 auto;
    padding: 45px 72px;
    transform: translateY(-33%);

    width: 100%;
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
      margin-left: 40px;
    }

    p {
      margin-top: 12px;
    }
  }

  main {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .footer__logo {
    fill: #fff;
    width: 108px;
    height: 50px;
  }

  .footer__buttons {
    display: flex;

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

    span {
      font: normal bold 16px "Poppins", Arial, Helvetica, sans-serif;
    }
  }

  .footer__built-with-svelte {
    display: flex;
    align-items: center;

    font-size: 14px;
    letter-spacing: -0.44px;

    svg {
      width: 20px;
      height: 24px;
      margin-left: 4px;
    }
  }
</style>

<footer>
  <aside>
    <svg>
      <use xlink:href="/images.svg#footer-envelope" />
    </svg>
    <div>
      <h3>Get in touch.</h3>
      <p>
        Got a question? A feature request for one of my projects? I’d like to
        hear from you!
      </p>
    </div>
    <a class="global__button" href="mailto:ryan@ryanwirth.ca">Say Hello</a>
  </aside>
  <main>
    <a href="https://ryanwirth.ca/">
      <svg class="footer__logo">
        <use xlink:href="/images.svg#icon-logo" />
      </svg>
    </a>
    <div class="footer__buttons">
      <a href="https://github.com/RyanWirth">
        <svg>
          <use xlink:href="/images.svg#icon-github" />
        </svg>
      </a>
      <a href="https://github.com/RyanWirth">
        <svg>
          <use xlink:href="/images.svg#icon-github" />
        </svg>
      </a>
      <a href="https://github.com/RyanWirth">
        <svg>
          <use xlink:href="/images.svg#icon-github" />
        </svg>
      </a>
      <a href="https://github.com/RyanWirth">
        <svg>
          <use xlink:href="/images.svg#icon-github" />
        </svg>
      </a>
      <a href="https://github.com/RyanWirth">
        <svg>
          <use xlink:href="/images.svg#icon-github" />
        </svg>
      </a>
    </div>
    <p class="footer__copyright">
      Handcrafted by me
      <span>©</span>
      twentytwenty
    </p>
    <a class="footer__built-with-svelte" href="https://svelte.dev/">
      Built with
      <svg>
        <use xlink:href="/images.svg#footer-svelte" />
      </svg>
    </a>
  </main>
</footer>
