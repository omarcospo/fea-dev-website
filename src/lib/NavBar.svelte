<script lang="ts">
  import devLogo from "/images/logo.svg";
  let isOpen = false;

  const toggleMenu = () => {
    isOpen = !isOpen;
  };

  import { base } from "$app/paths";
</script>

<main>
  <nav>
    <div class={`logo ${isOpen ? "open" : ""}`}>
      <a href="/">
        <img src={devLogo} alt="FEA.dev logo" width="125" />
      </a>
    </div>
    <div class={`menu ${isOpen ? "open" : ""}`}>
      <a href="{base}/projetos">Projetos</a>
      <a href="{base}/about">Sobre</a>
      <a href="{base}/contato">Contato</a>
    </div>
    <div class={`hamburger ${isOpen ? "open" : ""}`} on:click={toggleMenu}>
      <div></div>
      <div></div>
      <div></div>
    </div>
  </nav>
</main>

<style>
  main {
    margin-bottom: 4em;
  }

  nav {
    background-color: #1a1a1a;
    color: white;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1em;
    z-index: 1000;
  }

  .menu {
    display: flex;
    padding: 0.25em 2em 0 0;
    gap: 2em;
  }

  .menu a {
    border-bottom: 1px solid transparent;
  }

  .menu a:hover {
    color: #ffef02;
    border-bottom: 1px solid #ffef02;
  }

  .hamburger {
    display: none;
    cursor: pointer;
    flex-direction: column;
    gap: 0.3rem;
    padding-right: 2em;
  }

  .hamburger div {
    width: 25px;
    height: 2px;
    background-color: white;
  }

  /* --- mobile */
  @media (max-width: 768px) {
    .menu {
      display: none;
      flex-direction: column;
      gap: 0.5rem;
    }

    .menu.open {
      display: flex;
    }

    .hamburger {
      display: flex;
    }

    .hamburger.open {
      padding-bottom: 6em;
    }

    .logo.open {
      padding-bottom: 6em;
    }
  }
</style>
