<template>
  <div>
  <div class="progress-container is-flex">
    <span class="is-size-4">{{skill}}</span>
    <progress :class="['progress', type ? `is-${type}` : '', size ? `is-${size}` : '']" :value="value" :max="max"></progress>
    <span>{{percentage + '%'}}</span>
  </div>
  </div>
</template>

<script>
export default {
  props: {
    size: String,
    skill: String,
    value: {
      type: Number,
      required: true,
      default: 0
    },
    max: {
      type: Number,
      required: true,
      default: 0
    },
  },
  computed: {
    percentage () {
      return Math.floor(this.value / this.max * 100)
    },
    type () {
      let colors = ['','','danger','warning','primary','info'];
      return colors[Math.ceil(this.percentage / 20)];
    }
  }
}
</script>

<style lang="scss">
.progress-container {
  align-items: center;
  margin-bottom: 20px;
  .progress {
    position: relative;
    margin-bottom: 0 !important;
  }
  .progress + span {
    margin-left: 10px;
    min-width: 36px;
    text-align: right;
  }
  span {
    margin-right: 20px;
    min-width:120px;
    text-align: left;
    color: #fff;
  }
}
</style>