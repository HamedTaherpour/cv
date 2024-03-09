<script setup>
// https://www.sejda.com/html-to-pdf
const experiences = [
  {
    jobTitle: "Front-end Developer",
    company: {
      title: "Pol",
      link: "https://poltalk.me/",
    },
    startDate: "August, 2023",
    endDate: "Present",
    city: "Remote",
    description: "Pol is actually a website and application through which you can have online video consultations with psychologists and psychiatrists. Paul gives you the ability to connect to the psychology of your desired expertise at any time and place.",
    stack: ["Nuxt.js", "TypeScript", "Tailwind CSS", "VueUse", "SSR", "Github"],
    bullet: ["Designing and developing the front-end of the website using the Nuxt.js framework", "Utilizing reusable components and achieving rapid code execution with Nuxt.js", "Using Tailwind CSS for responsive and visually appealing design by leveraging CSS utility classes.", "Optimizing code and user experience using Nuxt.js and Tailwind CSS", "Implementing server-side rendering (SSR) with Nuxt.js to enhance SEO performance by ensuring that search engines can easily crawl and index the website's content."],
  },
  {
    jobTitle: "Front-end Developer",
    company: {
      title: "ArzDigital",
      link: "https://arzdigital.com",
    },
    startDate: "Feb, 2021",
    endDate: "Feb, 2024",
    city: "Karaj",
    description: "ArzDigital is the leading news agency in Iran’s cryptocurrency industry with over 30M monthly active users and we provide trading assistance services.",
    stack: ["Vue.js", "Nuxt.js", "TypeScript", "Tailwind CSS", "Quasar", "Storybook", "VueUse", "Vite", "SSR", "Highcharts", "Gitlab"],
    bullet: ["Implemented server-side rendering to improve website SEO and speed, resulting in a better user experience.", "I improved website performance by chunking JavaScript files and separating code for each page into smaller files, resulting in faster loading times. This reduced the page load time <strong>from 3 seconds to 0.5 seconds.</strong>", "Developed and maintained a consistent design system for the project, resulting in improved visual coherence and an efficient development process. This helped to <strong>reduce 60% of the challenges and discussions</strong> related to design and development.", "Interview <strong>over 20 candidates</<strong>"],
  },
  {
    jobTitle: "Front-end Developer",
    company: {
      title: "MagicalAPI",
      link: "https://magicalapi.com",
    },
    startDate: "Sep, 2022",
    endDate: "Nov, 2022",
    city: "Remote",
    description: "MagicalAPI is a provider of cloud-based APIs for developers and companies.",
    stack: ["Vue.js", "Nuxt.js", "TypeScript", "Tailwind CSS", "Storybook", "VueUse", "Vite", "SSR", "Highcharts", "Gitlab"],
    bullet: ["I designed and implemented a unique and responsive landing page using Tailwind CSS, featuring various optimized animations to enhance user experience and reduce loading times."],
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
  {
    jobTitle: "Augmented Reality",
    company: {
      title: "Raro",
      link: "http://raro.ir",
    },
    startDate: "Mar, 2016",
    endDate: "Jul, 2016",
    city: "Tehran",
    description: "I created a Red Crescent base map program and provided emergency response training using augmented reality technology.",
    stack: ["Unity Engine", "Vuforia", "Augmented Reality"],
    bullet: ["Reduced app size from <strong>28MB to 11MB.</strong>", "Implemented the feature to read AR image targets from a server, ensuring the application stays up-to-date and can read daily newspaper articles."],
  },
  {
    jobTitle: "Game Developer",
    company: {
      title: "Path",
      link: "https://cafebazaar.ir/app/ir.HamedTaherpour.Path",
    },
    startDate: "Jun, 2015",
    endDate: "Sep, 2016",
    city: "",
    description: "Path A 2D game using Unity engine for the Android platform.",
    stack: ["Unity Engine", "Photoshop", "PHP", "MySQL"],
    bullet: ["The application features a <strong>high score</strong> system that is managed on a server."],
  },
];

const ConceptKnowledge = ["VCS (Git)"];

const skills = ["Vue.js", "Nuxt.js", "Tailwind CSS", "VueUse", "Vite", "SSR", "TypeScript", "Highcharts", "Storybook", "Gitlab", "Quasar", "Vuetify", "jQuery", "UIKit", "Bootstrap"];
</script>

<template>
  <div class="w-full overflow-hidden bg-[url(/img/beams.jpg)]">
    <div class="w-[950px] mx-auto relative pb-10">
      <div class="relative flex flex-col w-11/12 mx-auto">
        <div class="mt-10 flex flex-row">
          <div class="flex w-8/12 flex-row items-center">
            <img src="/img/profile.jpg" class="rounded-full w-20 h-20 bg-cover object-cover mr-3" />
            <div class="flex flex-col">
              <h1 class="text-2xl font-bold">Hamed Taherpour</h1>
              <h4 class="text-lg font-semibold text-gray-500">Front-end Developer</h4>
            </div>
          </div>
          <div class="flex w-4/12 flex-col gap-y-1 text-sm px-4">
            <a href="tel:09371508754" class="font-medium text-gray-800">(+98) 937-150-8754</a>
            <a href="mailto: dev.hamedt@gmail.com">dev.hamedt@gmail.com</a>
            <div class="flex w-full flex-row gap-x-5">
              <a href="https://github.com/HamedTaherpour" class="capitalize">github</a>
              <a href="https://www.linkedin.com/in/hamed-taherpour-6a8558200/" class="capitalize">linkedin</a>
              <a href="https://t.me/HamedTaherpour" class="capitalize">telegram</a>
            </div>
          </div>
        </div>
        <div class="mt-10 flex flex-row">
          <div class="flex w-8/12 flex-col">
            <h4 class="section-title">EXPERIENCES</h4>
            <div class="flex flex-col mb-5" v-for="item in experiences" :key="item.company.title">
              <h2 class="text-base font-bold text-black"><a :href="item.company.link" v-text="item.company.title"></a>, {{ item.city }} - {{ item.jobTitle }}</h2>
              <div class="mt-1 mb-2 text-xs text-gray-400">{{ item.startDate }} - {{ item.endDate }}</div>
              <div class="text-sm text-gray-600">
                <p v-html="item.description"></p>
                <div class="flex flex-wrap mt-1 gap-1 items-center">
                  <span class="mr-0.5 px-0.5 text-xs">Stack:</span>
                  <span v-for="stack in item.stack" :key="stack" class="text-[10px] font-semibold bg-sky-100 ring-1 ring-sky-200 rounded px-1">
                    {{ stack }}
                  </span>
                </div>
                <ul v-if="item.bullet.length > 0" class="list-inside list-disc text-xs space-y-2 mt-2">
                  <li v-for="bullet in item.bullet" v-html="bullet" :key="bullet" class="italic"></li>
                </ul>
              </div>
            </div>
          </div>
          <div class="flex w-4/12 flex-col px-4">
            <h4 class="section-title">SKILLS</h4>
            <span class="font-bold">Tools / Technologies: </span>
            <ul class="list-inside list-disc font-semibold text-sm space-y-2 mt-1">
              <li v-for="item in skills" :key="item" v-text="item" class=""></li>
            </ul>
            <span class="font-bold mt-4">Concept / Knowledge: </span>
            <ul class="list-inside list-disc font-semibold text-sm space-y-2 mt-1">
              <li v-for="item in ConceptKnowledge" :key="item" v-text="item"></li>
            </ul>
            <h4 class="section-title mt-5">EDUCATION</h4>
            <div>
              <h2 class="text-base font-bold text-black">Kardani of Qods - Tehran Qods</h2>
              <div class="mt-1 mb-2 text-xs text-gray-400">2017</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
