<script>
import Title from '$lib/title.svelte'
import '../styles/global.css'

</script>

<header>
    <Title title ="Ninja Gaming Guide"/>
</header>

<main>
    <!-- page content -->
    <slot></slot>
</main>

<footer>
    <a href="/">Home</a>
    <a href="/guides">View Guides</a>
    <a href="/about">About</a>

    <p>
        Copyright 2022 Cadculus
    </p>
</footer>

<style>
    header{
        display: flex;
        justify-content: center;
    }
    main{
        max-width: 960px;
        margin: 20px auto;
    } 

    footer{
        text-align: center;
    }

</style>