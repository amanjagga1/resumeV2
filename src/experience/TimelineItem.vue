<template>
  <span>
  <li class="timeline-item">
    <div class="timeline-marker">
    </div>
    <div class="timeline-content">
      <p class="heading is-size-4"><strong>{{item.company}}</strong></p>
      <p>{{item.description}}</p>
    </div>
  </li>
  <li class="timeline-header">
    <span :class="['tag', 'is-large', type]">{{item.startDate}}</span>
  </li>
  </span>
</template>


<script>
export default {
  props: {
    item:Object,
    type:String
  }
}

</script>


<style lang="scss">
</style>