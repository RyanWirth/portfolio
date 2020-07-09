<script>
  import Event from "../components/Event.svelte";

  export let title;
  export let description;
  export let events;

  let scrollY = 0;
  let innerHeight = 0;
  $: position = scrollY + innerHeight * 0.65;

  let track = { offsetTop: 0, offsetHeight: 1 };
  $: height = Math.max(0, (position - track.offsetTop) / track.offsetHeight);
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

  .timeline__top-cap {
    width: 94px;
    height: 81px;
    fill: #20bf55;
  }

  .timeline__bottom-cap {
    width: 32px;
    height: 48px;
    fill: #20bf55;
    margin-top: -3px;
  }

  .timeline__track {
    width: 14px;
    height: 100%;
  }

  .timeline__track-fill {
    background: #20bf55;
    border-radius: 0 0 4px 4px;

    min-height: 40px;
    max-height: 100%;
    transition: height 500ms ease-out;
  }
</style>

<svelte:window bind:innerHeight bind:scrollY />

<section>
  <aside>
    <svg class="timeline__top-cap">
      <use xlink:href="/images.svg#timeline-top-cap" />
    </svg>
    <div class="timeline__track" bind:this={track}>
      <div class="timeline__track-fill" style="height: {height * 100}%" />
    </div>
    <svg class="timeline__bottom-cap">
      <use xlink:href="/images.svg#timeline-bottom-cap" />
    </svg>
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
        showYearInTimestamp={event.showYearInTimestamp}
        scrollPosition={position} />
    {/each}
  </main>
</section>
