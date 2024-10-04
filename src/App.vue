<template>
  <div class="max-w-7xl mx-auto flex flex-col relative">
    <!-- Navigation Bar -->
    <nav class="max-w-7xl px-5 md:fixed top-0 z-[98] w-screen backdrop-blur-md bg-[#121212] bg-opacity-80">
      <div class="container mx-auto flex flex-wrap items-center justify-between">
        <!-- Logo / Home Button -->
        <button @click="redirectToHome" class="flex">
          <span
            class="self-center text-lg text-[#ffb3c6] font-semibold whitespace-nowrap fadein-bot hover:text-pink-100">amelia();</span>
        </button>

        <!-- LinkedIn Profile Link -->
        <div class="flex md:order-2 fadein-bot">
          <a href="https://www.linkedin.com/in/ameliaraihana/">
            <img class="w-9 rounded-full" src="https://cdn.worldvectorlogo.com/logos/linkedin-icon-2.svg"
              alt="linkedin" />
          </a>
        </div>

        <!-- Navigation Links -->
        <div class="hidden md:flex justify-between items-center w-full md:w-auto md:order-1" id="mobile-menu-3">
          <ul class="flex-col md:flex-row flex md:space-x-8 mt-4 md:mt-0 md:text-sm md:font-medium">
            <li>
              <router-link to="/"
                class="fadein-bot text-gray-700 hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0"
                aria-current="page">
                Home
              </router-link>
            </li>
            <li>
              <router-link to="/about"
                class="fadein-bot fadein-1 text-gray-700 hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0">
                About
              </router-link>
            </li>
            <li>
              <router-link to="/portfolio"
                class="fadein-bot fadein-2 text-gray-700 hover:bg-gray-50 border-b border-gray-100 md:hover:bg-transparent md:border-0 block pl-3 pr-4 py-2 md:hover:text-gray-500 md:p-0">
                Portfolio
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- Main Content Area -->
    <div class="md:mt-[100px]">
      <router-view />
    </div>

    <!-- Footer for Mobile Devices -->
    <footer
      class="block md:hidden fixed bottom-0 left-0 right-0 rounded-t-3xl border border-[#383838] bg-[#121212] bg-opacity-80 backdrop-blur-md backdrop-opacity-90">
      <nav class="flex justify-around py-4 text-xs">
        <router-link to="/" class="text-gray-300 hover:text-pink-500">Home</router-link>
        <router-link to="/about" class="text-gray-300 hover:text-pink-500">About</router-link>
        <router-link to="/portfolio" class="text-gray-300 hover:text-pink-500">Portfolio</router-link>
      </nav>
    </footer>
  </div>
</template>

<script>
export default {
  methods: {
    redirectToHome() {
      this.$router.push('/');
    }
  },
}
</script>

<style>
/* Global Styles */
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Scrollbar Styles */
::-webkit-scrollbar {
  width: 5px;
  /* Vertical scrollbar */
  height: 5px;
  /* Horizontal scrollbar */
}

::-webkit-scrollbar-track {
  background: hsl(240, 1%, 17%);
  border-radius: 5px;
}

::-webkit-scrollbar-thumb {
  background: #ffc2d1;
  border-radius: 5px;
}

::-webkit-scrollbar-button {
  width: 20px;
}

/* Body Styles */
body {
  font-family: -apple-system, BlinkMacSystemFont, "Helvetica Neue", "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica", sans-serif;
  background: hsl(0, 0%, 7%);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
}

/* Navigation Styles */
nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  transition: color 0.3s;
}

nav a.router-link-exact-active {
  display: inline-flex;
  flex-direction: column;
  color: white;
  transition: color 0.3s;
}

nav a.router-link-exact-active::after {
  display: inline-block;
  content: "";
  margin-top: 0.08em;
  width: 100%;
  height: 4px;
  border-radius: 2px;
  background-color: #fb6f92;
}

nav a.router-link-exact-active:hover {
  color: white;
}

/* Animation Styles */
@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}</style>
