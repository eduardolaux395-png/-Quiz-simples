<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Quiz de pokemon</title>

<style>
  body {
    font-family: Arial;
    background: #f2f2f2;
    display: flex;
    justify-content: center;
    margin-top: 40px;
  }

  .quiz {
    background: #fff;
    padding: 25px;
    border-radius: 15px;
    width: 350px;
  }

  h1 {
    text-align: center;
  }

  #pergunta {
    font-size: 18px;
    margin: 20px 0;
    transition: 0.3s;
  }

  /* Hover no enunciado */
  #pergunta:hover {
    color: blue;
  }

  .opcao {
    border: 2px solid #ccc;
    padding: 12px;
    border-radius: 10px;
    margin: 10px 0;
    cursor: pointer;
    transition: 0.3s;
  }

  /* Azul antes de clicar */
  .opcao:hover {
    border-color: #007bff;
    background: #e7f1ff;
  }

  /* Estados após clique */
  .correta {
    border-color: green;
    background: #d4edda;
  }

  .errada {
    border-color: red;
    background: #f8d7da;
  }

  #resultado {
    margin-top: 15px;
    font-weight: bold;
  }
</style>
</head>

<body>

<div class="quiz">
  <h1>POKE QUIZ</h1>

  <div id="pergunta">Qual pokemon o ash mais usa</div>

  <div class="opcao" data-correta="false">Charizard</div>
  <div class="opcao" data-correta="true">Pikachu</div>
  <div class="opcao" data-correta="false">Bulbassaur</div>
  <div class="opcao" data-correta="false">Mewtwo</div>

  <div id="resultado"></div>
</div>

<script>
  const opcoes = document.querySelectorAll('.opcao');
  const resultado = document.getElementById('resultado');

  opcoes.forEach(opcao => {
    opcao.addEventListener('click', () => {

      // Limpa estados anteriores
      opcoes.forEach(op => {
        op.classList.remove('correta', 'errada');
      });

      const correta = opcao.getAttribute('data-correta') === 'true';

      if (correta) {
        opcao.classList.add('correta');
        resultado.textContent = "✅ Você acertou!";
      } else {
        opcao.classList.add('errada');
        resultado.textContent = "❌ Você errou!";

        // mostra correta
        opcoes.forEach(op => {
          if (op.getAttribute('data-correta') === 'true') {
            op.classList.add('correta');
          }
        });
      }
    });
  });
</script>

</body>
</html>
