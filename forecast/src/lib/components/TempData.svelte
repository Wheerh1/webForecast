<script>
	

    
    let {temperature = 2.2} = $props();
    let increment = 0.2
    let char = "#"

    function stringBar(){
        let tempString = ""
        for(let i = 0; i < temperature; i+= increment){
            tempString += char
        }
        return tempString;
    }


</script>

<div>
    <p>{temperature}</p>
    <p>{stringBar()}</p>
</div>


<style>
    div{
        background-color: red;
        size: 500px;
    }
</style>

