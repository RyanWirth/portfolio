<style type="text/scss">
  section {
    display: flex;
    height: 100vh;
  }

  article {
    flex: 1;
  }

  aside {
    flex: 1;
    background: #d0d0d0;
    border-bottom-left-radius: 35px;
  }

  p {
    font-size: 24px;
    font-weight: 600;
    line-height: 30px;
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

    font: normal 600 22px/70px "Poppins", Arial, Helvetica, sans-serif;
    letter-spacing: -0.2px;

    margin-right: 24px;
    padding: 0 56px;
  }
</style>

<section>
  <article>
    <h1>Front-End Software Developer</h1>
    <p>
      Hand crafting unique world most beautiful gradients for your personal as
      well as commercial projects. For a low cost of zero dollars and
    </p>
    <div class="hero__buttons">
      <a class="hero__button hero__button--get-started" href="/">Get Started</a>
      <a class="hero__button" href="/">
        <img src="/images/github.svg" alt="GitHub" />
      </a>
    </div>
  </article>
  <aside />
</section>
