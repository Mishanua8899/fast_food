
<svelte:head>
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Главная</title>
    
</svelte:head>

<script>
    import { link } from "./routes.js"
</script>

<body>
<div class="container">
    <main class="content-box">
        <p>Я же знаю, что ты готов похавать. Так закажи чего-нибуть?</p>
        <button class="catalog-button"><a href="{link}" class="catalog-link">Заказать</a></button>
    </main>
</div>
</body>

<style> 

   
    body {
        max-width: 1440px;
        margin: 0;
        height: 750px;
        background-color: bisque;
    }
    .container {
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        margin: 0;
    }
    .content-box {
        width: 100%;
        height: 100%;
        display: flex;
        align-items: center;
        text-align: center; 
        flex-direction: column;
        justify-content: center;
    }

    .catalog-link {
        text-decoration: none;
        color: black;
        font-size:20px;
        
    }

    .catalog-button {
        border: 1px solid black;
        border-radius: 8px;
        background-color: white;
        width: 30%;
        height: 7%;
        transition: all ease 0.4s; 
        font-size: 15px;
        margin-top: 20px;
    }

    p {
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        font-size: 20px;
    }

    .catalog-button:hover {
        background-color: bisque;
        transition: all ease 0.4s; 
        border: 0px;

    }




</style>

