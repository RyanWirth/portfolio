<script>
  import Header from "./components/Header.svelte";
  import Hero from "./components/Hero.svelte";
  import Skills from "./components/Skills.svelte";
  import Timeline from "./components/Timeline.svelte";
  import Project from "./components/Project.svelte";
  import Footer from "./components/Footer.svelte";
</script>

<Header />
<Hero />
<Skills />
<Timeline />
<Project
  type="Mobile"
  title="Kenko"
  description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ac
  nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim tortor
  eget vestibulum vulputate. Amsterdam consequat blandit dolor sit amet, ac
  nulla fringilla lectus in."
  cards={[{ icon: 'icon-logo', title: 'Native Mobile', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.' }, { icon: 'icon-logo', title: 'Cloud Firestore', description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.' }]} />
<Footer />
