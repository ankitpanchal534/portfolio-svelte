<script>
  const { project, index } = $props();
  import * as DynamicIcon from "lucide-svelte/icons";
  // const isEven = index % 2 === 0;
  const isEven = false;
</script>

<section class={"project-card-wrapper "} dir={!isEven ? "ltr" : "rtl"}>
  <div class="project-card grid md:grid-cols-2 relative">
    <div class={"project-details space-y-3 "}>
      <h3 class="project-title font-extralight">{project.title}</h3>
      <p class="project-description">{project.description}</p>
      <div class="w-full flex justify-start">
        <a
          href={project.link}
          target="_blank"
          class=" flex items-center underline text-sm font-semibold justify-center rounded-full gap-2"
        >
          See here
          <DynamicIcon.ExternalLinkIcon size={18} />
        </a>
      </div>
      <div class="project-technologies">
        {#each project.tech_skills as skill}
          <span class="project-language">{skill}</span>
        {/each}
        <!-- <p class="project-created">{project.date}</p> -->
      </div>
    </div>
    <div class={`project-thumbbnail md:block hidden `}>
      <!-- {index % 2} -->
      <!-- <iframe
          src={project.homepage}
          title="Project Preview"
          width="600"
          height="450"
        ></iframe> -->
      <img
        src={"https://ankitpanchal.in/projects/" + project.thumbnail}
        alt="Project Preview"
        class={!isEven ? "img1" : "img2"}
      />
    </div>
  </div>
</section>

<style>
  .project-card {
    /* display: flex;
    flex-direction: column;
    align-items: center; */
    padding: 1rem;
    /* border: 0.5px solid #ccc; */
    border-radius: 24px;
    box-shadow: 0 2px 24px rgba(0, 0, 0, 0.1);
    /* margin: 1rem; */
    max-width: 800px;
    background-color: #f9f9f9;
    overflow: hidden;
    height: 250px;
    border: 0.5px solid pink;
  }
  .project-card:hover {
    background-color: rgb(236, 233, 233);
  }
  .project-details {
    display: flex;
    flex-direction: column;
    /* align-items: center; */
    margin-bottom: 1rem;
  }

  .project-title {
    font-size: 1.5rem;
    /* font-weight: bold; */
    /* margin-bottom: 0.5rem; */
  }

  .project-description {
    font-size: 0.9rem;
    /* margin-bottom: 1rem; */
  }

  .project-link {
    /* display: flex;
    align-items: center;
    text-decoration: none;
    color: #007bff;
    font-weight: bold;
    transition: color 0.3s; */
    box-shadow: 0px 0px 16px whitesmoke;
    transition: ease-in-out 0.2s;
    border: 0.5px solid pink;
  }

  .project-link:hover {
    box-shadow: 0px 0px 24px rgb(240, 231, 233);
  }

  .project-technologies {
    display: flex;
    flex-wrap: wrap;
    font-size: 0.7rem;
    /* justify-content: center; */
    margin-top: 1rem;
    gap: 6px;
  }
  .project-language {
    /* margin-right: 1rem; */
    background-color: #656565;
    color: white;
    padding: 1px 8px;
    border-radius: 12px;
    /* font-size: 0.7rem; */
    /* font-weight: bold; */
  }

  .project-thumbbnail {
    /* display: flex; */
    /* justify-content: center; */
    /* align-items: center; */
    /* margin-right: -50%; */
    position: relative;
    /* max-height: 200px; */
    /* margin-top: 1rem; */
  }
  .project-thumbbnail img {
    position: absolute;
    height: 200px;
    width: 330px;
    border-radius: 8px;
    object-fit: fill;
    top: 0;
    transform: scale(1.2);
    transform-origin: top;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  .project-thumbbnail img.img1 {
    right: -25%;
    box-shadow: -4px -2px 12px rgba(0, 0, 0, 0.1);
  }
  .project-thumbbnail img.img2 {
    left: -25%;
  }
  .project-card .project-thumbbnail img.img1 {
    transform: rotate(-4deg) scale(1.2);
    transition: ease-in-out 0.2s;
  }
  .project-card:hover .project-thumbbnail img.img1 {
    transform: rotate(-2deg) scale(1.5);
  }
  .project-card .project-thumbbnail img.img2 {
    transform: rotate(4deg) scale(1.2);
    transition: ease-in-out 0.2s;
  }
  .project-card:hover .project-thumbbnail img.img2 {
    transform: rotate(2deg) scale(1.5);
  }
</style>
