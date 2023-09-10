<svelte:head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
    <title>Каталог</title>
</svelte:head>

<script>
    import { catalog } from "./routes.js"
</script>

<body>
    <div class="container">
        <div class="catalog">
        {#each catalog as burger}
            <div class="burger">
                <h1 class="header">{burger.name}</h1>
                <img src="../src/lib/images/{burger.img}" alt="burger" class="img_burg">
                <button class="zakaz"><h1>Заказать</h1></button>
                <div class="order-window">
                    <h2>Оформление заказа</h2>
                    <form>
                        <label for="name">Имя:</label>
                        <input type="text" id="name" name="name" required>
                    
                        <label for="email">Email:</label>
                        <input type="email" id="email" name="email" required>
                        <label for="phone">Телефон:</label>
                        <input type="tel" id="phone" name="phone" required>
                        <label for="address">Адрес доставки:</label>
                        <input type="text" id="address" name="address" required>
                        <button type="submit">Отправить заказ</button>
                    </form>
                </div>
            </div>
        {/each}
        </div>
    </div>
</body>


<style>
    body {
        max-width: 1440px;
        margin: 0;
        height: 750px;
        background-color: bisque;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }

    .container {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        margin: 0;
       
    }

    .catalog {
        width: 100%;
        height: 95%;
        display: flex;
        margin-top: 5%;
        flex-wrap: wrap;
        align-content:space-between;
    }

    .burger {
        width: 25%;
        height: 45%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-bottom: 5%;
    }

    .img_burg {
        width: 200px;
        height: 100px;
        transition: all ease-in 0.3s;
    }
    
    .header {
        font-size: large;
    }

    .zakaz {
        border: none;
        border-radius: 10px;
        display: none;
        width: 50%;
        background-color: bisque;
        transition: all 0.3s ease-in ;
        height: 10%;
        font-weight: 400;
    }

    .burger:hover .zakaz {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .zakaz:hover {
        background-color: whitesmoke ;
        transition: all 0.3s ease-in ;
    }
    
    .burger:hover .img_burg {
        height: 125px;
        width: 250px;
        transition: all ease-in 0.3s;
    }
    
    .zakaz h1 {
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        font-size: larger;
    }

    .order-window {
        display:none;
    }

    form {
        display: flex;
        flex-direction: column;
    }
</style>