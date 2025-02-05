<template>
    <div>
        <form @submit.prevent="submitForm" action="">
            <div>
                <label for="name"> Name : {{ formValues.name }}  </label>   <br/>  <br/>
                <input type="text" id="name" v-model.trim.lazy="formValues.name" ><br/>  <br/>
            </div>

            <div>
                <label for="profile"> Profile Summary : {{formValues.profileSummary}} </label><br/>  <br/>
                <textarea name="profile" id="profile" cols="30" rows="10" v-model.lazy=" formValues.profileSummary " ></textarea><br/>  <br/>
            </div>

            <div>
                <label for="country"> Country : {{ formValues.country }} </label><br/>  <br/>
                <select name="country" id="country" v-model=" formValues.country " >
                    <option value=""> Select a country </option>
                    <option value="Benin"> Benin </option>
                    <option value="Togo"> Togo </option>
                    <option value="Niger"> Niger </option>
                </select><br/>  <br/>
            </div>


            <div>
                <label for="joblocation"> Job Location(s) : {{ formValues.joblocation }} </label><br/>  <br/>
                <select name="country" id="joblocation" multiple v-model=" formValues.joblocation " >
                    <option value=""> Select a country </option>
                    <option value="Benin"> Benin </option>
                    <option value="Togo"> Togo </option>
                    <option value="Niger"> Niger </option>
                </select><br/>  <br/>
            </div>


            <div>
                <input type="checkbox" id="remotework" v-model="formValues.remotework" true-value = "Yes" false-value = "No" >
                <label for="remotework"> Open to remote work?  {{ formValues.remotework }} </label> <br/>  <br/>
            </div>

            <div>
                <label for="skillset"> Skillsets : {{ formValues.skillset }} </label> <br/>  <br/>

                <input type="checkbox" id= "html" value="HTML" v-model="formValues.skillset" >
                <label for="html"> HTML </label><br/>  <br/>

                <input type="checkbox" id= "CSS" value = "CSS" v-model="formValues.skillset" >
                <label for="CSS"> CSS </label><br/>  <br/>

                <input type="checkbox" id= "javascript" value = "Javascript" v-model="formValues.skillset" >
                <label for="javascript"> Javascript </label><br/>  <br/>

                <input type="checkbox" id= "python" value = "Python" v-model="formValues.skillset" >
                <label for="python"> Python </label><br/>  <br/>
            </div>

            <div>
                <label for="yearsofexperience"> Years of experience : {{ formValues.yearsOfExperience }} </label> <br/>  <br/>

                <input type="radio" id= "0-2" value="0-2" v-model="formValues.yearsOfExperience" >
                <label for="0-2"> 0 - 2 </label><br/>  <br/>

                <input type="radio" id= "3-4" value = "3-4" v-model="formValues.yearsOfExperience" >
                <label for="3-4"> 3 - 4 </label><br/>  <br/>

                <input type="radio" id= "4-5" value = "4-5" v-model="formValues.yearsOfExperience" >
                <label for="4-5"> 4 - 5 </label><br/>  <br/>

                <input type="radio" id= "5+" value = "5+" v-model="formValues.yearsOfExperience" >
                <label for="5+"> 5+ </label><br/>  <br/>

            </div>

            <div>
                <label for="age"> Age : {{ formValues.age }} </label><br/>  <br/>
                <input type="number" id = "age" v-model.number="formValues.age" max="120" min="0" ><br/>  <br/>
            </div>

            <div>
                <button> Submit </button>
            </div>

        </form>
    </div>
</template>

<script>
    export default {
        name : "FormHandling",
        data(){
            return {
                formValues : {
                    name : "",
                    profileSummary : "",
                    country : "",
                    joblocation : [],
                    remotework : "No",
                    skillset : [],
                    yearsOfExperience : "",
                    age : null
                }
            }
        },
        methods : {
            // submitForm(event){

            //     event.preventDefault()
            //     console.log("Form Values :", this.formValues)

            // },

            submitForm(){
                console.log("Form Values :", this.formValues)

            },

        },

    }
</script>

<style scoped>
form {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 8px;
}
label {
    display: block;
    margin-bottom: 8px;
    font-weight: bold;
}
input, textarea, select {
    width: 100%;
    padding: 8px;
    margin-bottom: 16px;
    border: 1px solid #ccc;
    border-radius: 4px;
}
button {
    padding: 10px 20px;
    background-color: #42b983;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}
button:hover {
    background-color: #369f6e;
}
</style>