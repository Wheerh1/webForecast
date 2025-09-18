<script>
import { createEventDispatcher } from 'svelte';

const dispatch = createEventDispatcher();


let {styleLight = "$lb/styleLight.css", styleDark = "$lib/styleDark.css" } = $props();
let styleCheck = 0;

function handleClick() {
    if(styleCheck === 0){
        dispatch('ThemeChange', {detail: '$lib/styleDark.css'});
        styleCheck = 1;
    }
    else if(styleCheck === 1) {
        dispatch('ThemeChange', {detail: '$lb/styleLight.css'});
    }
}


</script>

<button on:click={handleClick}>Change Theme</button>

