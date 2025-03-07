<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Manrope:wght@200..800&display=swap');

  :global {
    body {
      font-family: "Manrope", sans-serif;
      font-style: normal;
    }

    *, *::before, *::after {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: inherit;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    main {
      max-width: 576px;
      margin: 2em auto;
      padding: 0 1em;
    }
  
    main * {
      margin: 25px 0;
    }
  }

  nav, footer {
    padding: 15px 1em;
  }

  .navContainer,footer {
    display: flex;
    justify-content: space-between;
    max-width: 768px;
    margin: auto;
  }

  nav a {
    margin: 0 5px;
  }

  nav img {
    max-height: 25px;
    width: auto;
  }
</style>

<script lang="ts">
  let { children } = $props();
</script>

<nav>
  <section class="navContainer">
    <div>
      <a href="/">
        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Visual_Studio_Code_1.35_icon.svg/512px-Visual_Studio_Code_1.35_icon.svg.png" alt="Website Logo">
      </a>
    </div>
    <div>
      <a href="/blog">Blog</a>
      <a href="/about">About</a>
    </div>
  </section>
</nav>

{@render children()}

<footer>
  Copyright {new Date().getFullYear()}
</footer>