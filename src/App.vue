<script>
    export default{
        data(){
            return{
                name:"saravan",
                isDisabled:false,
            }
        }
    }
</script>

<template>
  <h2>Text Binding Example</h2><br>
  <h3>Hello {{ name }}</h3>
  <h4 v-text="name"></h4>
  <br>
  <button v-bind:disabled="isDisabled">disabled</button>
</template>

<style>

</style>
