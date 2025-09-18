<script>
	import { isString } from "util";

    
    let {temperature = Number(2.2)} = $props();
    let increment = 1
    let char = "#"

    let stringBar = ""
    stringBar = () =>{
        tempString = ""
        for(i = 0; i < temperature; i+= increment){

        }
        return tempString;
    }


</script>

<div>
    <p>{temperature}</p>
    <p>{stringBar}</p>
</div>


<style>
    div{
        background-color: red;
        size: 500px;
    }
</style>

