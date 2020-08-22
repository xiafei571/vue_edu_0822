<template id="pop">
    <div>
        <p>{{result_data}}</p>

    </div>

</template>

<script>
import axios from "axios";

const url = "http://localhost:8081/pop/info/1";

export default {

    data(){
        return { result_data : "Hello world"}
    },

    mounted(){
        axios.get(url).then(response => (this.result_data = response.data)).catch(function(error){
            console.log(error)
        })
    }
};



</script>

<style>

</style>