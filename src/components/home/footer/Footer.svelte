<script>
  import {
    Facebook,
    Github,
    Instagram,
    Linkedin,
    Twitter,
  } from "lucide-svelte";
</script>

<footer class="bg-gradient-to-br text-rose-600 py-12 px-4 mt-16 shadow-xl">
  <div class="max-w-7xl mx-auto flex flex-col items-center space-y-8">
    <div class="flex flex-wrap justify-center gap-8">
      <a
        href="/"
        class="text-rose-400 hover:text-pink-600 transition-all duration-300 text-lg relative after:content-[''] after:absolute after:w-0 after:h-0.5 after:bg-pink-600 after:left-0 after:-bottom-1 hover:after:w-full after:transition-all after:duration-300"
        >Home</a
      >
      <a
        href="/#about"
        class="text-rose-400 hover:text-pink-600 transition-all duration-300 text-lg relative after:content-[''] after:absolute after:w-0 after:h-0.5 after:bg-pink-600 after:left-0 after:-bottom-1 hover:after:w-full after:transition-all after:duration-300"
        >About</a
      >
      <a
        href="https://linkedin.com/in/ankit-panchal534"
        class="text-rose-400 hover:text-pink-600 transition-all duration-300 text-lg relative after:content-[''] after:absolute after:w-0 after:h-0.5 after:bg-pink-600 after:left-0 after:-bottom-1 hover:after:w-full after:transition-all after:duration-300"
        >Contact</a
      >
    </div>
    <div class="flex flex-wrap justify-center gap-8">
      <script>
        import { Facebook, Twitter, Instagram, Linkedin } from "lucide-svelte";
      </script>
      <a
        target="_blank"
        href="https://github.com/ankitpanchal534"
        aria-label="Github"
        class="text-rose-400 hover:text-pink-600 transform hover:scale-110 hover:rotate-6 transition-all duration-300"
      >
        <Github class="w-8 h-8" />
      </a>
      <a
        target="_blank"
        href="https://instagram.com/__ankit.panchal"
        aria-label="Instagram"
        class="text-rose-400 hover:text-pink-600 transform hover:scale-110 hover:rotate-6 transition-all duration-300"
      >
        <Instagram class="w-8 h-8" />
      </a>
      <a
        target="_blank"
        href="https://linkedin.com/in/ankit-panchal534"
        aria-label="LinkedIn"
        class="text-rose-400 hover:text-pink-600 transform hover:scale-110 hover:-rotate-6 transition-all duration-300"
      >
        <Linkedin class="w-8 h-8" />
      </a>
    </div>
    <div
      class="w-24 h-0.5 bg-gradient-to-r from-transparent via-pink-200 to-transparent my-4"
    ></div>
    <p class="text-rose-600/80 text-sm font-light tracking-wider">
      ankitpanchal.in © 2024 All Rights Reserved
    </p>
  </div>
</footer>
