<template>
  <header class="navbar" aria-label="Main Menu">
    <nuxt-link tag="h1" class="navbar__heading h4" to="/">
      Doling Neighborhood Association
      <img src="/img/tree-graphic.png" alt="" />
    </nuxt-link>
    <nav class="navbar__main-nav">
      <button class="menu-toggle" id="menuToggle" aria-expanded="false" v-on:click="toggleMenu" tab-index="1">
        <span class="sr-only">Menu</span>
        <svg width="100" height="100" viewBox="0 0 100 100">
          <path
            class="line line1"
            d="M 20,29.000046 H 80.000231 C 80.000231,29.000046 94.498839,28.817352 94.532987,66.711331 94.543142,77.980673 90.966081,81.670246 85.259173,81.668997 79.552261,81.667751 75.000211,74.999942 75.000211,74.999942 L 25.000021,25.000058"
          />
          <path class="line line2" d="M 20,50 H 80" />
          <path
            class="line line3"
            d="M 20,70.999954 H 80.000231 C 80.000231,70.999954 94.498839,71.182648 94.532987,33.288669 94.543142,22.019327 90.966081,18.329754 85.259173,18.331003 79.552261,18.332249 75.000211,25.000058 75.000211,25.000058 L 25.000021,74.999942"
          />
        </svg>
      </button>
      <ul class="navbar__links" id="navLinks">
        <li class="navbar__link">
          <nuxt-link class="" to="/">Home</nuxt-link>
        </li>
        <li class="navbar__link">
          <nuxt-link class="" to="/about">About</nuxt-link>
        </li>
        <li class="navbar__link">
          <nuxt-link class="" to="/blog">History</nuxt-link>
        </li>
      </ul>
    </nav>
    <div class="navbar__social">
      <a href="https://nextdoor.com/neighborhood/doling--springfield--mo/" rel="noreferrer noopener">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 195 195">
          <title>Doling Neighborhood on Nextdoor</title>
          <g data-name="Layer 2">
            <path
              d="M4 92a94 94 0 0 1 160-61A94 94 0 1 1 4 92Zm131-33a28 28 0 0 0-3-2c-21-13-53-7-67 15-2 3-6 3-8 0-4-4-3-10-4-15 0-2 0-3-3-3l-24 2c0 20 7 36 28 40 3 1 4 3 4 5v43c0 4 0 5 4 5h18c4 0 5-1 5-5V99a24 24 0 0 1 5-16c14-17 40-4 38 16v45c1 4 1 5 5 5h19c2 0 3-1 3-4V92c0-14-9-26-20-33Z"
              style="stroke-miterlimit: 10; stroke-width: 8px"
              data-name="Layer 1"
            />
          </g>
        </svg>
      </a>
      <a href="https://www.facebook.com/groups/1045034285583613/" rel="noreferrer noopener">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 195 195">
          <title>Doling Neighborhood Association on Facebook</title>
          <g data-name="Layer 2">
            <path
              d="M192 98c0-52-43-94-94-94a95 95 0 0 0-15 187v-66H59V98h24V77c0-23 14-37 35-37a144 144 0 0 1 21 2v24h-11c-12 0-16 7-16 14v18h26l-4 27h-22v67a94 94 0 0 0 80-94Z"
              style="stroke-miterlimit: 10; stroke-width: 8px"
              data-name="Layer 1"
            />
          </g>
        </svg>
      </a>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  methods: {
    toggleMenu: function (e) {
      const menu = document.getElementById('navLinks')
      const toggle = document.getElementById('menuToggle')
      if (menu.classList.contains('is-active')) {
        menu.classList.remove('is-active')
        toggle.classList.remove('is-active')
      } else {
        menu.classList.add('is-active')
        toggle.classList.add('is-active')
        e.target.setAttribute('aria-expanded', 'true')
      }
    },
  },
}
</script>
<style lang="scss" scoped>
  
</style>