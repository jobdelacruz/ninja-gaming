<script context='module'>
        export async function load({fetch, params}){ //page already replace with params
        //delay sometimes need if more data fetching from the server
        await new Promise(resolve => setTimeout(resolve,1000))
        const id = params.id
        const res = await fetch(`http://127.0.0.1:8000/posts/${id}.json`)
        const guide = await res.json()
        console.log(guide)
    
       if (res.ok){
           return{
               props:{
                   guide
               }
           }
       }
       return{
           status: 301,
        //    error: new Error('Could not fetch the guide')
        //redirect: '/guides'
       }
    }
    </script>
<script>
    export let guide
</script>
<div class="guide">
    <h2>{guide.title}</h2>
    <p>{guide.body}</p>
</div>

<style>
    .guide{
        margin-top: 40px;
        padding: 10px;
        border: 1px dotted rgb(255,255,255,0.2);
    }
</style>