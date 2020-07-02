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
    <a
      class="global__button global__button--large"
      href="mailto:ryan@ryanwirth.ca">
      Say Hello
    </a>
  </aside>
  <main>World</main>
</footer>
