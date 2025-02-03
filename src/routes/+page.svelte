<script>
  import AboutMe from "../components/home/about/AboutMe.svelte";
  import ContactMe from "../components/home/contact/ContactMe.svelte";
  import MyExperience from "../components/home/experience/MyExperience.svelte";
  import Hero from "../components/home/hero/Hero.svelte";
  import MyProjects from "../components/home/projects/MyProjects.svelte";
  import MySkills from "../components/home/skills/MySkills.svelte";
</script>

<section class="hero-background flex flex-col items-center justify-center">
  <div class="max-w-3xl w-full">
    <Hero />
    <AboutMe />
    <MyProjects />
    <MySkills />
    <MyExperience />
    <ContactMe />
  </div>
</section>
