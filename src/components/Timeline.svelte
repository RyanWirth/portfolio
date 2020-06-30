<script>
  import Event from "./Event.svelte";

  let scrollY = 0;
  $: progress = 100 * (scrollY / 7000);
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
    <h3>Here's a look at what I've been up to.</h3>
    <p>
      PicnicHealth collects, digitizes, and encrypts all your medical
      records—then arranges everything in one intuitive timeline. No need to
      worry about a note from your doctor or the results from a lab. It’s all
      there for easy reference, right when you need it.
    </p>

    <Event
      title="Software Developer Intern"
      start={new Date('Sep 5, 2017')}
      end={new Date('Aug 28, 2018')}
      organization="SMART Technologies"
      description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis
      ac nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim
      tortor eget vestibulum vulputate." />

    <Event
      title="Front-End Developer Intern"
      start={new Date('May 7, 2019')}
      end={new Date('Aug 30, 2019')}
      organization="Mobify"
      description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis
      ac nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim
      tortor eget vestibulum vulputate." />

    <Event
      title="B.Sc. in Computer Science"
      start={new Date('Sep 5, 2015')}
      end={new Date('Apr 28, 2020')}
      organization="University of British Columbia"
      description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis
      ac nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim
      tortor eget vestibulum vulputate." />

    <Event
      title="Forward-Deployed Engineer"
      start={new Date('Sep 14, 2020')}
      organization="Palantir Technologies"
      description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis
      ac nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim
      tortor eget vestibulum vulputate." />
  </main>
</section>
