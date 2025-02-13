<title>Star Shopping</title>
<style>
  :global(.body) {
    background-color: #121212;
    color: #f1f1f1;
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
  }


  .top-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #2d2d2d;
    padding: 20px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
  }

  .top-bar h1 {
    font-size: 3rem;
    color: #9b4dca;
    margin: 0;
    letter-spacing: 2px;
  }

  .top-bar .links {
    display: flex;
    align-items: center;
  }

  .top-bar .links a {
    color: #9b4dca;
    text-decoration: none;
    font-size: 18px;
    margin: 0 15px;
    display: flex;
    align-items: center;
    transition: color 0.3s ease;
  }

  .top-bar .links a img {
    width: 20px;
    height: 20px;
    margin-left: 8px;
  }

  .top-bar .links a:hover {
    color: #fff;
  }

  
  :global(.container) {
    padding: 20px;
  }

  .produtos {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
    padding: 20px;
    margin-top: 20px;
  }

  .produto {
    background-color: #1a1a1a;
    padding: 15px;
    border-radius: 12px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .produto:hover {
    transform: scale(1.05);
    box-shadow: 0 4px 20px rgba(155, 77, 202, 0.3);
  }

  .produto img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 8px;
    margin-bottom: 15px;
  }

  .produto h3 {
    color: #9b4dca;
    font-size: 1.4rem;
    margin: 0 0 10px 0;
  }

  .produto p {
    font-size: 1.2rem;
    color: #bbb;
  }

  .produto button {
    background-color: #9b4dca;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 8px;
    cursor: pointer;
    transition: background 0.3s;
  }

  .produto button:hover {
    background-color: #6d2a8b;
  }


  footer {
    background-color: #2d2d2d;
    color: #f1f1f1;
    padding: 20px;
    text-align: center;
    margin-top: 30px;
  }

  footer p {
    margin: 0;
    font-size: 1rem;
  }

  footer .links a {
    color: #9b4dca;
    text-decoration: none;
    font-size: 16px;
    margin: 10px 15px;
    transition: color 0.3s ease;
  }

  footer .links a:hover {
    color: #fff;
  }


  @media (max-width: 768px) {
    .top-bar {
      flex-direction: column;
      align-items: center;
    }

    .produtos {
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    }

    .top-bar h1 {
      font-size: 2.5rem;
    }
  }
</style>


<div class="top-bar">
  <h1>𝔖𝔱𝔞𝔯 𝔖𝔥𝔬𝔭𝔭𝔦𝔫𝔤</h1>
  <div class="links">
    <a href="/carrinho">
      Carrinho de Compras
      <img src="iconcarrinho.jpg" alt="Carrinho">
    </a>
    <a href="/informacoes">
      Informações da Loja
      <img src="iconinformacoes.jpg" alt="Informações">
    </a>
  </div>
</div>


<div class="produtos">
  <div class="produto">
    <img src="vestidobranco.jpg" alt="Vestido Branco com Babados">
    <h3>Vestido Branco com Babados</h3>
    <p>R$ 50</p>
    <button on:click={() => adicionarAoCarrinho('Vestido Branco com Babados', 50)}>Adicionar ao Carrinho</button>
  </div>
  
  <div class="produto">
    <img src="calcaestrela.jpg" alt="Calça Jeans com Estrelas">
    <h3>Calça Jeans com Estrelas</h3>
    <p>R$ 120</p>
    <button on:click={() => adicionarAoCarrinho('Calça Jeans com Estrelas', 120)}>Adicionar ao Carrinho</button>
  </div>
  
  <div class="produto">
    <img src="saidadepraia.jpg" alt="Saída de Praia Preta">
    <h3>Saída de Praia Preta</h3>
    <p>R$ 200</p>
    <button on:click={() => adicionarAoCarrinho('Saída de Praia Preta', 200)}>Adicionar ao Carrinho</button>
  </div>
  
  <div class="produto">
    <img src="blusarosa.jpg" alt="Blusa Rosa com Babados">
    <h3>Blusa Rosa com Babados</h3>
    <p>R$ 80</p>
    <button on:click={() => adicionarAoCarrinho('Blusa Rosa com Babados', 80)}>Adicionar ao Carrinho</button>
  </div>
  
  <div class="produto">
    <img src="bolsapreta.jpg" alt="Bolsa Preta">
    <h3>Bolsa Preta</h3>
    <p>R$ 150</p>
    <button on:click={() => adicionarAoCarrinho('Bolsa Preta', 150)}>Adicionar ao Carrinho</button>
  </div>
  
  <div class="produto">
    <img src="kitaneis.jpg" alt="Kit de Anéis Vintage">
    <h3>Kit de Anéis Vintage</h3>
    <p>R$ 250</p>
    <button on:click={() => adicionarAoCarrinho('Kit de Anéis Vintage', 250)}>Adicionar ao Carrinho</button>
  </div>
  
  <div class="produto">
    <img src="blusaestrelarosa.jpg" alt="Blusa com Estampa Alto Relevo de Estrela Rosa">
    <h3>Blusa com Estampa Alto Relevo de Estrela Rosa</h3>
    <p>R$ 180</p>
    <button on:click={() => adicionarAoCarrinho('Blusa com Estampa Alto Relevo de Estrela Rosa', 180)}>Adicionar ao Carrinho</button>
  </div>
  
  <div class="produto">
    <img src="teninho.jpg" alt="Tênis Moderno">
    <h3>Tênis Moderno</h3>
    <p>R$ 300</p>
    <button on:click={() => adicionarAoCarrinho('Tênis Moderno', 300)}>Adicionar ao Carrinho</button>
  </div>
  
  <div class="produto">
    <img src="cinto.jpg" alt="Cinto de Couro">
    <h3>Cinto de Couro</h3>
    <p>R$ 110</p>
    <button on:click={() => adicionarAoCarrinho('Cinto de Couro', 110)}>Adicionar ao Carrinho</button>
  </div>
</div>

<footer>
  <p>&copy; 2025 𝔖𝔱𝔞𝔯 𝔖𝔥𝔬𝔭𝔭𝔦𝔫𝔤. Todos os direitos reservados.</p>
  <div class="links">
    <a href="/sobre">Sobre Nós</a>
    <a href="https://www.instagram.com/yayadi.jpeg?igsh=MWZndHdyM2N2NzNkMQ==" target="_blank">
      <img src="iconinsta.jpg" alt="Instagram" width="20"> Instagram
    </a>
  </div>
</footer>
