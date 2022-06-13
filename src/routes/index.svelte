<script>
    import Title from '$lib/title.svelte'
    let title = "Ninja Gaming Guide"
    let count = 1
    const updateTitle = ()=>{
        title = "Something change in the title " + count
        count += 1
    }
</script>

<Title/>
<div class="index">
    <h2>{title}</h2>
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer vitae diam at augue sagittis eleifend ac vel quam. Cras vestibulum orci magna, feugiat consequat leo bibendum vitae. Suspendisse gravida ullamcorper velit ac interdum. Pellentesque vitae magna et erat imperdiet suscipit sit amet non ligula. Quisque eget tincidunt odio. Duis semper orci et placerat tincidunt. Sed euismod facilisis imperdiet. Nam dictum sit amet sem sed molestie. Praesent condimentum, enim eget ornare sollicitudin, turpis velit venenatis leo, nec iaculis quam metus rhoncus dolor.
    </p>
    <button on:click={updateTitle}>Change title</button>
    <input type="text" bind:value={title}>

</div>

<style>
    .index{
        text-align: center;
        display: block;
        margin:  20px auto;
    }
</style>
