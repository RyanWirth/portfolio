<script>
  import Event from "./Event.svelte";

  export let title;
  export let description;
  export let events;

  let scrollY = 0;
  $: progress = 100;
</script>

<style type="text/scss">
  section {
    display: flex;

    margin: 0 auto;
    max-width: 1200px;
  }

  aside {
    display: flex;
    flex-direction: column;
    align-items: center;

    margin: 0 112px 0 48px;
  }

  svg {
    width: 94px;
    height: 81px;
    fill: #20bf55;
  }

  .timeline__track {
    width: 14px;
    height: 100%;
  }

  .timeline__track-fill {
    background: #20bf55;
    border-radius: 0 0 4px 4px;
  }
</style>

<svelte:window bind:scrollY />

<section>
  <aside>
    <svg>
      <use xlink:href="/images.svg#timeline-top-cap" />
    </svg>
    <div class="timeline__track">
      <div class="timeline__track-fill" style="height: {progress}%" />
    </div>
  </aside>
  <main>
    <h3>{title}</h3>
    <p>{description}</p>
    {#each events as event}
      <Event
        title={event.title}
        start={new Date(event.start)}
        end={new Date(event.end)}
        organization={event.organization}
        description={event.description}
        showStartAsTimestamp={event.showStartAsTimestamp}
        showYearInTimestamp={event.showYearInTimestamp} />
    {/each}
  </main>
</section>
