<script setup>
import { ref } from 'vue';
import Tabs from '@/components/Tabs.vue';
const tabs = [
  { name: 'About', label: 'О проекте' },
  { name: 'Vue', label: 'Про Vue' },
  { name: 'React', label: 'Про React' },
];

const selectedTab = ref('Vue');
const changeTab = (tabName) => {
  selectedTab.value = tabName;
};
</script>

<template>
  <h1 class="heading-1">Tabs</h1>
  <Tabs :selectedTab="selectedTab" :names="tabs" @changeTab="changeTab">
    <div v-if="selectedTab === 'About'">Lorem ipsum dolor sit amet.</div>
    <div v-if="selectedTab === 'Vue'">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam, delectus.</div>
    <div v-if="selectedTab === 'React'">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Vel cum saepe voluptas ipsum quisquam obcaecati?</div>
  </Tabs>
</template>
