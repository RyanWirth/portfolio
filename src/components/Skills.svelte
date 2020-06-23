<style type="text/scss">
  section {
    margin: 224px 0;
  }

  h2 {
    width: 520px;
    margin: 0 auto;
    text-align: center;

    &:after {
      display: block;
      content: " ";

      margin: 40px auto 0 auto;

      width: 58px;
      height: 6px;
      background: #20bf55;
      border-radius: 3px;
    }
  }

  h4 {
    margin: 32px 0 16px 0;
  }

  .skills__container {
    display: flex;
    justify-content: center;
    margin: 104px 0;
  }

  .skills__item {
    flex: 0 340px;
    margin: 0 16px;
    text-align: center;
  }

  .skills__item--web-developer svg {
    width: 128px;
    height: 93px;
  }
</style>

<section>
  <h2>Building awesome, one commit at a time.</h2>
  <div class="skills__container">
    <div class="skills__item skills__item--web-developer">
      <svg>
        <use xlink:href="/images.svg#icon-web-developer" />
      </svg>
      <h4>Paperwork is out</h4>
      <p>Flip through your complete records with the tap of a button.</p>
    </div>
    <div class="skills__item skills__item--web-developer">
      <svg>
        <use xlink:href="/images.svg#icon-web-developer" />
      </svg>
      <h4>A chronology of care</h4>
      <p>Keep organized with a timeline of your entire health history.</p>
    </div>
    <div class="skills__item skills__item--web-developer">
      <svg>
        <use xlink:href="/images.svg#icon-web-developer" />
      </svg>
      <h4>You are in control</h4>
      <p>Review and share -- all on your own terms.</p>
    </div>
  </div>
</section>
