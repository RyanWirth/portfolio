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
    margin: 256px 0;
  }

  svg {
    flex: 0 0 243px;
    margin-right: 128px;
  }
</style>

<article>
  <svg>
    <use xlink:href="/images.svg#timeline-smart" />
  </svg>
  <div class="event__details">
    <h4>{title}</h4>
    <h6>{organization} &bull; {start} &mdash; {end}</h6>
    <p>{description}</p>
  </div>
</article>
