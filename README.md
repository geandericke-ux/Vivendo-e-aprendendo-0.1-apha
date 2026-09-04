<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Vivendo e Aprendendo</title>

<style>
:root {
    --preto: #090909;
    --preto2: #121212;
    --preto3: #1c1c1c;
    --dourado: #d4af37;
    --dourado-claro: #f4d675;
    --branco: #ffffff;
    --cinza: #aaaaaa;
    --verde: #38b26d;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
}

html {
    scroll-behavior: smooth;
}

body {
    background: var(--preto);
    color: var(--branco);
}

/* NAVBAR */

header {
    position: sticky;
    top: 0;
    z-index: 1000;
    background: rgba(9,9,9,0.95);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid #292929;
}

nav {
    max-width: 1200px;
    margin: auto;
    padding: 18px 25px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    color: var(--dourado);
    font-size: 24px;
    font-weight: bold;
    letter-spacing: 1px;
}

.logo span {
    color: white;
}

.menu {
    display: flex;
    gap: 25px;
}

.menu a {
    color: white;
    text-decoration: none;
    transition: 0.3s;
}

.menu a:hover {
    color: var(--dourado);
}

/* HERO */

.hero {
    min-height: 85vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 50px 20px;

    background:
    radial-gradient(circle at center,
    #2b240d 0%,
    #090909 60%);
}

.hero-content {
    max-width: 850px;
}

.va-logo {
    font-size: 110px;
    font-weight: bold;
    color: var(--dourado);
    text-shadow: 0 0 30px rgba(212,175,55,0.3);
}

.hero h1 {
    font-size: clamp(40px, 7vw, 80px);
    margin-bottom: 20px;
}

.hero h1 span {
    color: var(--dourado);
}

.hero p {
    color: var(--cinza);
    font-size: 19px;
    line-height: 1.6;
    margin-bottom: 30px;
}

.btn {
    border: none;
    padding: 15px 28px;
    border-radius: 10px;
    background: var(--dourado);
    color: black;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    transition: 0.3s;
}

.btn:hover {
    transform: scale(1.05);
    background: var(--dourado-claro);
}

/* SEÇÕES */

section {
    padding: 80px 25px;
}

.container {
    max-width: 1200px;
    margin: auto;
}

.titulo {
    text-align: center;
    margin-bottom: 50px;
}

.titulo h2 {
    font-size: 40px;
}

.titulo p {
    color: var(--cinza);
    margin-top: 10px;
}

/* PESQUISA */

.search-box {
    max-width: 600px;
    margin: 0 auto 40px;
}

.search-box input {
    width: 100%;
    padding: 16px;
    border-radius: 10px;
    border: 1px solid #333;
    background: var(--preto2);
    color: white;
    font-size: 16px;
}

.search-box input:focus {
    outline: 1px solid var(--dourado);
}

/* CARDS */

.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
    gap: 20px;
}

.card {
    background: var(--preto2);
    border: 1px solid #282828;
    border-radius: 15px;
    padding: 25px;
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-8px);
    border-color: var(--dourado);
}

.card .emoji {
    font-size: 40px;
}

.card h3 {
    margin: 15px 0 10px;
}

.card p {
    color: var(--cinza);
    line-height: 1.5;
}

/* PROGRESSO */

.progresso-box {
    background: var(--preto2);
    padding: 30px;
    border-radius: 15px;
    max-width: 700px;
    margin: auto;
}

.progress-bar {
    width: 100%;
    height: 18px;
    background: #292929;
    border-radius: 20px;
    overflow: hidden;
    margin: 20px 0;
}

.progress {
    width: 0%;
    height: 100%;
    background: linear-gradient(
        90deg,
        var(--dourado),
        var(--dourado-claro)
    );
    transition: 0.5s;
}

#porcentagem {
    color: var(--dourado);
    font-size: 25px;
    font-weight: bold;
}

/* QUIZ */

.quiz {
    max-width: 700px;
    margin: auto;
    background: var(--preto2);
    padding: 35px;
    border-radius: 15px;
    border: 1px solid #282828;
}

.quiz h3 {
    font-size: 22px;
    margin-bottom: 25px;
}

.opcao {
    width: 100%;
    text-align: left;
    padding: 15px;
    margin: 10px 0;
    background: var(--preto3);
    color: white;
    border: 1px solid #333;
    border-radius: 10px;
    cursor: pointer;
    transition: 0.2s;
}

.opcao:hover {
    border-color: var(--dourado);
}

.resultado {
    margin-top: 20px;
    font-weight: bold;
    font-size: 18px;
}

/* ANOTAÇÕES */

.notas {
    max-width: 800px;
    margin: auto;
}

textarea {
    width: 100%;
    min-height: 200px;
    background: var(--preto2);
    color: white;
    border: 1px solid #333;
    border-radius: 12px;
    padding: 20px;
    resize: vertical;
    font-size: 16px;
}

textarea:focus {
    outline: 1px solid var(--dourado);
}

.nota-info {
    color: var(--cinza);
    margin-top: 10px;
}

/* SOBRE */

.sobre {
    background: var(--preto2);
    border-radius: 20px;
    padding: 50px;
    text-align: center;
}

.sobre p {
    color: var(--cinza);
    line-height: 1.8;
    max-width: 700px;
    margin: 20px auto;
}

/* FOOTER */

footer {
    padding: 40px;
    text-align: center;
    border-top: 1px solid #282828;
    color: var(--cinza);
}

footer strong {
    color: var(--dourado);
}

/* MOBILE */

@media(max-width: 700px) {

    .menu {
        display: none;
    }

    .va-logo {
        font-size: 80px;
    }

    .sobre {
        padding: 30px 20px;
    }

}
</style>
</head>


<body>

<header>

<nav>

<div class="logo">
VA <span>| Vivendo e Aprendendo</span>
</div>

<div class="menu">
<a href="#aprender">Aprender</a>
<a href="#progresso">Progresso</a>
<a href="#quiz">Quiz</a>
<a href="#notas">Notas</a>
</div>

</nav>

</header>


<!-- HERO -->

<section class="hero">

<div class="hero-content">

<div class="va-logo">VA</div>

<h1>
Vivendo e <span>Aprendendo</span>
</h1>

<p>
O conhecimento não termina quando a escola acaba.
Cada experiência é uma oportunidade para aprender algo novo.
</p>

<button class="btn"
onclick="document.getElementById('aprender').scrollIntoView()">

Começar a aprender

</button>

</div>

</section>



<!-- APRENDER -->

<section id="aprender">

<div class="container">

<div class="titulo">

<h2>Explore o conhecimento</h2>

<p>
Escolha um assunto e comece sua jornada.
</p>

</div>


<div class="search-box">

<input
type="text"
id="pesquisa"
placeholder="🔎 Pesquisar um assunto..."
onkeyup="pesquisar()">

</div>


<div class="cards" id="cards">


<div class="card">

<div class="emoji">🧠</div>

<h3>Psicologia</h3>

<p>
Entenda melhor a mente humana,
comportamentos e emoções.
</p>

</div>


<div class="card">

<div class="emoji">🌍</div>

<h3>História</h3>

<p>
Descubra acontecimentos que
mudaram completamente o mundo.
</p>

</div>


<div class="card">

<div class="emoji">🔬</div>

<h3>Ciência</h3>

<p>
Explore o universo, a natureza
e os mistérios da ciência.
</p>

</div>


<div class="card">

<div class="emoji">💻</div>

<h3>Tecnologia</h3>

<p>
Aprenda sobre programação,
inteligência artificial e inovação.
</p>

</div>


<div class="card">

<div class="emoji">💰</div>

<h3>Finanças</h3>

<p>
Entenda melhor dinheiro,
economia e planejamento.
</p>

</div>


<div class="card">

<div class="emoji">🗣️</div>

<h3>Comunicação</h3>

<p>
Aprenda a se expressar
e melhorar suas relações.
</p>

</div>


</div>

</div>

</section>



<!-- PROGRESSO -->

<section id="progresso">

<div class="container">

<div class="titulo">

<h2>Seu progresso</h2>

<p>
Pequenos aprendizados criam grandes mudanças.
</p>

</div>


<div class="progresso-box">

<h3>Nível de aprendizado</h3>

<div class="progress-bar">

<div class="progress" id="barra"></div>

</div>

<div id="porcentagem">0%</div>

<br>

<button class="btn" onclick="aumentarProgresso()">

Concluir aprendizado

</button>

</div>

</div>

</section>



<!-- QUIZ -->

<section id="quiz">

<div class="container">

<div class="titulo">

<h2>Teste seus conhecimentos</h2>

<p>
Aprender também significa se desafiar.
</p>

</div>


<div class="quiz">

<h3 id="pergunta">

Qual é a principal função do aprendizado?

</h3>


<button class="opcao"
onclick="responder(false)">

Decorar tudo sem entender

</button>


<button class="opcao"
onclick="responder(true)">

Adquirir conhecimento e desenvolver habilidades

</button>


<button class="opcao"
onclick="responder(false)">

Apenas passar em provas

</button>


<button class="opcao"
onclick="responder(false)">

Nunca cometer erros

</button>


<div class="resultado" id="resultado"></div>

</div>

</div>

</section>



<!-- NOTAS -->

<section id="notas">

<div class="container">

<div class="titulo">

<h2>Suas anotações</h2>

<p>
Guarde aquilo que você aprendeu.
</p>

</div>


<div class="notas">

<textarea
id="anotacoes"
placeholder="Escreva aqui o que você aprendeu hoje..."
oninput="salvarNotas()">
</textarea>

<p class="nota-info">
💾 Suas anotações são salvas automaticamente neste dispositivo.
</p>

</div>

</div>

</section>



<!-- SOBRE -->

<section>

<div class="container">

<div class="sobre">

<h2>O que é o Vivendo e Aprendendo?</h2>

<p>

Vivendo e Aprendendo é um projeto criado com a ideia de que
o conhecimento não pertence apenas às escolas ou livros.

Todos os dias aprendemos através de experiências,
erros, conversas, descobertas e desafios.

</p>

<p>

Nosso objetivo é transformar a curiosidade em conhecimento
e tornar o aprendizado algo acessível para todos.

</p>

<button class="btn"
onclick="alert('Obrigado por fazer parte do Vivendo e Aprendendo!')">

Fazer parte do projeto

</button>

</div>

</div>

</section>



<footer>

<p>
© 2026 <strong>Vivendo e Aprendendo</strong>
</p>

<p>
Aprender é uma das formas mais poderosas de evoluir.
</p>

</footer>



<script>

/* =========================
SALVAR NOTAS
========================= */

const anotacoes = document.getElementById("anotacoes");

window.onload = function() {

    const notasSalvas =
    localStorage.getItem("notasVA");

    if(notasSalvas) {

        anotacoes.value =
        notasSalvas;

    }

    atualizarProgresso();

}


function salvarNotas() {

    localStorage.setItem(
        "notasVA",
        anotacoes.value
    );

}


/* =========================
PROGRESSO
========================= */

let progresso =
Number(
localStorage.getItem("progressoVA")
) || 0;


function aumentarProgresso() {

    if(progresso < 100) {

        progresso += 10;

        if(progresso > 100) {
            progresso = 100;
        }

        localStorage.setItem(
            "progressoVA",
            progresso
        );

        atualizarProgresso();

    }

}


function atualizarProgresso() {

    document.getElementById("barra")
    .style.width =
    progresso + "%";


    document.getElementById("porcentagem")
    .innerText =
    progresso + "%";

}


/* =========================
QUIZ
========================= */

function responder(correta) {

    const resultado =
    document.getElementById("resultado");


    if(correta) {

        resultado.innerHTML =
        "✅ Correto! Aprender é desenvolver conhecimentos e habilidades.";

        resultado.style.color =
        "#38b26d";

        if(progresso < 100) {

            progresso += 10;

            localStorage.setItem(
                "progressoVA",
                progresso
            );

            atualizarProgresso();

        }

    }

    else {

        resultado.innerHTML =
        "❌ Quase! Errar também faz parte do aprendizado.";

        resultado.style.color =
        "#ff6b6b";

    }

}


/* =========================
PESQUISA
========================= */

function pesquisar() {

    const texto =
    document.getElementById("pesquisa")
    .value
    .toLowerCase();


    const cards =
    document.querySelectorAll(".card");


    cards.forEach(function(card) {

        const conteudo =
        card.innerText.toLowerCase();


        if(
            conteudo.includes(texto)
        ) {

            card.style.display =
            "block";

        }

        else {

            card.style.display =
            "none";

        }

    });

}

</script>


</body>
</html>
