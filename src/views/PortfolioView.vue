<script>
export default {
  data() {
    return {
      activeTab: 1,
      currentImage: 0, // Index of the current image for the Payment Link project
      personalProjects: [
        {
          id: 1,
          name: "Portfolio Website",
          images: "portfolio",
          description: "My personal website, which I designed to showcase my personality, skills, and projects. As well as my testing ground for new technologies that I learned during the 4-day Modern Full-Stack Hero Workshop in December 2023.",
          tech: "Vue.js, Tailwind",
          github: "https://github.com/amelraihana/portfolio",
          demo: "https://ame-portfolio.vercel.app/",
        },
        {
          id: 2,
          name: "IstiqamaTracker",
          images: "portfolio-istiqamatracker",
          description: "A comprehensive daily ibadah mobile tracker app for Muslims. Main features include trackers for daily prayers, Quran recitation and memorization, fasting, dhikr, and sadaqah, alongside additional features like user authentication, analytics, prayer times, countdown to the next prayer.",
          tech: "SwiftUI, Firebase",
          github: null,
          demo: null,
        },
        {
          id: 3,
          name: "Chess Game",
          images: "portfolio-chessgame",
          description: "A web-based interactive chess game that features dynamic piece movements and provides a user-friendly and interactive experience.",
          tech: "HTML, CSS, Javascript",
          github: "https://github.com/amelraihana/chess-game",
          demo: "https://ame-chess-game.vercel.app/",
        },
      ],
      others: [
        {
          id: 1,
          name: "Payment Link",
          images: [
            "payment-link-1",
            "payment-link-2",
            "payment-link-3",
            "payment-link-4",
          ],
          description: "Designed & developed an efficient payment link page with three distinct payment types, now actively used by merchants. The page dynamically adapts to the payment type and provides a seamless checkout experience to users.",
          tech: "HTML, CSS, JavaScript, jQuery, Bootstrap",
          github: null,
          demo: "https://www.betterpay.me/payment/link/?invoice-sample-INV0004A",
        },
        {
          id: 2,
          name: "Invoice Page",
          images: "invoice-page",
          description: "Developed a clear & organized invoice page that dynamically fetches and displays the invoice details from the BetterPay backend API. Merchants can now easily issue professional-looking invoices to their customers.",
          tech: "HTML, CSS, JavaScript, jQuery, Bootstrap",
          github: null,
          demo: "https://www.betterpay.me/payment/invoice/?id=65fbc11acbea5",
        },
        {
          id: 3,
          name: "API Design",
          images: "api-design",
          description: "Created Postman collections to streamline the API integration process for BetterPay's PRO and LITE APIs. Merchants can now seamlessly test API calls using the Postman collections designed, making it much easier for them to understand & integrate BetterPay systems.",
          tech: "Postman",
          github: "https://github.com/betterpayme/POSTMAN-APIs/tree/main",
          demo: null,
        },
      ],
    };
  },
  methods: {
    nextImage() {
      const item = this.others.find(o => o.name === 'Payment Link');
      if (this.currentImage < item.images.length - 1) {
        this.currentImage++;
      } else {
        this.currentImage = 0; // Loop back to the first image
      }
    },
    prevImage() {
      const item = this.others.find(o => o.name === 'Payment Link');
      if (this.currentImage > 0) {
        this.currentImage--;
      } else {
        this.currentImage = item.images.length - 1; // Loop to the last image
      }
    },
  },
};
</script>

<template>
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Personal Projects</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-pink-500">
            Explore the projects I've worked on so far
          </h4>
        </div>
      </header>

      <!-- Personal Projects Section -->
      <section>
        <div>
          <div
            class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in">
            <div v-for="item in personalProjects" :key="item.id">
              <div
                class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5">
                <div class="flex h-84 w-84 items-center justify-center p-0 h-full w-full lg:p-0 zoom-in">
                  <img alt="HTML" loading="lazy" decoding="async" data-nimg="1" class="drop-shadow-xl rounded-xl"
                    :src="'/' + item.images + '.png'" />
                </div>
                <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                  <div class="title-text font-medium text-secondary">
                    {{ item.name }}
                  </div>
                  <div class="w-full text-left text-[12px] text-[#c1c1c1] md:text-sm lg:text-base">
                    {{ item.description }}
                  </div>
                  <div class="w-full mt-4 text-normal text-sm text-left text-purple-200">
                    {{ item.tech }}
                  </div>
                  <div class="w-full flex justify-end">
                    <div class="flex cursor-pointer items-end gap-2 text-primary">
                      <a v-if="item.github !== null" :href="item.github" target="_blank" rel="noreferrer"
                        title="View github repository" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round"
                          stroke-linejoin="round" height="16" width="16" xmlns="http://www.w3.org/2000/svg">
                          <path
                            d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22">
                          </path>
                        </svg>
                      </a>
                      <a v-if="item.demo !== null" :href="item.demo" target="_blank" rel="noreferrer"
                        title="View finished project" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round"
                          stroke-linejoin="round" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
                          <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                          <polyline points="15 3 21 3 21 9"></polyline>
                          <line x1="10" y1="14" x2="21" y2="3"></line>
                        </svg>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>

    <article data-page="about">
      <header>
        <div
          class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Others</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-pink-500">
            Explore some of the projects I had proudly worked on during internship
          </h4>
        </div>
      </header>

      <!-- Professional Projects Section -->
      <section>
        <div>
          <div
            class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-3 md:gap-3 xl:grid-cols-3 xl:gap-3 2xl:gap-5 fade-zoom-in">
            <div v-for="item in others" :key="item.id">
              <div
                class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5">

                <!-- Carousel for Payment Link Project -->
                <div v-if="item.name === 'Payment Link'" class="relative w-full h-84 overflow-hidden">
                  <div class="flex transition-transform duration-300 ease-in-out"
                    :style="{ transform: `translateX(-${currentImage * 100}%)` }">
                    <img v-for="(img, index) in item.images" :key="index" :src="'/' + img + '.png'"
                      class="w-full h-full object-cover rounded-xl" />
                  </div>
                  <button @click="prevImage"
                    class="absolute top-1/2 left-2 transform -translate-y-1/2 bg-black bg-opacity-20 text-white rounded-full w-6 h-6 flex items-center justify-center shadow transition duration-200 hover:bg-opacity-30">
                    ←
                  </button>
                  <button @click="nextImage"
                    class="absolute top-1/2 right-2 transform -translate-y-1/2 bg-black bg-opacity-20 text-white rounded-full w-6 h- flex items-center justify-center shadow transition duration-200 hover:bg-opacity-30">
                    →
                  </button>
                </div>

                <div v-else class="flex h-84 w-84 items-center justify-center p-0 h-full w-full lg:p-0 zoom-in">
                  <img alt="HTML" loading="lazy" decoding="async" class="drop-shadow-xl rounded-xl"
                    :src="'/' + item.images + '.png'" />
                </div>

                <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                  <div class="title-text font-medium text-secondary">
                    {{ item.name }}
                  </div>
                  <div class="w-full text-left text-[12px] text-[#c1c1c1] md:text-sm lg:text-base">
                    {{ item.description }}
                  </div>
                  <div class="w-full mt-4 text-normal text-sm text-left text-purple-200">
                    {{ item.tech }}
                  </div>
                  <div class="w-full flex justify-end">
                    <div class="flex cursor-pointer items-end gap-2 text-primary">
                      <a v-if="item.github !== null" :href="item.github" target="_blank" rel="noreferrer"
                        title="View github repository" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round"
                          stroke-linejoin="round" height="16" width="16" xmlns="http://www.w3.org/2000/svg">
                          <path
                            d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22">
                          </path>
                        </svg>
                      </a>
                      <a v-if="item.demo !== null" :href="item.demo" target="_blank" rel="noreferrer"
                        title="View finished project" class="transition-all hover:text-accent">
                        <svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round"
                          stroke-linejoin="round" height="18" width="18" xmlns="http://www.w3.org/2000/svg">
                          <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                          <polyline points="15 3 21 3 21 9"></polyline>
                          <line x1="10" y1="14" x2="21" y2="3"></line>
                        </svg>
                      </a>
                    </div>
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

<style scoped>
.item-card:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
}

svg:hover {
  stroke: #ffdb70;
}

@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }

  100% {
    opacity: 1;
    transform: scale(1);
  }
}

.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}
</style>