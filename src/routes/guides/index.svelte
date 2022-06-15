<script context='module'>
export async function load({fetch}){
   const response = await fetch('http://127.0.0.1:8000/posts.json')
   const guides = await response.json()
   console.log(guides)

   if (response.ok){
       return{
           props:{
               guides
           }
       }
   }
   return{
       status: response.status,
       error: new Error('Could not fetch the guieds')
   }
}
</script>

<script>
    export let guides
</script>


<div class="guides">
    <ul>
        {#each guides as guide}
            <li>
                <!-- prefetch the data when mouse over -->
                <a sveltekit:prefetch href={`/guides/${guide.id}`}>{guide.title}</a>
            </li>
        {/each}
    </ul>
</div>

<style>
    .guides {
        margin-top: 20px;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
    a{
        display: inline-block;
        margin: 10px;
        padding: 10px;
        border: 1px dotted rgb(255,255,255,0.2);
    }
</style>