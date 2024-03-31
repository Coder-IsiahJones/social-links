<script lang="ts" setup>
import LinkItem from "@/components/LinkItem.vue";
import { ref } from "vue";

const links = ref([
  {
    id: 1,
    text: "GitHub",
    link: "https://github.com",
  },
  {
    id: 2,
    text: "Frontend Mentor",
    link: "https://www.frontendmentor.io",
  },
  {
    id: 3,
    text: "LinkedIn",
    link: "https://www.linkedin.com",
  },
  {
    id: 4,
    text: "Twitter",
    link: "https://twitter.com",
  },
  {
    id: 5,
    text: "Instagram",
    link: "https://www.instagram.com",
  },
]);
</script>

<template>
  <div
    class="bg-[#1F1F1F] rounded-lg h-[579px] w-[384px] mx-6 flex flex-col py-6 gap-6 items-center"
  >
    <img
      class="w-20 h-20 rounded-full"
      src="/public/avatar-jessica.jpeg"
      alt="avatar image"
    />

    <h2 class="text-white text-[24px] font-semibold">Jessica Randall</h2>
    <p class="text-[#C4F82A] font-bold text-[14px]">London, United Kingdom</p>

    <p class="text-white text-[14px]">"Front-end developer and avid reader."</p>

    <LinkItem
      v-for="item in links"
      :text="item.text"
      :link="item.link"
      :key="item.id"
    />
  </div>
</template>
