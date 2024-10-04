<script>
export default {
  data() {
    return {
      activeTab: 1, // Tracks the currently active tab (1 for Key Skills, 2 for Others)
      tech: [
        {
          id: 1,
          name: "HTML",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/1051/1051277.png",
          status: null,
        },
        {
          id: 2,
          name: "CSS",
          imageUrl: "https://cdn-icons-png.flaticon.com/512/732/732190.png",
          status: null,
        },
        {
          id: 3,
          name: "Javascript",
          imageUrl:
            "https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png",
          status: null,
        },
        {
          id: 4,
          name: "VueJS",
          imageUrl:
            "https://cdn.iconscout.com/icon/free/png-256/free-vue-282497.png?f=webp",
          status: null,
        },
        {
          id: 5,
          name: "Tailwind",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg",
          status: null,
        },
        {
          id: 6,
          name: "C",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/commons/1/18/C_Programming_Language.svg",
          status: null,
        },
        {
          id: 7,
          name: "C++",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/commons/1/18/ISO_C%2B%2B_Logo.svg",
          status: null,
        },
        {
          id: 8,
          name: "Python",
          imageUrl:
            "https://cdn.freebiesupply.com/logos/large/2x/python-5-logo-png-transparent.png",
          status: null,
        },
        {
          id: 9,
          name: "Swift",
          imageUrl:
            "https://cdn4.iconfinder.com/data/icons/logos-3/504/Swift-2-1024.png",
          status: null,
        },
        {
          id: 10,
          name: "Firebase",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/commons/c/cf/Firebase_icon.svg",
          status: null,
        },
        {
          id: 11,
          name: "Flutter",
          imageUrl:
            "https://web-strapi.mrmilu.com/uploads/flutter_logo_470e9f7491.png",
          status: null,
        },
        {
          id: 12,
          name: "SQLite",
          imageUrl:
            "https://dwglogo.com/wp-content/uploads/2018/03/SQLite_Vector_logo-1024x705.png",
          status: null,
        },
        {
          id: 13,
          name: "Go",
          imageUrl:
            "https://i.pinimg.com/736x/f0/1f/69/f01f692c14ed47421cbc564ae4bf0ed3.jpg",
          status: null,
        },
        {
          id: 14,
          name: "Laravel",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/commons/9/9a/Laravel.svg",
          status: null,
        },
        {
          id: 15,
          name: "Bootstrap",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/commons/b/b2/Bootstrap_logo.svg",
          status: null,
        },
        {
          id: 16,
          name: "Postman",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/commons/c/c2/Postman_%28software%29.png",
          status: null,
        },
        {
          id: 17,
          name: "MySQL",
          imageUrl:
            "https://upload.wikimedia.org/wikipedia/en/d/dd/MySQL_logo.svg",
          status: null,
        },
      ],
      otherSkills: [
        {
          id: 1,
          name: "Communication",
          status: null,
        },
        {
          id: 2,
          name: "Adaptability",
          status: null,
        },
        {
          id: 3,
          name: "Attention to Detail",
          status: null,
        },
        {
          id: 4,
          name: "Interpersonal",
          status: null,
        },
      ],
    };
  },
};
</script>

<template>
  <div
    class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5"
  >
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center"
        >
          About Me &nbsp;
          <div
            class="h-[1px] w-32 bg-stone-400 md:w-96 aos-init aos-animate"
            data-aos="zoom-in-left"
            data-aos-duration="600"
          ></div>
        </div>
      </header>

      <section
        class="text-sm md:text-base text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center"
      >
        <!-- <div class="flex justify-center">
          <img class="w-9/12 rounded-full mb-3 fadein-up"
             src="/amelia.png" alt="ame"> 
        </div> -->
        <div class="md:w-11/12">
          <p class="mb-3 md:mb-7 fadein-left fadeins-1">
            &nbsp; &nbsp; &nbsp; Hello! 👋 I'm Amelia, and I'm passionate about
            making a meaningful impact through technology. My name, Amelia,
            itself means ambitious, reflecting my drive for continuous growth
            and excellence. As a Computer Science graduate from International
            Islamic University Malaysia, I've been fostering my love for
            programming since my foundation year. Two words that best describe
            me are ambitious and committed.
          </p>
          <p class="mb-3 md:mb-7 fadein-left fadeins-2">
            &nbsp; &nbsp; &nbsp; Having software engineering internship
            experience, and real-world expertise in web and mobile development.
            Also proven ability to design and develop user-friendly interfaces,
            integrate APIs, and build backend systems, I'm on the lookout for a
            software engineer role or related opportunities where I can
            contribute my skills and continue learning in a dynamic environment.
          </p>
          <p class="mb-3 fadein-left fadeins-3">
            &nbsp; &nbsp; &nbsp; If you're interested in connecting or have an
            exciting opportunity to discuss, please feel free to contact me.
            Let's build something impactful together!
          </p>
        </div>
      </section>
    </article>
  </div>

  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center"
        >
          <div
            class="h-[1px] w-10 bg-stone-400 md:w-20 aos-init aos-animate"
            data-aos="zoom-in-left"
            data-aos-duration="600"
          ></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul
            class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5"
          >
            <li class="mr-2">
              <button
                class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{
                  'text-fuchsia-200 bg-slate-200 bg-opacity-10':
                    activeTab === 1,
                }"
                @click="activeTab = 1"
              >
                Key Skills
              </button>
            </li>
            <li class="mr-2">
              <button
                class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{
                  'text-fuchsia-200 bg-slate-200 bg-opacity-10':
                    activeTab === 2,
                }"
                @click="activeTab = 2"
              >
                Others
              </button>
            </li>
          </ul>
        </div>
        <div v-show="activeTab === 1">
          <div
            class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12"
          >
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-neutral-200 px-2 py-2 hover:bg-neutral-200 hover:bg-opacity-10 md:gap-3 lg:px-3"
              >
                <div
                  class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in"
                >
                  <img
                    alt="HTML"
                    loading="lazy"
                    width="32"
                    height="32"
                    decoding="async"
                    data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                    :src="item.imageUrl"
                    style="color: transparent"
                  />
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div
                    class="tech font-medium text-secondary transition-all duration-300 translate-y-0"
                  >
                    {{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-sky-300 transition-all duration-300 md:text-xs lg:text-sm"
                  >
                    {{ item.status }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div
            class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12"
          >
            <div v-for="item in otherSkills" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-neutral-500 px-3 py-3 hover:bg-neutral-200 hover:bg-opacity-10 md:gap-3 lg:px-3"
              >
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div
                    class="tech font-medium text-secondary transition-all duration-300 translate-y-0"
                  >
                    {{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-neutral-200 transition-all duration-300 md:text-xs lg:text-sm"
                  >
                    {{ item.status }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.item-tech {
  transition: all 0.3s ease-in-out; 
  background-color: rgba(255, 255, 255, 0.05); 
}

.item-tech:hover {
  background-color: rgba(255, 255, 255, 0.15); /* Darker on hover */
  transform: translateY(-5px); /* Slight lift effect */
  box-shadow: 0 10px 15px rgba(0, 0, 0, 0.3); /* Drop shadow for depth */
}

/* Add a soft glow effect to images on hover */
.item-tech:hover .img-tech {
  transform: scale(1.3); /* Enlarge image on hover */
  filter: brightness(1.2) drop-shadow(0 0 10px rgba(255, 255, 255, 0.5)); /* Brightness and glow */
}

.tech {
  font-size: 1rem;
  color: #e5e7eb; 
  transition: transform 0.3s;
}
</style>