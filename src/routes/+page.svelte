<script>
    // Aqui podemos definir os dados dos produtos ou carregar de uma API.
    let produtos = [
      { id: 1, nome: 'Produto 1', preco: 'R$ 29,99', imagem: '/assets/images/produto1.jpg' },
      { id: 2, nome: 'Produto 2', preco: 'R$ 49,99', imagem: '/assets/images/produto2.jpg' },
      { id: 3, nome: 'Produto 3', preco: 'R$ 19,99', imagem: '/assets/images/produto3.jpg' }
    ];
  </script>
  
  <style>
    header {
      background-color: #2c3e50;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    
    .produtos {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1rem;
      padding: 2rem;
    }
    
    .produto {
      border: 1px solid #ccc;
      border-radius: 8px;
      overflow: hidden;
      text-align: center;
      padding: 1rem;
      background-color: #fff;
    }
  
    .produto img {
      width: 100%;
      height: auto;
      border-bottom: 1px solid #ccc;
    }
  
    footer {
      background-color: #2c3e50;
      color: white;
      text-align: center;
      padding: 1rem;
      position: fixed;
      width: 100%;
      bottom: 0;
    }
  </style>
  
  <header>
    <h1>Bem-vindo ao Mercado Online</h1>
  </header>
  
  <main>
    <h2>Produtos em Destaque</h2>
    <div class="produtos">
      {#each produtos as produto}
        <div class="produto">
          <img src={produto.imagem} alt={produto.nome} />
          <h3>{produto.nome}</h3>
          <p>{produto.preco}</p>
          <button>Adicionar ao Carrinho</button>
        </div>
      {/each}
    </div>
  </main>
  
  <footer>
    <p>&copy; 2025 Mercado Online | Todos os direitos reservados</p>
  </footer>
  