<script>
    const nav = [
        {
           link: "/about",
           title: "О нас"
        },
        {
            link: "/additionally",
            title: "Дополнительно"
        }
    ]
</script>

<nav>
    <div class='nav-container'>
        <a href="/" class="head-link" title="Back To Homepage">Тут типа лого</a>
        <div class="nav-links">
            {#each nav as page}
                <a href="{page.link}"class="link">{page.title}</a>
            {/each}
        </div>
    </div>
</nav>
<div class="container">
    <slot></slot>
</div>
<style>

    nav {
        width: 100%;
        height: 5%;
        margin: 0;
        padding-top: 10px;
        padding-left: 10px;
        position: fixed;
        overflow: hidden;
        background-color: whitesmoke;

    }
    .nav-container{
        width: 100%;
        height: 70%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        margin: 0;
        align-items: center;
    }

    .nav-links {
        width: 25%;
        display: flex;
        flex-direction: row-reverse;
        justify-content: space-between;
        text-align: center;
        padding-right: 20%;
    }

    .link {
        padding-right: 10px;
        text-decoration: none;
        color: black;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        text-align: start;
    }

    .head-link {
        text-decoration: none;
        color: black;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }

    @media screen and (max-width: 800px) {
        .nav-links {
            width: 40%;
        }
    }
    
</style>