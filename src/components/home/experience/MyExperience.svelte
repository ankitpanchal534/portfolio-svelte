<script>
  import { fade, fly, slide } from "svelte/transition";

  const experiences = [
    {
      year: "June 2024 - Present",
      title: "Software Engineer II - Frontend",
      company: "Orufy Technologies Pvt. Ltd.",
      description:
        "Led a team of developers, increasing team velocity by 35% through efficient sprint planning. Architected and deployed a template building system with a real-time preview for multi-channel marketing campaigns, boosting user engagement by 40%. Reduced application load times by 40% through code splitting and bundle size optimization. Working on 3 major projects for the company.",
    },
    {
      year: "Nov 2023 – June 2024",
      title: "Frontend Developer",
      company: "Flathalt Technologies Pvt Ltd",
      description:
        "Architected a scalable and responsive property rental platform, delivering a seamless user experience across devices. Designed an advanced search system with multi-criteria filtering for location, price, and amenities, ensuring intuitive property discovery. Engineered immersive property detail pages with interactive maps, high-resolution image galleries, and real-time updates. Optimized platform performance using lazy loading, caching strategies, and modular component architecture for scalability.",
    },
    {
      year: "Jan 2022 - Oct 2023",
      title: "Frontend Developer",
      company: "Shorea Softech Pvt. Ltd.",
      description:
        "Developed and scaled React.js applications, achieving 10,000+ monthly active users with a focus on performance. Designed and implemented a Salon Management Software, serving 500+ active users with intuitive interfaces and seamless functionality. Enhanced page load speed by 40% through optimization techniques, improving overall user experience. Built a React Native application that secured a 4.5+ App Store rating, boosting user retention by 25%. Contributed to the development of a CRM Admin Portal, added reports for diff departments, capabilities and features for efficient product management.",
    },
  ];
</script>

<section class="experience-section" id="experience">
  <div class="container" in:fly={{ y: 50, duration: 1000 }}>
    <h2 class="title" in:fade={{ duration: 800 }}>Experience</h2>

    <div class="timeline">
      {#each experiences as experience, i}
        <div class="year" in:fade={{ duration: 800, delay: 400 * (i + 1) }}>
          {experience.year}
        </div>

        <div class="card relative">
          <div class="rotating-circle"></div>
          <div class="experience-item">
            <div class="content">
              <h3 in:slide={{ duration: 800, delay: 500 * (i + 1) }}>
                {experience.title}
              </h3>
              <h4 in:slide={{ duration: 800, delay: 600 * (i + 1) }}>
                {experience.company}
              </h4>
              <p
                in:fade={{ duration: 800, delay: 700 * (i + 1) }}
                class="text-sm
            "
              >
                {experience.description}
              </p>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </div>
</section>

<style>
  .title {
    text-align: center;
    font-size: 2.5rem;
    margin-bottom: 3rem;
    color: #2d3436;
  }

  .timeline {
    position: relative;

    margin: 0 auto;
  }

  .timeline::before {
    content: "";
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    width: 2px;
    height: 100%;
    background: #3498db;
  }

  .experience-item {
    position: relative;
    margin-bottom: 3rem;
    /* width: calc(50% - 2rem); */
    padding: 1.5rem;
    background: white;
    border-radius: 24px;
    box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
    transition:
      transform 0.3s ease,
      box-shadow 0.3s ease;
  }

  .experience-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 25px rgba(0, 0, 0, 0.2);
  }

  .experience-item:nth-child(odd) {
    margin-left: auto;
  }

  .year {
    /* position: absolute; */
    /* top: 0; */
    /* background: #3498db; */
    /* color: white; */
    padding: 0.5rem 1rem;
    border-radius: 20px;
    font-weight: bold;
    transition: transform 0.3s ease;
  }
  /* 
  .experience-item:nth-child(odd) .year {
    left: 100%;
  } */

  /* .experience-item:nth-child(even) .year {
    right: 100%;
  } */

  .content h3 {
    color: #2d3436;
    margin-bottom: 0.5rem;
    transition: color 0.3s ease;
  }

  .content h4 {
    color: #3498db;
    margin-bottom: 1rem;
    transition: color 0.3s ease;
  }

  .content p {
    color: #636e72;
    line-height: 1.6;
  }

  .experience-item:hover h3 {
    color: #3498db;
  }

  .experience-item:hover h4 {
    color: #2d3436;
  }

  .experience-item {
    backdrop-filter: blur(24px);
  }
  .experience-item {
    position: relative;
    margin-bottom: 3rem;
    padding: 1.5rem;
    background: rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(10px);
    border-radius: 24px;
    box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
    transition:
      transform 0.3s ease,
      box-shadow 0.3s ease;
    overflow: hidden;
  }
  .rotating-circle {
    position: absolute;
    width: 100px;
    height: 100px;
    background: linear-gradient(45deg, #e74c3c, #9b59b6);
    clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
    top: 20px;
    right: 120px;
    z-index: -1;
    animation: moveAroundCard 10s linear infinite;
  }

  @keyframes moveAroundCard {
    0% {
      transform: translate(0, 0) rotate(0deg);
    }
    25% {
      transform: translate(calc(100% - 140px), 0) rotate(90deg);
      clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
      background: linear-gradient(45deg, #e6d5f5, #c4e3ff);
    }
    50% {
      transform: translate(calc(100% - 240px), calc(100% - 20px)) rotate(180deg);
      clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
      background: linear-gradient(45deg, #c4e3ff, #d4f7e1);
    }
    75% {
      transform: translate(0, calc(100% - 180px)) rotate(270deg);
      clip-path: circle(50% at 50% 50%);
      background: linear-gradient(45deg, #e8f9f1, #f5f5f5);
    }
    100% {
      transform: translate(0, 0) rotate(360deg);
      clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
      background: linear-gradient(45deg, #ffd5d5, #e6d5f5);
    }
  }

  .content {
    position: relative;
    z-index: 1;
  }
</style>
