<script>
    let produtos = [
      { id: 1, nome: 'Vestido Branco com Babados', preco: 50, imagem: 'vestidobranco.jpg', selecionado: false },
      { id: 2, nome: 'Calça Jeans com Estrelas', preco: 120, imagem: 'calcaestrela.jpg', selecionado: false },
      { id: 3, nome: 'Saída de Praia Preta', preco: 200, imagem: 'saidadepraia.jpg', selecionado: false },
      { id: 4, nome: 'Blusa Rosa com Babados', preco: 80, imagem: 'blusarosa.jpg', selecionado: false },
      { id: 5, nome: 'Bolsa Preta', preco: 150, imagem: 'bolsapreta.jpg', selecionado: false },
      { id: 6, nome: 'Brincos de Estrela', preco: 90, imagem: 'brincos.jpg', selecionado: false },
      { id: 7, nome: 'Kit de Aneis Vintage', preco: 250, imagem: 'kitaneis.jpg', selecionado: false },
      { id: 8, nome: 'Blusa com Estampa Alto Relevo de Estrela Rosa', preco: 180, imagem: 'blusaestrelarosa.jpg', selecionado: false },
      { id: 9, nome: 'Tênis Moderno', preco: 300, imagem: 'teninho.jpg', selecionado: false },
      { id: 10, nome: 'Cinto de Couro', preco: 110, imagem: 'cinto.jpg', selecionado: false }
    ];
  
    function calcularTotais() {
      const itensSelecionados = produtos.filter(produto => produto.selecionado);
      return {
        totalItens: itensSelecionados.length,
        totalValor: itensSelecionados.reduce((total, produto) => total + produto.preco, 0)
      };
    }
  
    function finalizarCompra() {
      const itensSelecionados = produtos.filter(produto => produto.selecionado);
      if (itensSelecionados.length === 0) {
        alert('Nenhum item selecionado!');
        return;
      }
      const resumoCompra = itensSelecionados.map(produto => `${produto.nome} - R$${produto.preco}`).join('\n');
      alert(`Resumo da Compra:\n${resumoCompra}\nTotal: R$${calcularTotais().totalValor}`);
    }
  </script>
  
  <style>
    :global(body) {
      background-color: #121212;
      color: #f1f1f1;
      font-family: 'Arial', sans-serif;
      margin: 0;
      padding: 0;
    }
  
    .container {
      padding: 20px;
      max-width: 900px;
      margin: 0 auto;
    }
  
    .titulo-carrinho {
      color: #9b4dca;
      font-size: 2.5rem;
      margin-bottom: 20px;
      text-align: left;
    }
  
    .produtos {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 20px;
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
      margin-bottom: 10px;
    }
  
    .produto p {
      font-size: 1.2rem;
      color: #bbb;
    }
  
    .produto input {
      margin-top: 10px;
    }
  
    .totais {
      margin-top: 20px;
      font-size: 1.5rem;
    }
  
    .totais h4 {
      color: #f1f1f1;
      margin: 5px 0;
    }
  
    .botao-finalizar {
      background-color: #9b4dca;
      color: white;
      border: none;
      padding: 12px 20px;
      border-radius: 8px;
      cursor: pointer;
      font-size: 1.2rem;
      margin-top: 20px;
      transition: background 0.3s;
    }
  
    .botao-finalizar:hover {
      background-color: #6d2a8b;
    }
  </style>
  
  <div class="container">
    <h1 class="titulo-carrinho">Carrinho de Compras</h1>
    <div class="produtos">
      {#each produtos as produto (produto.id)}
        <div class="produto">
          <img src={produto.imagem} alt={produto.nome} />
          <h3>{produto.nome}</h3>
          <p>R$ {produto.preco}</p>
          <input type="checkbox" bind:checked={produto.selecionado} />
        </div>
      {/each}
    </div>
  
    <div class="totais">
      <h4>Total de Itens: {calcularTotais().totalItens}</h4>
      <h4>Valor Total: R$ {calcularTotais().totalValor}</h4>
    </div>
  
    <button class="botao-finalizar" on:click={finalizarCompra}>Finalizar Compra</button>
  </div>
  a