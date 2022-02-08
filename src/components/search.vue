<template>
  <div class="divSearch">
    <label for="search">Search</label>    
     <input type="text" id="search" v-model="searchValue">

     <input type="radio" id="radioS" v-model="checked">
    <label for="radioS">Starts with</label>
  <input type="radio" id="radioE" v-model="checked">
    <label for="radioE"> Ends with</label>
  <input type="radio" id="radioC" v-model="checked">
    <label for="radioC">Contains</label>

    <input type="checkbox" id="checkbox" v-model="checked">
    <label for="checkbox">{{ checkData }}</label>
  </div>
</template>

<script>

export default {
  name: 'Search',
  props: ["onSearch"],
  data () {
  return {
      checked: true,
      searchValue: "",
        radioSelect: "contains"
  }
},
computed: {
    checkData(){
        return this.checked? "enabling" : "disabling"
    } 
}
}
</script>

<style>

.divSearch { 
	background-color: lightgray; 
	padding: 10px; 
	border-radius: 10px; 

}

input{ 
	border-radius: 10px; 
	padding: 5px 
}
</style>
