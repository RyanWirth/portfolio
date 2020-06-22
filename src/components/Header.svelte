<style type="text/scss">
  header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    position: absolute;
    margin: 0 auto;
    left: 0;
    right: 0;

    width: 100%;
    max-width: 1600px;
  }

  nav a {
    font: normal 600 20px "Poppins", Arial, Helvetica, sans-serif;
    letter-spacing: -1px;
    margin: 0 24px;
  }

  .header__logo {
    width: 108px;
    height: 40px;
  }
</style>

<header>
  <a href="/">
    <svg class="header__logo">
      <use xlink:href="/images.svg#icon-logo" />
    </svg>
  </a>
  <nav>
    <a href="/">Home</a>
    <a href="/">Skills</a>
    <a href="/">Work</a>
    <a href="/">Projects</a>
    <a href="/">Contact</a>
  </nav>
</header>
