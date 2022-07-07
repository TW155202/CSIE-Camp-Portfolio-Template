<script setup>
import { ref } from "vue";
import MdiGithub from "~icons/mdi/github";
import MdiInstagram from "~icons/mdi/instagram";
import Typing from "@components/Typing.vue";

const step = ref(0);
</script>
<template>
    <div class="w-full overflow-y-auto px-8 pt-16 sm:px-12 sm:pt-20 lg:px-16 lg:pt-24">
        <Typing
            v-if="step >= 0"
            @done="step++"
            text="My name is Patrick"
            class="mb-2 block text-2xl sm:text-3xl lg:text-4xl"
        />
        <Typing
            v-if="step >= 1"
            @done="step++"
            text="Been to Monaghan Collegiate School, Monaghan, Ireland."
            :speed="60"
        /><br />
        <Typing
            v-if="step >= 2"
            @done="step++"
            text="Studying in Dali Senior High School"
            :speed="60"
        />
        <a
            v-if="step >= 3"
            @done="step++"
            class="mt-4 flex items-center text-lg text-gray-500 transition-all hover:text-gray-700"
            href="https://instagram.com/feng_hsu0825?igshid=YmMyMTA2M2Y="
            target="_blank"
        >
            <MdiInstagram class="mr-1 inline-block" />
            <Typing v-if="step >= 2" @done="step++" text="Instagram" :speed="60" />
        </a>
    </div>
</template>
