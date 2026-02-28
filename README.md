# color-damo
color link

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Color Changer App</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1>🎨 Color Changer App</h1>
        <button id="btn">Change Color</button>
        <p id="colorName">Color: #ffffff</p>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    margin: 0;
    padding: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Arial, sans-serif;
    background: #ffffff;
    transition: 0.5s;
}

.container {
    text-align: center;
    background: #000;
    padding: 40px;
    border-radius: 10px;
    color: #fff;
}

button {
    padding: 12px 20px;
    border: none;
    background: orange;
    color: #000;
    font-size: 16px;
    border-radius: 6px;
    cursor: pointer;
}

button:hover {
    background: yellow;
}
const btn = document.getElementById("btn");
const colorName = document.getElementById("colorName");

btn.addEventListener("click", () => {
    let randomColor = "#" + Math.floor(Math.random()*16777215).toString(16);
    document.body.style.background = randomColor;
    colorName.innerText = "Color: " + randomColor;
});
