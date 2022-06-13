<script>
    //if with export then other components can overwrite the default value
    export let title = "Ninja Gaming"
</script>
<div class="title">
    <img src="/controller.svg" alt="site logo">
    <h1>{title}</h1>
</div>

<style>
    .title{
        display: flex;
        align-items: center;
            }
    .title img{
        display: inline-block;
        filter: invert(86%) sepia(18%) saturate(886%) hue-rotate(199deg) brightness(100%) contrast(90%);
        width: 3rem;
        height: 3rem;
        
    }
    .title h1{
        margin-left: 10px;
        
    }
</style>