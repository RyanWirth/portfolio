<style type="text/scss">
  section {
    display: flex;

    height: 100vh;
    max-height: 1200px;
  }

  article {
    flex: 48;

    > div {
      float: right;
      width: 520px;
      margin: 0 136px 0 112px;
    }
  }

  aside {
    flex: 52;
    background: #20bf55;
    border-bottom-left-radius: 35px;
  }

  h1 {
    margin: 320px 0 64px 0;
  }

  p {
    font-size: 24px;
    font-weight: 600;
    line-height: 30px;
    margin: 64px 0 104px 0;
  }

  .hero__buttons {
    display: flex;
    flex-direction: row;
  }

  .hero__button {
    border-radius: 35px;
    height: 70px;
  }

  .hero__button--get-started {
    background: #d0d0d0;
    color: #fff;

    font-size: 22px;
    font-weight: 600;
    line-height: 70px;
    letter-spacing: -0.2px;

    margin-right: 24px;
    padding: 0 56px;
  }

  .hero__button--github {
    width: 70px;

    svg {
      height: inherit;
      width: inherit;

      fill: #d0d0d0;
      transition: fill 250ms ease-in-out;

      &:hover {
        fill: #121212;
      }
    }
  }
</style>

<section>
  <article>
    <div>
      <h1>Front-End Software Developer</h1>
      <p>
        Hand crafting unique world most beautiful gradients for your personal as
        well as commercial projects. For a low cost of zero dollars and
      </p>
      <div class="hero__buttons">
        <a class="hero__button hero__button--get-started" href="/">
          Get Started
        </a>
        <a
          class="hero__button hero__button--github"
          href="https://github.com/RyanWirth">
          <svg>
            <use xlink:href="/images.svg#icon-github" />
          </svg>
        </a>
      </div>
    </div>
  </article>
  <aside />
</section>
