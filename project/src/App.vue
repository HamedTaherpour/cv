<script setup>
// https://www.sejda.com/html-to-pdf
const experiences = [
  {
    jobTitle: "Front-end Developer",
    company: {
      title: "ArzDigital",
      link: "https://beta.arzdigital.com",
    },
    startDate: "Feb, 2021",
    endDate: "Present",
    city: "Karaj",
    description: "ArzDigital is the leading news agency in Iran's cryptocurrency industry, serving over 30M monthly active users and providing trading assistance services.",
    stack: ["Vue.js", "Nuxt.js", "TypeScript", "Tailwind CSS", "Nx", "Shadcn"],
    bullet: [
      "Contributed to the largest Persian-language crypto website.",
      "Implemented Nx monorepo with multiple Nuxt 3 apps.",
      "Shared components and configs via libs/ structure.",
      "Built internal Design System with TailwindCSS and Shadcn.",
      "Implemented real-time data with Centrifugo WebSocket.",
      "Created interactive dashboards with Highcharts and TradingView.",
      "Optimized SSR and SEO in Nuxt.",
      "Improved performance: reduced load time and enabled service caching.",
    ],
  },
  {
    jobTitle: "Front-end Developer",
    company: {
      title: "Pol",
      link: "https://poltalk.me/",
    },
    startDate: "April, 2023",
    endDate: "December ",
    city: "Remote PartTime",
    description: "Pol is a website and application for online video consultations with psychologists and psychiatrists, providing access to experts in psychology at any time and place.",
    stack: ["Nuxt.js", "TypeScript", "Tailwind CSS", "VueUse", "SSR", "Github"],
    bullet: ["Designing and developing the front-end using the Nuxt.js framework.", "Utilizing reusable components and achieving rapid code execution with Nuxt.js", "Using Tailwind CSS for responsive and visually appealing design.", "Optimizing code and user experience with Nuxt.js and Tailwind CSS.", "Implementing server-side rendering (SSR) with Nuxt.js to enhance SEO performance."],
  },
  {
    jobTitle: "Front-end Developer",
    company: {
      title: "Majaziland",
      link: "https://majaziland.me",
    },
    startDate: "Feb, 2020",
    endDate: "Feb, 2021",
    city: "Karaj",
    description: "Iran's Majaziland crypto exchange currently serves over <strong>3,000 users</strong> for buying and selling cryptocurrency.",
    stack: ["Vue.js", "TypeScript", "Tailwind CSS", "Vuetify", "Gitlab"],
    bullet: ["I designed and developed a user-friendly and intuitive UI/UX for a digital currency exchange platform, resulting in improved user engagement and satisfaction. As a result, daily transaction <strong>volume increased from 50 to 250.</strong>", "I implemented a seamless and secure user verification process to ensure compliance with regulations and mitigate the risk of fraud. This led to a reduction in the number of <strong>support staff from 5 to 2.</strong>", "Designed and maintained an advanced admin panel with robust features for efficient customer support and streamlined management, resulting in increased operational efficiency and higher customer satisfaction."],
  },
  {
    jobTitle: "Web Developer",
    company: {
      title: "Nezaco",
      link: "https://nezaco.ir",
    },
    startDate: "Feb, 2017",
    endDate: "Feb, 2020",
    city: "Tehran",
    description: "Nezaco is a game development company with one of its products being <a href='https://sahabapps.com'>Sahab</a>, a web-based software that specializes in accounting and inventory management for stores and restaurants.",
    stack: ["jQuery", "UIKit", "Bootstrap", "PHP", "CodeIgniter", "MySQL", "Gitlab"],
    bullet: ["Developed a restaurant website for accounting and inventory management using PHP and MySQL.", "Developed and implemented an email-based messaging and ticketing service.", "Connecting the application to hardware such as barcode scanners for restaurants and stores."],
  },
];

const ConceptKnowledge = ["VCS (Git)"];

const skills = ["Vue.js", "Nuxt.js", "React.js", "Next.js", "Tailwind CSS", "Cursor", "Design System", "Design Components", "Shadcn", "VueUse", "Vite", "SSR", "TypeScript", "Highcharts", "Storybook", "Gitlab", "Quasar", "Vuetify", "jQuery", "UIKit", "Bootstrap"];
</script>

<template>
  <div class="w-full overflow-hidden bg-[url(/img/beams.jpg)]">
    <div class="w-[950px] mx-auto relative pb-10">
      <div class="relative flex flex-col w-11/12 mx-auto">
        <div class="mt-10 flex flex-row">
          <div class="flex w-8/12 flex-row items-center">
            <div class="flex flex-col items-start">
              <h1 class="text-3xl font-bold">Hamed Taherpour</h1>
              <h4 class="text-2xl font-semibold text-slate-600 border-b-2 border-dashed border-sky-500">Front-end
                Developer</h4>
            </div>
          </div>
          <div class="flex w-4/12 flex-col gap-y-1 text-lg px-4">
            <a href="tel:09371508754" class="font-medium text-gray-800">(+98) 937-150-8754</a>
            <a href="mailto: dev.hamedt@gmail.com">dev.hamedt@gmail.com</a>
            <div class="flex w-full flex-row gap-x-5">
              <a href="https://github.com/HamedTaherpour" class="capitalize">github</a>
              <a href="https://www.linkedin.com/in/hamed-taherpour-6a8558200/" class="capitalize">linkedin</a>
              <a href="https://t.me/HamedTaherpour" class="capitalize">telegram</a>
            </div>
          </div>
        </div>
        <div class="flex flex-col mt-10 items-start">
          <h4 class="section-title"> <span>About Me</span></h4>
          <p class="font-semibold text-slate-700">
            Experienced Front-end Developer with over 7 years of expertise in building and optimizing web applications.
            Specializing in Vue.js and Nuxt.js, I have a strong background in developing scalable, high-performance web
            solutions, creating interactive dashboards, and improving user experience. Proven ability to lead projects,
            implement best practices, and collaborate effectively to deliver impactful results. </p>
        </div>
        <div class="mt-10 flex flex-row">
          <div class="flex w-8/12 flex-col items-start">
            <h4 class="section-title"><span>EXPERIENCES</span></h4>
            <div class="flex flex-col mb-5" v-for="item in experiences" :key="item.company.title">
              <h2 class="text-base font-bold text-black"><a :href="item.company.link" v-text="item.company.title"></a>,
                {{ item.city }} - {{ item.jobTitle }}</h2>
              <div class="mt-1 mb-2 text-xs text-slate-500">{{ item.startDate }} - {{ item.endDate }}</div>
              <div class="text-sm text-slate-700">
                <p class="text-slate-800" v-html="item.description"></p>
                <ul v-if="item.bullet.length > 0" class="list-inside list-disc text-sm space-y-2 mt-2">
                  <li v-for="bullet in item.bullet" v-html="bullet" :key="bullet"></li>
                </ul>
              </div>
            </div>
          </div>
          <div class="flex w-4/12 flex-col items-start px-4">
            <h4 class="section-title"><span>SKILLS</span></h4>
            <span class="font-bold">Tools / Technologies: </span>
            <ul class="list-inside list-disc font-semibold text-sm space-y-2 mt-1">
              <li v-for="item in skills" :key="item" v-text="item" class=""></li>
            </ul>
            <span class="font-bold mt-4">Concept / Knowledge: </span>
            <ul class="list-inside list-disc font-semibold text-sm space-y-2 mt-1">
              <li v-for="item in ConceptKnowledge" :key="item" v-text="item"></li>
            </ul>
            <h4 class="section-title mt-5"><span>EDUCATION</span></h4>
            <div>
              <h2 class="text-base font-bold text-black">Kardani of Qods - Tehran Qods</h2>
              <div class="mt-1 mb-2 text-xs text-slate-700">2017</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
