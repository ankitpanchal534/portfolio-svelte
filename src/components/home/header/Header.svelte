<script>
  import { page } from "$app/stores";

  const links = [
    {
      name: "Home",
      href: "/",
    },
    {
      name: "About",
      href: "/#about",
    },
    {
      name: "Projects",
      href: "/#projects",
    },
    {
      name: "Skills",
      href: "/#skills",
    },
    {
      name: "Experience",
      href: "/#experience",
    },
  ];
</script>

<section class="flex justify-center">
  <div
    class="header flex justify-evenly items-center max-w-xl rounded-full p-2 w-full list-none"
  >
    {#each links as link, index}
      {@const isHashMatch = $page.url.hash === link.href.replace("/", "")}

      {@const isActive = isHashMatch}

      <li>
        <a
          href={link.href}
          class="transition-colors duration-300 px-6 py-2 rounded-full {isActive
            ? 'bg-pink-100 text-pink-800'
            : 'hover:bg-pink-100 opacity-65'} {index > 2 && 'hidden'} md:block"
        >
          {link.name}
        </a>
      </li>
    {/each}
  </div>
</section>

<style>
  .header {
    box-shadow: 0px 0px 42px rgb(248, 188, 231);
    background-color: white;
  }
</style>
