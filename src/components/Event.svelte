<script>
  export let title;
  export let organization;
  export let start;
  export let end;
  export let description;
</script>

<style type="text/scss">
  article {
    display: flex;
    align-items: center;

    position: relative;
    margin: 256px 0;
  }

  .event__timestamp {
    display: flex;
    flex-direction: column;
    align-items: center;

    position: absolute;
    left: -221px;
  }

  .event__timestamp-year {
    display: inline-block;

    margin-bottom: 30px;
    padding: 10px 15px;

    background: #093819;
    border-radius: 5px;
  }

  .event__timestamp-date {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    width: 105px;
    height: 105px;

    background: #fff;
    border: 10px solid #f3f3f3;
    border-radius: 100%;
  }

  svg {
    flex: 0 0 243px;
    margin-right: 128px;
  }
</style>

<article>
  <div class="event__timestamp">
    <div class="event__timestamp-year">2017</div>
    <div class="event__timestamp-date">
      <small>Sep</small>
      <strong>26</strong>
    </div>
  </div>
  <svg>
    <use xlink:href="/images.svg#timeline-smart" />
  </svg>
  <div class="event__details">
    <h4>{title}</h4>
    <h6>{organization} &bull; {start} &mdash; {end}</h6>
    <p>{description}</p>
  </div>
</article>
