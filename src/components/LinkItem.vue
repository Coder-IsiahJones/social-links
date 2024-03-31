<script lang="ts" setup>
import { defineProps } from "vue";

const props = defineProps({
  text: {
    type: String,
    required: true,
  },

  link: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <a
    :href="link"
    class="bg-[#333333] w-[279px] hover:bg-[#C4F82A] cursor-pointer hover:text-[#333333] h-[45px] rounded-[8px] text-white flex justify-center items-center text-[14px] font-bold"
  >
    {{ text }}
  </a>
</template>
