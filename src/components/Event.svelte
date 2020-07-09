<script>
  export let title;
  export let organization;
  export let start;
  export let end;
  export let description;
  export let position;

  export let showYearInTimestamp = true;
  export let showStartAsTimestamp = true;

  let el = { offsetTop: 0, offsetHeight: 1 };
  $: progress = (position - el.offsetTop) / el.offsetHeight * 1.5;
  $: opacity = Math.min(Math.max(progress, 0), 1);
  $: translation = (1 - opacity) * 10;

  $: timestamp = showStartAsTimestamp ? start : end;
  $: timestampDay = timestamp.getDate();
  $: timestampYear = timestamp.getFullYear();
  $: timestampMonth = timestamp.toLocaleString("default", { month: "short" });

  $: image = organization.replace(/ /g, "-").toLowerCase();

  // `true` if the start and end dates fall in the same year.
  $: sameYear = !end || start.getFullYear() !== end.getFullYear();

  // eg. "Sep 2020"
  $: startDate = start.toLocaleString("default", {
    month: "short",
    year: sameYear ? "numeric" : undefined
  });

  // eg. "Oct 2020" or "Present", if the end date is undefined
  $: endDate = end
    ? end.toLocaleString("default", {
        month: "short",
        year: "numeric"
      })
    : "Present";
</script>

<style type="text/scss">
  article {
    display: flex;
    align-items: center;

    position: relative;
    margin: 248px 0 160px 0;
    transition: opacity 500ms ease-out;

    > div {
      transition: transform 500ms ease-out;
    }
  }

  .event__timestamp {
    display: flex;
    flex-direction: column;
    align-items: center;

    position: absolute;
    left: -212px;
    top: -96px;
  }

  .event__timestamp-year {
    display: none;
    margin-bottom: 30px;
    padding: 6px 12px;

    background: #093819;
    border-radius: 5px;
    color: #fff;

    &.visible {
      display: inline-block;
    }
  }

  .event__timestamp-date {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    width: 88px;
    height: 88px;

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

  .event__image {
    flex: 0 0 243px;
    margin-right: 128px;
  }

  h6 {
    margin-bottom: 8px;
  }
</style>

<article style="opacity: {opacity}" bind:this={el}>
  <div class="event__timestamp">
    <h5 class="event__timestamp-year {showYearInTimestamp && 'visible'}">
      {timestampYear}
    </h5>
    <div class="event__timestamp-date">
      <small>{timestampMonth}</small>
      <strong>{timestampDay}</strong>
    </div>
  </div>
  <div class="event__image" style="transform: translateX({translation}%)">
    <svg>
      <use xlink:href="/images.svg#timeline-{image}" />
    </svg>
  </div>
  <div class="event__details" style="transform: translateX({translation}%)">
    <h4>{title}</h4>
    <h6>{organization} &bull; {startDate} &mdash; {endDate}</h6>
    <p>{description}</p>
  </div>
</article>
