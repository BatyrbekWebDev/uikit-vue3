<script setup>
import { ref } from 'vue';

import Radiobutton from '../components/Radiobutton.vue';

const footballClubs = ref([
  { name: 'Barcelona', id: 'f1' },
  { name: 'Real Madrid', id: 'f2' },
  { name: 'Chelsea', id: 'f3' },
  { name: 'Manchester United', id: 'f4' },
]);
const selectedClub = ref('');
const disabledRadio = ref(true);
const disabledRadioChecked = ref(true);
</script>

<template>
  <h1 class="heading-1">Checkbox</h1>
  <h2 class="heading-2">Basic</h2>
  <div class="line line_block">
    <p>Selected Club: {{ selectedClub }}</p>
    <div v-for="club in footballClubs" :key="club.id">
      <radiobutton
        :value="club.name"
        :label="club.name"
        :id="club.id"
        name="club"
        v-model:checkedValue="selectedClub"
      />
    </div>
  </div>
  <h2 class="heading-2">Disabled</h2>
  <div class="line">
    <radiobutton
      value="Radiobutton Disabled"
      label="Radiobutton Disabled"
      id="RadiobuttonDisabled"
      name="Radiobutton Disabled"
      :disabled="disabledRadio"
      v-model:checkedValue="disabledRadioChecked"
    />
  </div>
</template>
