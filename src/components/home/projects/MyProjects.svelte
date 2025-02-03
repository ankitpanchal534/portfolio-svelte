<script>
  import { onMount } from "svelte";
  import ProjectCard from "./ProjectCard.svelte";
  import { json } from "@sveltejs/kit";

  /**
   * @type {any[]}
   */
  let projects = $state([]);

  onMount(async () => {
    const response = await fetch(
      "https://raw.githubusercontent.com/ankitpanchal534/constants/main/projects.json"
    );

    const data = await response.json();
    projects = data;
  });
</script>

<section>
  <div class="pt-14 mt-12" id="projects">
    <h2 class="text-xl font-bold md:text-4xl text-pink-700 my-12">
      My Projects
    </h2>
    {#if projects && Array.isArray(projects)}
      <div class="projects space-y-6">
        {#each projects as project, index}
          <ProjectCard {project} {index} />
        {/each}
      </div>
    {/if}
  </div>
</section>
