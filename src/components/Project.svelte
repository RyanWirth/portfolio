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
    width: 70px;
    height: 70px;

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
      <h5>Mobile</h5>
      <h2>Kenko</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ac nulla
        consequat, fringilla lectus in, blandit tortor. Aliquam dignissim tortor
        eget vestibulum vulputate. Amsterdam consequat blandit dolor sit amet,
        ac nulla fringilla lectus in.
      </p>
    </main>
    <div class="project__cards">
      <div class="project__card">
        <svg />
        <h4>Cloud Firestore</h4>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
      </div>
      <div class="project__card">
        <svg />
        <h4>Cloud Firestore</h4>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
      </div>
    </div>
  </article>
</section>
