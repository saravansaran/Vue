<script>
    export default{
        data(){
            return{
                name:"saravan",
                isDisabled:false,
                checkList:false,
                title:"Default Title",
                formValues:{
                    name:"",
                    description:"",
                    gender:"",
                    languages:[],
                }
            }
        },
        methods:{
            handleClick()
            {
                this.title = "Updated Title"
            },
            formSubmit(event)
            {
                event.preventDefault();
                console.log("form values", this.formValues);
            }
        }
    }
</script>

<template>
  <!-- <h2>Text Binding Example</h2><br>
  <h3>Hello {{ name }}</h3>
  <h4 v-text="name"></h4>
  <br>
  <button v-bind:disabled="isDisabled">disabled</button>
  <br><br>
  <div v-if="checkList">this will display if checkList is true</div>
  <div v-else>checkList is false</div>
  <br>
  <h2>{{ title }}</h2>
    <button v-on:click="handleClick">Click to change the title</button>
    <hr> -->
    <pre>
        {{ JSON.stringify(formValues, null, 1) }}
    </pre>
    <form v-on:submit="formSubmit">
        <div>
            <label for="">Name</label>
            <input type="text" v-model="formValues.name"/>
        </div>
        <div>
            <label for="">Description</label>
            <textarea v-model="formValues.description"></textarea>
        </div>
        <div>
            <label for="">Gender</label>
            <select v-model="formValues.gender">
                <option value="male">Male</option>
                <option value="female">Female</option>
            </select>
        </div>
        <div>
            <input type="checkbox" v-model="formValues.languages" value="tamil" id="tamil"/> 
            <label for="tamil">Tamil</label>
        </div>
        <div>
            <input type="checkbox" v-model="formValues.languages" value="english" id="english"/> 
            <label for="english">English</label>
        </div>
        <button>Submit</button>
    </form>
</template>

<style>
    form div
    {
        display: flex;
        flex-direction: column;
        margin-bottom:20px;
    }
    form div label
    {
        margin-bottom:10px;
    }
    form div input, select, textarea
    {
        height: 30px;
    }
</style>
