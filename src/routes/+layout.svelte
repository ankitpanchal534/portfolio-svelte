<script lang="ts">
  import "../app.css";
  import Footer from "../components/home/footer/Footer.svelte";
  import Header from "../components/home/header/Header.svelte";
</script>

<section>
  <nav class="sticky top-6 z-50">
    <Header />
  </nav>
  <main class="-mt-14">
    <slot />
  </main>
  <footer>
    <Footer />
  </footer>
</section>
