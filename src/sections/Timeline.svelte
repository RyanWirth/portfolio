<script>
  import Event from "../components/Event.svelte";

  export let title;
  export let description;
  export let events;

  let scrollY = 0;
  let innerHeight = 0;
  $: position = scrollY + innerHeight * 0.65;

  let el = { offsetTop: 0, offsetHeight: 1 };
  $: progress = (position - el.offsetTop) / el.offsetHeight;
  $: height = Math.min(Math.max(progress, 0), 1) * 100;
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

  main {
    margin-top: 16px;
  }

  p {
    margin: 16px 0 -32px 0;
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
    min-height: 40px;

    background: #20bf55;
    transition: height 500ms ease-in-out;
  }
</style>

<svelte:window bind:innerHeight bind:scrollY />

<section>
  <aside bind:this={el}>
    <svg class="timeline__top-cap">
      <use xlink:href="/images/sprites.svg#timeline-top-cap" />
    </svg>
    <div class="timeline__track" style="height: {height}%" />
    <svg class="timeline__bottom-cap">
      <use xlink:href="/images/sprites.svg#timeline-bottom-cap" />
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
        {innerHeight}
        {position} />
    {/each}
  </main>
</section>
