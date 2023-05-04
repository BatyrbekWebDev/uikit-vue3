<script setup>
const props = defineProps({
  maxWidth: {
    type: String,
    default: '500px',
  },
  percent: {
    type: Number,
    required: true,
  },
  color: {
    type: String,
    default: 'primary',
  },
});
</script>

<template>
  <div class="progress-container" :style="[{ 'max-width': maxWidth }]">
    <div class="progress-percent" :style="[{'color': `var(--${color})`}]">{{ percent }}%</div>
    <div class="progress" :style="[{'background': `var(--${color}-hover)`}]">
      <div class="progress-bar" :style="[{ width: `${percent}%` }, {'background': `var(--${color}`}]"></div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.progress {
  height: 10px;
  border-radius: 4px;
  &-container {
    margin-bottom: 20px;
    overflow: hidden;
  }
  &-bar {
    background: #000;
    height: 100%;
    border-radius: 4px;
    transition: 0.5s;
  }
  &-percent {
    display: block;
    text-align: center;
    font-weight: bold;
    font-size: 17px;
    margin-bottom: 10px;
  }
}
</style>
