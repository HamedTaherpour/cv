<script setup>
import { computed } from "@vue/runtime-core";

const experiences = [
  {
    jobTitle: "Front-end Developer",
    company: {
      title: "ArzDigital",
      link: "https://arzdigital.com",
    },
    startDate: "Feb, 2021",
    endDate: "Present",
    city: "Karaj",
    description: "ArzDigital is the leading news agency in Iran’s cryptocurrency industry with over 30M monthly active users and we provide trading assistance services.",
    stack: ["Vue.js", "Nuxt.js", "TypeScript", "Tailwind CSS", "Quasar", "Storybook", "VueUse", "Vite", "SSR", "Highcharts", "Gitlab"],
  },
  {
    jobTitle: "Front-end Developer",
    company: {
      title: "MagicalAPI",
      link: "https://magicalapi.com",
    },
    startDate: "Sep, 2022",
    endDate: "Present",
    city: "Remote",
    description: "MagicalAPI is a provider of cloud-based APIs for developers and companies.",
    stack: ["Vue.js", "Nuxt.js", "TypeScript", "Tailwind CSS", "Storybook", "VueUse", "Vite", "SSR", "Highcharts", "Gitlab"],
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
    description: "Iran's Majaziland crypto exchange has 3,000+ users for buying and selling crypto.",
    stack: ["Vue.js", "TypeScript", "Tailwind CSS", "Vuetify", "Gitlab"],
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
    description: "https://sahabapps.com",
    stack: ["jQuery", "UIKit", "Bootstrap", "PHP", "CodeIgniter", "MySQL", "Gitlab"],
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
  },
];

const ConceptKnowledge = ["Git", "Design System"];
const softSkills = ["Stress Management", "Risk Assessment", "Active Listening", "Patience"];

const skills = computed(() => {
  let skill = [];

  for (let item of experiences) {
    skill.push(...item.stack);
  }

  return new Set(skill);
});
</script>

<template>
  <div class="w-[950px] mx-auto relative">
    <img src="img/beams.jpg" alt="" class="absolute top-1/2 left-1/2 max-w-none -translate-x-1/2 -translate-y-1/2" />
    <div class="relative flex flex-col w-10/12 mx-auto">
      <div class="mt-10 flex flex-row">
        <div class="flex w-8/12 flex-row items-center">
          <img src="img/profile.jpg" class="rounded-full w-20 h-20 bg-cover object-cover mr-3" />
          <div class="flex flex-col">
            <h1 class="text-3xl font-bold">Hamed Taherpour</h1>
            <h4 class="mt-2 text-xl font-semibold text-gray-500">Front-end Developer</h4>
          </div>
        </div>
        <div class="flex w-4/12 flex-col gap-y-1 text-sm px-2">
          <span class="font-medium">(+98) 937-150-8754</span>
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
          <div>
            <h4 class="section-title">EXPERIENCES</h4>
            <div class="flex flex-col mb-5" v-for="item in experiences" :key="item.company.title">
              <h2 class="text-base font-bold text-black"><a :href="item.company.link" v-text="item.company.title"></a>, {{ item.city }} - {{ item.jobTitle }}</h2>
              <div class="mt-1 mb-2 text-xs text-gray-400">{{ item.startDate }} - {{ item.endDate }}</div>
              <div class="text-sm text-gray-500">
                <p v-text="item.description"></p>
                <div class="flex flex-wrap mt-1">
                  <span class="mr-0.5">Stack:</span>
                  <span v-for="(stack, index) in item.stack" :key="stack" class="px-0.5 text-xs font-semibold"> {{ stack }}<template v-if="index < item.stack.length - 1">,</template> </span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="flex w-4/12 flex-col px-2">
          <h4 class="section-title">SKILLS</h4>
          <span class="font-bold">Tools / Technologies: </span>
          <ul class="list-inside list-disc font-semibold text-sm space-y-2 mt-1">
            <li v-for="item in skills" :key="item" v-text="item"></li>
          </ul>
          <span class="font-bold mt-4">Concept / Knowledge: </span>
          <ul class="list-inside list-disc font-semibold text-sm space-y-2 mt-1">
            <li v-for="item in ConceptKnowledge" :key="item" v-text="item"></li>
          </ul>
          <h4 class="section-title mt-5">SOFT SKILLS</h4>
          <ul class="list-inside list-disc font-semibold text-sm space-y-2">
            <li v-for="item in softSkills" :key="item" v-text="item"></li>
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
</template>
