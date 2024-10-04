<template>
  <main
    class="mt-10 md:mt-1 flex flex-col-reverse gap-8 items-center md:flex-row md:gap-16 md:justify-center min-h-[65vh] md:min-h-[80vh]">
    <!-- Text section with introduction -->
    <div class="space-y-2 text-center md:text-left px-10">
      <p class="text-fuchsia-200 font-semibold">Hello World, I'm</p>
      <h1 class="text-4xl font-bold md:text-5xl text-white fadein-up">
        Amelia Raihana
      </h1>
      <div class="py-2">
        <h1
          class="typewrite text-xl font-semibold text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-pink-500 md:text-2xl fadein-up"
          ref="typewriter">
          <span class="wrap">{{ txt }}</span>
        </h1>
      </div>
      <p class="text-white pr-4 fade-in-from-left font-light">
        Welcome to my personal website <span class="wave">👋🏼</span>
      </p>
      <br />
    </div>
    <!-- Image section for personal avatar -->
    <div class="flex justify-center md:justify-start fadein-right">
      <img alt="amemoji" fetchpriority="high" width="300" height="300" decoding="async" data-nimg="1"
        class="w-10/12 md:h-auto rounded-full border-4 border-purple-200 pict" src="/ameliamemoji.png" />
    </div>
  </main>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      // Text options for typewriter effect
      toRotate: [
        "Computer Science Graduate",
        "Major in Software Engineering",
        "Currently Looking For..",
        "A Software Engineer Role",
        "Or Related Opportunities",
      ],
      period: 2000, // Time period for typewriter effect
      txt: "", // Current text being displayed
      loopNum: 0, // Index for looping through text options
      isDeleting: false, // Flag for deleting text
    };
  },
  mounted() {
    // Start typewriter effect after component is mounted
    this.$nextTick(() => {
      this.tick();
    });
  },
  methods: {
    tick() {
      let typewriter = this.$refs.typewriter; // Reference to typewriter element

      // Return if typewriter reference is not found
      if (!typewriter) {
        return;
      }

      let i = this.loopNum % this.toRotate.length; // Current index for text rotation
      let fullTxt = this.toRotate[i]; // Full text to be displayed

      // Update the text based on whether we are deleting or adding characters
      this.txt = this.isDeleting
        ? fullTxt.substring(0, this.txt.length - 1)
        : fullTxt.substring(0, this.txt.length + 1);
      typewriter.innerHTML = `<span class="wrap">${this.txt}</span>`; // Update typewriter display

      let that = this; // Store reference to `this`
      let delta = 200 - Math.random() * 100; // Random delay for effect

      // Adjust delay based on deletion state
      if (this.isDeleting) {
        delta /= 2;
      }

      // Manage typewriter behavior based on text state
      if (!this.isDeleting && this.txt === fullTxt) {
        delta = this.period; // Set delay when text is complete
        this.isDeleting = true; // Start deleting
      } else if (this.isDeleting && this.txt === "") {
        this.isDeleting = false; // Reset deleting flag
        this.loopNum++; // Move to next text option
        delta = 500; // Delay after finishing a full text
      }

      // Recursive call to keep updating text
      setTimeout(() => {
        that.tick();
      }, delta);
    },
  },
};
</script>

<style>
/* General body styles */
body {
  overflow-y: scroll;
  /* Enable vertical scrolling */
  overflow-x: hidden;
  /* Disable horizontal scrolling */
}

/* Styles for typewriter effect */
.typewrite>.wrap {
  border-right: 0.08em solid #fff;
  /* Cursor effect */
}

/* Wave animation for emoji */
.wave {
  animation-name: wave-animation;
  animation-duration: 2.5s;
  animation-iteration-count: infinite;
  transform-origin: 70% 70%;
  display: inline-block;
}

/* Keyframes for wave animation */
@keyframes wave-animation {
  0% {
    transform: rotate(0deg);
  }

  10% {
    transform: rotate(14deg);
  }

  20% {
    transform: rotate(-8deg);
  }

  30% {
    transform: rotate(14deg);
  }

  40% {
    transform: rotate(-4deg);
  }

  50% {
    transform: rotate(10deg);
  }

  60% {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(0deg);
  }
}

/* Styles for image with shadow */
.pict {
  box-shadow: 0px 0px 73px -9px #fb6f92;
  /* Shadow effect */
  -webkit-box-shadow: 0px 0px 73px -9px #fb6f92;
  /* Webkit shadow */
  -moz-box-shadow: 0px 0px 73px -9px #fb6f92;
  /* Firefox shadow */
}

/* Fade-in animations */
.fadein-up {
  opacity: 0;
  /* Start invisible */
  animation-name: fadeInUp;
  /* Animation name */
  animation-duration: 0.5s;
  /* Animation duration */
  animation-fill-mode: forwards;
  /* Keep final state */
  animation-delay: 500ms;
  /* Delay before starting */
}

/* Keyframes for fade-in up animation */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate3d(0, 100%, 0);
    /* Move up */
  }

  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
    /* End position */
  }
}

/* Fade-in from left animation */
.fade-in-from-left {
  opacity: 0;
  /* Start invisible */
  animation: fadeInLeft 0.5s ease-out forwards;
  /* Animation */
  animation-delay: 500ms;
  /* Delay before starting */
}

/* Keyframes for fade-in left animation */
@keyframes fadeInLeft {
  0% {
    opacity: 0;
    /* Start invisible */
    transform: translateX(-100%);
    /* Move left */
  }

  100% {
    opacity: 1;
    /* End visible */
    transform: translateX(0);
    /* Final position */
  }
}

/* Fade-in from right animation */
.fadein-right {
  opacity: 0;
  /* Start invisible */
  animation: fadeInRight 0.5s ease-out forwards;
  /* Animation */
  animation-delay: 500ms;
  /* Delay before starting */
}

/* Keyframes for fade-in right animation */
@keyframes fadeInRight {
  0% {
    opacity: 0;
    /* Start invisible */
    transform: translateX(100%);
    /* Move right */
  }

  100% {
    opacity: 1;
    /* End visible */
    transform: translateX(0);
    /* Final position */
  }
}

/* Fade-in from bottom animation */
.fadein-bot {
  opacity: 0;
  /* Start invisible */
  animation: fadeInBot 0.5s forwards;
  /* Animation */
}

/* Keyframes for fade-in bottom animation */
@keyframes fadeInBot {
  from {
    opacity: 0;
    /* Start invisible */
    transform: translate3d(0, -100%, 0);
    /* Move down */
  }

  to {
    opacity: 1;
    /* End visible */
    transform: translate3d(0, 0, 0);
    /* Final position */
  }
}

/* Animation delays for various fade-in effects */
.fadein-1 {
  animation-delay: 200ms;
  /* Delay for first animation */
}

.fadein-2 {
  animation-delay: 400ms;
  /* Delay for second animation */
}

.fadein-3 {
  animation-delay: 600ms;
  /* Delay for third animation */
}

.fade-500 {
  animation-delay: 500ms;
  /* Delay for fade animation */
}</style>
