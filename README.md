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

