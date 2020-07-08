<script>
  import Project from "./Project.svelte";

  export let title;
  export let description;
  export let projects;
</script>

<style type="text/scss">
  section {
    margin-top: 128px;
  }

  h2 {
    text-align: center;
  }

  p {
    margin-top: 16px;
    text-align: center;
  }
</style>

<section>
  <h2>{title}</h2>
  <p>{description}</p>

  {#each projects as project}
    <Project
      type={project.type}
      title={project.title}
      description={project.description}
      cards={project.cards} />
  {/each}
</section>
