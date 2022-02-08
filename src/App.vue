<template>
  <div id="app" class="clsCommon">
    <search :onSearch="onSearch.bind()"/> 
    <ListOfColors :searchValue="searchValue"/>
  </div>
</template>

<script>
import search from './components/search'
import ListOfColors from './components/listOfColors'

export default {
  name: 'App',
  components: {
    search,
    ListOfColors
  },
  data () {
  return {
    searchValue: ""
  }
},
methods:{
  onSearch:(color)=>{
    this.searchValue = color
  }
}
   
}
</script>

<style>
.clsCommon {
	font-size: 20px; 
	font-family: arial;
}

search{
      position: -webkit-sticky;
      position: sticky;
      top: 20px;

}

</style>
