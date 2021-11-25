<template>
  <p class="reaction-time">Your reaction time: {{ score }} ms</p>
  <span class="rank">{{rank}}</span>
</template>

<script>
export default {
  props: ["score"],
  data(){
      return {
          rank: null
      }
  },
  mounted(){
      if(this.score < 250){
          this.rank = "Stenographer speed 🤩"
      }else if(this.score < 400){
          this.rank = "Rapid reflexes ☑️"
      } else {
          this.rank = "Snail pace 🐌. Try again..."
      }
  }
};
</script>

<style>
.reaction-time {
    font-size: 24px;
}
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>