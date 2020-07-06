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
<Timeline
  title="Here's a look at what I've been up to."
  description="PicnicHealth collects, digitizes, and encrypts all your medical
  records—then arranges everything in one intuitive timeline. No need to
  worry about a note from your doctor or the results from a lab. It’s all
  there for easy reference, right when you need it."
  events={[
    {
      title: 'Software Developer Intern',
      start: 'Sep 5, 2017',
      end: 'Aug 28, 2018',
      organization: 'SMART Technologies',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ac nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim tortor eget vestibulum vulputate.'
    },
    {
      title: 'Front-End Developer Intern',
      start: 'May 7, 2019',
      end: 'Aug 30, 2019',
      organization: 'Mobify',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ac nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim tortor eget vestibulum vulputate.'
    },
    {
      title: 'B.Sc. in Computer Science',
      start: 'Sep 5, 2015',
      end: 'Apr 29, 2020',
      organization: 'University of British Columbia',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ac nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim tortor eget vestibulum vulputate.',
      showStartAsTimestamp: false
    },
    {
      title: 'Forward-Deployed Engineer',
      start: 'Sep 14, 2020',
      organization: 'Palantir Technologies',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ac nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim tortor eget vestibulum vulputate.',
      showYearInTimestamp: false
    }
  ]} />
<Project
  type="Mobile"
  title="Kenko"
  description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ac
  nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim tortor
  eget vestibulum vulputate. Amsterdam consequat blandit dolor sit amet, ac
  nulla fringilla lectus in."
  cards={[
    {
      icon: 'icon-github',
      title: 'Native Mobile',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
    {
      icon: 'icon-facebook',
      title: 'Cloud Firestore',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    }
  ]} />
<Project
  type="Desktop"
  title="PokemOnline"
  description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis ac
  nulla consequat, fringilla lectus in, blandit tortor. Aliquam dignissim tortor
  eget vestibulum vulputate. Amsterdam consequat blandit dolor sit amet, ac
  nulla fringilla lectus in."
  cards={[
    {
      icon: 'icon-mail',
      title: 'Native Mobile',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
    {
      icon: 'icon-instagram',
      title: 'Cloud Firestore',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    }
  ]} />
<Footer />
