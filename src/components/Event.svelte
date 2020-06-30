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
    left: -212px;
  }

  .event__timestamp-year {
    display: inline-block;

    margin-bottom: 30px;
    padding: 6px 12px;

    background: #093819;
    border-radius: 5px;
    color: #fff;
  }

  .event__timestamp-date {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    width: 85px;
    height: 85px;

    background: #fff;
    border: 10px solid #f3f3f3;
    border-radius: 100%;

    small {
      font: normal 600 11px "Poppins", Arial, Helvetica, sans-serif;
      text-transform: uppercase;
    }

    strong {
      font: normal bold 32px/32px "Poppins", Arial, Helvetica, sans-serif;
    }
  }

  svg {
    flex: 0 0 243px;
    margin-right: 128px;
  }
</style>

<article>
  <div class="event__timestamp">
    <h5 class="event__timestamp-year">2017</h5>
    <div class="event__timestamp-date">
      <small>Oct</small>
      <strong>23</strong>
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
