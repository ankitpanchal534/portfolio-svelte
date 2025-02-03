<script>
  import * as DynamicIcon from "lucide-svelte/icons";
</script>

<section class="hero flex flex-col w-full items-center">
  <div class="content flex justify-center items-center w-full pt-52 pb-14">
    <div
      class="bg-red-400 text-xs text-white w-fit m-auto p-1 mt-2 rounded-full px-4"
    >
      Built with Svelte 🚀
    </div>
    <h1>
      <span class="text-2xl">Hello,</span>
      <span class="hand_emoji"> 👋 </span>

      I'm
      <span
        class="bg-gradient-to-r from-emerald-500 via-teal-500 to-blue-500 text-transparent bg-clip-text"
        >Ankit Kumar
      </span>
      ✨
    </h1>
    <p>
      Frontend Developer | Building the Future with React, JavaScript, and
      Tailwind CSS
    </p>

    <div class="cta mt-4">
      <a
        target="_blank"
        href="https://drive.google.com/file/d/1BkOXhviNE2E2MNPvSFleaUorF_ZuwSXP/view"
        class="cta-button flex gap-2"
      >
        View CV <DynamicIcon.TextQuote />
      </a>
      <a
        target="_blank"
        href="https://linkedin.com/in/ankit-panchal534"
        class="cta-button shadow-fuchsia-50 shadow-2xl"
      >
        <DynamicIcon.Linkedin /></a
      >
      <a
        target="_blank"
        href="https://github.com/ankitpanchal534"
        class="cta-button shadow-fuchsia-50 shadow-2xl"
      >
        <DynamicIcon.Github /></a
      >
    </div>
  </div>
</section>

<style>
  /* Animation for background gradient */
  @keyframes gradientShift {
    0% {
      background-position: 100% 0;
    }
    50% {
      background-position: 0 100%;
    }
    100% {
      background-position: 100% 0;
    }
  }

  @keyframes wave {
    0%,
    100% {
      transform: rotate(0deg);
    }
    25% {
      transform: rotate(-20deg);
    }
    75% {
      transform: rotate(20deg);
    }
  }

  /* .hand_emoji {
    animation: wave 2s infinite;
  } */
  .hand_emoji:hover {
    cursor: pointer;
    transform: rotate(10deg);
  }
  /* Content Styling */
  .content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .content h1 {
    font-size: 3rem;
    font-weight: bold;
    margin-bottom: 20px;
  }

  .content p {
    font-size: 1.25rem;
    margin-bottom: 30px;
    opacity: 0.85;
  }

  /* Call to Action Buttons */
  .cta {
    display: flex;
    justify-content: center;
    gap: 20px;
  }

  .cta-button {
    padding: 10px 20px;
    /* border: 2px solid transparent; */
    border-radius: 30px;
    font-size: 1.1rem;
    font-weight: bold;
    text-decoration: none;
    background-color: transparent;
    transition: all 0.3s ease;
    box-shadow: 0px 0px 24px lightgray;
  }

  .cta-button:hover {
    background-color: white;
    color: #ff586e;
    transform: scale(1.2);
  }
  /* .cta-button-link {
    padding: 10px 20px;
    border: 2px solid transparent;
    border-radius: 30px;
    font-size: 1.1rem;
    font-weight: bold;
    text-decoration: none;
    background-color: transparent;
    transition: all 0.3s ease;
    box-shadow: 0px 0px 24px lightgray;
  } */
</style>
