<script>
  import {
    Atom,
    Code2,
    CodeXml,
    Component,
    FileCode,
    FileCode2,
    FileJson2,
    FileType,
    GitBranch,
    Package,
  } from "lucide-svelte";

  const skillsData = {
    languages: {
      title: "Languages",
      items: [
        { icon: FileJson2, color: "text-yellow-500", name: "JavaScript" },
        { icon: FileType, color: "text-blue-500", name: "TypeScript" },
        { icon: FileCode, color: "text-orange-500", name: "HTML" },
        { icon: FileCode, color: "text-blue-400", name: "CSS" },
      ],
    },
    frameworks: {
      title: "Frameworks",
      items: [
        { icon: Atom, color: "text-blue-500", name: "React" },
        { icon: CodeXml, color: "text-blue-500", name: "Next.js" },
        { icon: Component, color: "text-orange-500", name: "Svelte" },
        { icon: Component, color: "text-purple-500", name: "Redux" },
        { icon: Component, color: "text-green-500", name: "React Query" },
      ],
    },
    buildTools: {
      title: "Build Tools",
      items: [
        { icon: Package, color: "text-blue-500", name: "Webpack" },
        { icon: Package, color: "text-purple-500", name: "Vite" },
        { icon: Package, color: "text-yellow-500", name: "Babel" },
        { icon: Package, color: "text-red-500", name: "npm" },
        { icon: Package, color: "text-blue-400", name: "yarn" },
      ],
    },
    otherTools: {
      title: "Other Tools",
      items: [
        { icon: GitBranch, color: "text-orange-500", name: "Git" },
        { icon: Code2, color: "text-blue-500", name: "VS Code" },
        { icon: Package, color: "text-green-500", name: "ESLint" },
        { icon: Package, color: "text-pink-500", name: "Prettier" },
        { icon: Package, color: "text-yellow-500", name: "Jest" },
        { icon: Package, color: "text-red-500", name: "Testing Library" },
      ],
    },
  };
</script>

<section class="py-14 mt-12" id="skills">
  <h2 class="text-xl font-bold md:text-4xl text-pink-700 my-12">Skills</h2>
  <div class="flex flex-col gap-4">
    {#each Object.values(skillsData) as category}
      <div class="relative group">
        <div
          class="bg-white rounded-xl p-6 border border-gray-100 hover:border-indigo-200 transition-all duration-300 h-full"
        >
          <div class="text-indigo-600 mb-4">
            <h3 class="text-sm font-bold inline-flex items-center">
              {category.title}
            </h3>
          </div>
          <div class="space-y-3 flex">
            {#each category.items as item}
              <div
                class="flex items-center gap-3 p-2 rounded-lg hover:bg-gray-50"
              >
                <svelte:component this={item.icon} class={item.color} />
                <span class="text-gray-700">{item.name}</span>
              </div>
            {/each}
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>
