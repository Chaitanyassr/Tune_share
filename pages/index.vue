<template>
 <div>
 <h1>Search Itunes</h1>
 <br/>
 <form @submit.prevent="submit">
 <input placeholder="Enter Artist name" v-model="search" autofocus />
 </form>
 </div>
</template>

<script>

import ToolBar from '~/components/Toolbar.vue';
export default {
  components: {
  ToolBar
  },
  data(){
  return{
  search: ''
  }
  },
  methods: {
  submit(event){
      this.$router.push('results/${this.search}');
  }
  }
}

</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
