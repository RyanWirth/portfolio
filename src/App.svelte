<script>
  import Header from "./components/Header.svelte";
  import Hero from "./components/Hero.svelte";
  import Skills from "./components/Skills.svelte";
  import Timeline from "./components/Timeline.svelte";
  import Project from "./components/Project.svelte";
  import Footer from "./components/Footer.svelte";
</script>

<Header />

<Hero
  title="Front-End Software Developer"
  description="Hand crafting unique world most beautiful gradients for your
  personal as well as commercial projects. For a low cost of zero dollars
  and" />

<Skills
  title="Building awesome, one commit at a time."
  cards={[
    {
      icon: 'icon-web-developer',
      title: 'Paperwork is out',
      description: 'Flip through your complete records with the tap of a button.'
    },
    {
      icon: 'icon-web-developer',
      title: 'A chronology of care',
      description: 'Keep organized with a timeline of your entire health history.'
    },
    {
      icon: 'icon-web-developer',
      title: 'You are in control.',
      description: 'Review and share &mdash; all on your own terms.'
    }
  ]} />

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
      color: '#ff6600',
      icon: 'icon-github',
      title: 'Native Mobile',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
    {
      color: '#0000ff',
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
      color: '#20bf55',
      icon: 'icon-mail',
      title: 'Native Mobile',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
    {
      color: '#20bf55',
      icon: 'icon-instagram',
      title: 'Cloud Firestore',
      description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    }
  ]} />

<Footer
  title="Get in touch."
  description="Got a question? A feature request for one of my projects? I'd
  like to hear from you!"
  action={{ label: 'Say Hello', href: 'mailto:ryan@ryanwirth.ca' }}
  links={[
    {
      icon: 'icon-facebook',
      href: 'https://facebook.com/ryankwirth'
    },
    {
      icon: 'icon-instagram',
      href: 'https://instagram.com/ryankwirth'
    },
    {
      icon: 'icon-linkedin',
      href: 'https://www.linkedin.com/in/ryankwirth/'
    },
    {
      icon: 'icon-github',
      href: 'https://github.com/RyanWirth'
    },
    {
      icon: 'icon-mail',
      href: 'mailto:ryan@ryanwirth.ca'
    }
  ]} />
