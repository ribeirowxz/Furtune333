# Furtune333
300 + 30 + 3 A cartinha vem.
projeto-aposta/
│
├── index.html
├── style.css
└── script.js
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Site de Apostas</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Site de Apostas</h1>
    </header>

    <main>
        <section id="apostas">
            <h2>Faça sua Aposta</h2>
            <input type="number" id="valorAposta" placeholder="Valor da Aposta">
            <button id="apostarBtn">Apostar</button>
        </section>

        <section id="resultado">
            <h2>Resultado</h2>
            <p id="mensagemResultado"></p>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Site de Apostas</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
}

header, footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
}

main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 70vh;
}

section {
    margin: 20px;
    padding: 20px;
    border: 1px solid #ccc;
}

input[type="number"], button {
    margin-bottom: 10px;
    padding: 5px;
}

button {
    cursor: pointer;
    background-color: #333;
    color: #fff;
    border: none;
}

button:hover {
    background-color: #555;
}

#resultado {
    display: none;
    text-align: center;
}
document.getElementById('apostarBtn').addEventListener('click', function() {
    var valorAposta = parseInt(document.getElementById('valorAposta').value);
    var resultado = Math.random() >= 0.5; // Simula um resultado aleatório

    var mensagemResultado = document.getElementById('mensagemResultado');
    mensagemResultado.textContent = resultado ? 'Você Ganhou!' : 'Você Perdeu!';
    mensagemResultado.style.color = resultado ? 'green' : 'red';

    var resultadoSection = document.getElementById('resultado');
    resultadoSection.style.display = 'block';
});
