<template>
  <div id="skills" class="columns">
    <div class="column is-5">
    <progress-bar v-for="language in languages" :size="'small'" :value="language[1]" :skill="language[0]" :max="5"></progress-bar>
    </div>
    <div class="column"></div>
    <div class="column is-5">
        <progress-bar v-for="framework in frameworks" :size="'small'" :value="framework[1]" :skill="framework[0]" :max="5"></progress-bar>
    </div> 
  </div>
</template>


<script>
import ProgressBar from './ProgressBar.vue';
export default {
    data() {
        return {
            frameworks: null,
            languages: null,
        }
    },
    components:{
        ProgressBar
    },
    methods: {
        getData() {
        let self = this;
        this.$http.get('https://cover-dd6f0.firebaseio.com/skills.json').then(response => {
          return response.json();
          }, error => {
    
          }).then(data => {
            //self.frameworks = data.framewroks
            self.frameworks = Object.entries(data.framewroks).sort(function(a,b) {
                return b[1]- a[1];
            }),
            //self.languages = data.languages;
            self.languages = Object.entries(data.languages).sort(function(a,b) {
                return b[1]- a[1];
            })
          });
        },
    },
    created() {
        this.getData();
    }
}
</script>


<style scoped>
#skills {
    width:90%;
    margin: auto
}
</style>