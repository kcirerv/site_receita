<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Site de Receitas</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Site de Receitas</h1>
    <nav>
      <a href="#">Início</a>
      <a href="#">Sobre</a>
      <a href="#">Contato</a>
    </nav>
  </header>

  <main>
    <section class="recipes">
      <h2>Receitas Populares</h2>
      <div class="recipe-card">
        <img src="https://via.placeholder.com/300x200" alt="Imagem da Receita 1">
        <h3>Receita 1</h3>
        <p>Uma descrição curta da receita.</p>
        <button onclick="showRecipeDetails(1)">Ver Receita</button>
      </div>

      <div class="recipe-card">
        <img src="https://via.placeholder.com/300x200" alt="Imagem da Receita 2">
        <h3>Receita 2</h3>
        <p>Uma descrição curta da receita.</p>
        <button onclick="showRecipeDetails(2)">Ver Receita</button>
      </div>

      <div class="recipe-card">
        <img src="https://via.placeholder.com/300x200" alt="Imagem da Receita 3">
        <h3>Receita 3</h3>
        <p>Uma descrição curta da receita.</p>
        <button onclick="showRecipeDetails(3)">Ver Receita</button>
      </div>
    </section>
  </main>

  <footer>
    <p>© 2025 Site de Receitas | Todos os direitos reservados</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  color: #333;
  margin: 0;
  padding: 0;
}

header {
  background-color: #f8b400;
  padding: 20px;
  text-align: center;
  color: white;
}

h1 {
  margin: 0;
  font-size: 2em;
}

.receitas {
  padding: 20px;
}

.receita-item {
  background-color: white;
  padding: 15px;
  margin-bottom: 10px;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.adicionar-receita {
  padding: 20px;
  background-color: #fff;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

#form-receita input, #form-receita textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

#form-receita button {
  padding: 10px 15px;
  background-color: #f8b400;
  border: none;
  border-radius: 5px;
  color: white;
  cursor: pointer;
}

#form-receita button:hover {
  background-color: #f79c42;
}

// Lista de receitas
const receitas = [
  { nome: "Bolo de Cenoura", descricao: "Um delicioso bolo de cenoura com cobertura de chocolate." },
  { nome: "Macarrão à Carbonara", descricao: "Macarrão com molho cremoso e bacon crocante." }
];

// Exibe as receitas na tela
function exibirReceitas() {
  const listaReceitas = document.getElementById("receita-list");
  listaReceitas.innerHTML = "";

  receitas.forEach((receita) => {
    const div = document.createElement("div");
    div.classList.add("receita-item");
    div.innerHTML = `<h3>${receita.nome}</h3><p>${receita.descricao}</p>`;
    listaReceitas.appendChild(div);
  });
}

// Adiciona uma nova receita
document.getElementById("form-receita").addEventListener("submit", function(event) {
  event.preventDefault();

  const nome = document.getElementById("nome-receita").value;
  const descricao = document.getElementById("descricao-receita").value;

  if (nome && descricao) {
    receitas.push({ nome, descricao });
    exibirReceitas();

    // Limpa o formulário
    document.getElementById("nome-receita").value = "";
    document.getElementById("descricao-receita").value = "";
  }
});

// Exibe as receitas quando a página carrega
exibirReceitas();
