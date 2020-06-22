<style type="text/scss">
  header {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

    position: absolute;
    margin: 0 auto;
    padding: 48px 36px;
    left: 0;
    right: 0;

    max-width: 1600px;
  }

  a {
    margin: 8px 12px;
    padding: 4px 12px;

    font: normal 600 20px "Poppins", Arial, Helvetica, sans-serif;
    letter-spacing: -1px;
  }

  svg {
    width: 108px;
    height: 40px;
  }
</style>

<header>
  <a href="/">
    <svg>
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
