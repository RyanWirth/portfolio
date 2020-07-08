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
    transition: fill 250ms ease-in-out;

    &:hover {
      fill: #20bf55;
    }
  }

  svg {
    width: 108px;
    height: 40px;
  }

  nav {
    display: flex;
    flex-direction: row;

    a {
      &:after {
        display: block;
        content: "";

        border-bottom: solid 2px #fff;
        transform: scaleX(0);
        transition: transform 250ms ease-in-out;
      }

      &:hover:after {
        transform: scaleX(1);
      }
    }
  }
</style>

<header>
  <a href="/">
    <svg>
      <use xlink:href="/images.svg#icon-logo" />
    </svg>
  </a>
  <nav>
    <a href="/">Skills</a>
    <a href="/">Timeline</a>
    <a href="/">Projects</a>
    <a href="/">Contact</a>
  </nav>
</header>
