<template>
  <!-- <nav class="scrim-bg fixed z-40 top-0 inset-x-0 pt-3 px-3" aria-label="Main Menu">
    <ul class="flex">
      <li class="flex-1">
        <nuxt-link class="btn block" to="/">Home</nuxt-link>
      </li>
      <li class="flex-1 ml-2">
        <nuxt-link class="btn block" to="/blog">Study</nuxt-link>
      </li>
      <li class="flex-1 ml-2">
        <nuxt-link class="btn block" to="/projects">Projects</nuxt-link>
      </li>
    </ul>
  </nav> -->
  <nav class="main-nav" aria-label="Main Menu">
    <div class="nav">
      <a href="/" class="logo-holder">
        <nuxt-img src="logo-circle.svg" width="50" alt="gift-logo" />
        <span class="logo-name"><b>UPC GIFT - PASAY</b></span>
      </a>
      <div>
        <nuxt-link class="" to="/">Home</nuxt-link>
        <nuxt-link class="ml-2" to="/blog">Study</nuxt-link>
        <nuxt-link class="ml-2" to="/projects">Projects</nuxt-link>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="postcss" scoped>
.scrim-bg {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  &::before {
    content: '';
    z-index: -1;
    background-color: var(--bg);
    @apply absolute bottom-0 inset-x-0 h-12 mb-4 transition-colors duration-200 ease-in-out;
  }
  &::after {
    content: '';
    z-index: -1;
    opacity: 1;
    animation: fadeIn1 500ms ease-in-out;
    @apply pointer-events-none absolute bottom-0 inset-x-0 h-16 -mb-12;
    background: linear-gradient(to bottom, #111827, cubic-bezier(0.15, 0, 0.45, 1), transparent);
  }
}

.main-nav {
  background-color: var(--bg);
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 9999;
  display: flex;
  justify-content: center;
}

.main-nav .nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 64rem;
  padding: 8px 0;
}

.main-nav .nav {
  @media screen and (max-width: 1025px) {
    padding: 8px 2rem;
  }
}

.main-nav .nav .logo-holder {
  display: flex;
  align-items: center;
}

.main-nav .nav .logo-name {
  margin-left: 10px;
  @media screen and (max-width: 426px) {
    display: none;
  }
}

.nuxt-link-exact-active {
  @apply text-gray-200 bg-opacity-25 cursor-default;
}

.light {
  & .scrim-bg {
    &::after {
      animation-name: fadeIn2;
      background: linear-gradient(to bottom, #e5e7eb, cubic-bezier(0.15, 0, 0.45, 1), transparent);
    }
  }
  & .nuxt-link-exact-active {
    @apply text-primary-700;
  }
}

/* Need two because of smoother switching between color modes */
@keyframes fadeIn1 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@keyframes fadeIn2 {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
