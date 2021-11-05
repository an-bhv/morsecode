<script>
import { createEventDispatcher } from 'svelte';

const dispatch = createEventDispatcher();

let txt;

const onSubmit = (e) => {
    e.preventDefault();
    dispatch("txt",txt);
    txt = "";
}

</script>


<form class="grid-3" on:submit="{onSubmit}">

<input type='text' id='txt' placeholder="Type morse code here, add space by adding ' / '" bind:value="{txt}">
<br>
<input type='submit'>

</form>



<style>

.grid-3{
    text-align: center;
}
#txt{
      height:100px;
      width: 1000px;
    font-size:14pt;
}

</style>