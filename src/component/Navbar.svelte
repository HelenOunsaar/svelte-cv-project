<script>
  import { Link } from "svelte-navigator";
  import Name from "../lib/Name.svelte";
  import { onMount } from "svelte";

  let links = [
    { text: "About", url: "/" },
    { text: "Skills", url: "/skills" },
    { text: "Experience", url: "/experience" },
    { text: "Education", url: "/education" },
  ];

  let click = false;

  const handleClick = () => {
    click = !click;
  };

  const handleKeyPress = (event) => {
    if (event.key === "Enter" || event.key === " ") {
      handleClick();
    }
  };

  const closeMobileMenu = () => {
    click = false;
  };

  onMount(() => {
    // Close the mobile menu when the window is resized
    window.addEventListener("resize", closeMobileMenu);

    return () => {
      window.removeEventListener("resize", closeMobileMenu);
    };
  });
</script>

<nav>
  <div class="nav-content">
    <Name />
    <div class="menu-icon" on:click={handleClick} on:keydown={handleKeyPress}>
      {#if click}
        <i class="fa-solid fa-x" />
      {:else}
        <i class="fa-solid fa-bars" />
      {/if}
    </div>
    <ul class={click ? "nav-links active" : "nav-links"}>
      {#each links as link}
        <li>
          <Link to={link.url} class="mytag" on:click={closeMobileMenu}
            >{link.text}</Link
          >
        </li>
      {/each}
    </ul>
  </div>
</nav>

<style>
  @import "@fortawesome/fontawesome-free/css/all.css";

  nav {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .nav-links {
    list-style: none;
    display: flex;
    margin: 0;
    padding: 0;
  }

  nav li:hover {
    transform: scale(1.1);
  }

  .nav-content {
    height: 23px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding: 20px 10px;
    border-bottom: 2px solid #BFA181;
    width: 100%;
    max-width: 850px;
  }

  .menu-icon {
    cursor: pointer;
    font-size: 1.5rem;
    margin-left: auto;
    display: none;
  }

  @media screen and (max-width: 768px) {
    
    .nav-links {
      background-color: #0A1828;
      display: flex;
      flex-direction: column;
      position: absolute;
      top: -100vh;
      left: 0;
      align-items: center;
    }

    .nav-links.active {
      display: flex;
      justify-content: center;
      width: 100%;
      height: 70%;
      top: 12vh;
      transition: all 0.6s ease;
      z-index: 2;
      gap: 15px;
      font-size: 18px;
    }

    .menu-icon {
      display: block;
    }
  }
</style>
