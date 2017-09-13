<template>
<div id="experience">
<ul class="timeline">
  <li class="timeline-header">
    <span class="tag is-large is-danger">In Present</span>
  </li>
  <timeline-item v-for= "(experience, i) in experiences" :item = "experience" :type = "colors[i % 3]"></timeline-item>
</ul>
</div>
</template>


<script>
import TimelineItem from './TimelineItem.vue';
export default {
  components: {
    TimelineItem
  },
  data() {
    return {
      experiences: null,
      colors: ['is-info','is-primary','is-warning']
    }
  },
  methods: {
        getData() {
        let self = this;
        this.$http.get('https://cover-dd6f0.firebaseio.com/experiences.json').then(response => {
          return response.json();
          }, error => {
    
          }).then(data => {
            self.experiences = data
            console.log(self.experiences);
          });
        },
    },
    created() {
        this.getData();
    }
    
}
</script>


<style scoped>
#experience {
  width:90%;
  margin:auto
}
</style>