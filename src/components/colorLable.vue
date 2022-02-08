<template>
  <div class="single-color" v-bind:style="{ background: color}" >
      <label>{{color}}</label>
      <button type="submit" v-on:click="onRemove(color)" disabled="isFavorite"> Remove </button>
  </div>
</template>

<script>

export default {
    name: 'App',
    components: {},
    props: ['color', 'onRemove'], 
    data () {
    return {
        isFavorite: false
    }
    },
    methods:{}
   
}
</script>

<style>
.single-color { 
	padding: 0px; 
	margin-top: 5px; 
	margin-bottom: 5px; 
	border: 1px solid gray; 
	border-radius: 10px; 
	width: 300px;
    
}
button{
    background-color: rgb(53, 128, 241);
    color: white;
    border-radius: 5px; 
    font-size: 50%;
    padding: 7px;
    align-items: right;

}
</style>
