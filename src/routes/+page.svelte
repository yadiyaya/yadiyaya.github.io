<script>
    let produtos = [
      { nome: 'Camiseta Preta', preco: 'R$ 50', imagem: 'camiseta_preta.jpg' },
      { nome: 'Jaqueta Azul', preco: 'R$ 120', imagem: 'jaqueta_azul.jpg' },
      { nome: 'Tênis Verde Neon', preco: 'R$ 200', imagem: 'tenis_verde.jpg' },
      { nome: 'Boné Estiloso', preco: 'R$ 80', imagem: 'bone.jpg' },
      { nome: 'Calça Jeans', preco: 'R$ 150', imagem: 'calca_jeans.jpg' },
      { nome: 'Blusa Cinza', preco: 'R$ 90', imagem: 'blusa_cinza.jpg' },
      { nome: 'Óculos de Sol', preco: 'R$ 250', imagem: 'oculos_sol.jpg' },
      { nome: 'Mochila Urbana', preco: 'R$ 180', imagem: 'mochila.jpg' },
      { nome: 'Relógio Moderno', preco: 'R$ 300', imagem: 'relogio.jpg' },
      { nome: 'Carteira de Couro', preco: 'R$ 110', imagem: 'carteira.jpg' }
    ];
  </script>
  
  <style>
    body {
      background-color: black;
      color: white;
      font-family: Arial, sans-serif;
    }
    .container {
      text-align: center;
      padding: 20px;
    }
    .produtos {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 20px;
      padding: 20px;
    }
    .produto {
      background-color: #001f3f;
      padding: 15px;
      border-radius: 10px;
    }
    .produto img {
      width: 100px;
      height: 100px;
      border-radius: 5px;
    }
    .produto h3 {
      color: #39ff14;
    }
    .links {
      margin-top: 20px;
    }
    .links a {
      color: #39ff14;
      text-decoration: none;
      font-size: 18px;
      margin: 10px;
    }
  </style>
  
  <div class="container">
    <h1>Loja de Roupas</h1>
    <div class="produtos">
      {#each produtos as produto}
        <div class="produto">
          <img src={produto.imagem} alt={produto.nome}>
          <h3>{produto.nome}</h3>
          <p>{produto.preco}</p>
        </div>
      {/each}
    </div>
    <div class="links">
      <a href="/carrinho">Carrinho de Compras</a>
      <a href="/informacoes">Informações da Loja</a>
    </div>
  </div>
  