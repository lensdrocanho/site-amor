<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Para Minha Princesa 💖</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Arial', sans-serif;
      background: #fff0f6;
      text-align: center;
      overflow-x: hidden;
    }

    h1 {
      color: #d63384;
      margin-bottom: 30px;
    }

    button {
      background: #ff69b4;
      color: white;
      font-size: 1.2em;
      border: none;
      border-radius: 15px;
      padding: 15px 25px;
      cursor: pointer;
      position: relative;
      z-index: 2;
    }

    .page1 {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      position: relative;
      padding: 20px;
    }

    .hearts {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      justify-content: center;
      z-index: 1;
      width: 100%;
    }

    .heart {
      color: #ff6b81;
      font-size: 1.5em;
      animation: float 2s infinite ease-in-out;
      position: absolute;
    }

    @keyframes float {
      0% { transform: translateY(0); opacity: 1; }
      50% { transform: translateY(-10px); opacity: 0.5; }
      100% { transform: translateY(0); opacity: 1; }
    }

    .page2 {
      display: none;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      background: #ff69b4;
      min-height: 100vh;
      width: 100vw;
      padding: 40px 20px;
      position: relative;
      overflow: hidden;
    }

    .heart-bg {
      position: absolute;
      font-size: 1.5em;
      color: #fff0f6;
      animation: flutuar 6s infinite ease-in-out;
      z-index: 0;
      opacity: 0.5;
    }

    @keyframes flutuar {
      0% { transform: translateY(100vh) rotate(0deg); }
      100% { transform: translateY(-10vh) rotate(360deg); }
    }

    .foto {
      max-width: 40%;
      height: auto;
      margin: 20px 0;
      border-radius: 10px;
      z-index: 2;
    }

    .texto {
      max-width: 90%;
      color: #fff;
      font-size: 1.2em;
      margin-bottom: 30px;
      z-index: 2;
    }
  </style>
</head>
<body>
  <div class="page1">
    <h1>Feliz Dia dos Namorados! 💕</h1>
    <div class="hearts">
      <div class="heart">💖</div>
      <div class="heart">💗</div>
      <div class="heart">💓</div>
      <div class="heart">💘</div>
      <div class="heart">❤️</div>
      <div class="heart">💕</div>
    </div>
    <button onclick="mostrarFotos()">Clique aqui minha princesa 💘</button>
  </div>

  <div class="page2">
    <script>
      for (let i = 0; i < 40; i++) {
        const heart = document.createElement('div');
        heart.classList.add('heart-bg');
        heart.innerText = ['💖','💗','💓','💘','💕','❤️'][Math.floor(Math.random()*6)];
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.top = Math.random() * 100 + 'vh';
        heart.style.fontSize = (Math.random() * 1.5 + 1) + 'em';
        heart.style.animationDuration = (Math.random() * 4 + 4) + 's';
        document.querySelector('.page2').appendChild(heart);
      }
    </script>

    <img class="foto" src="ela.JPEG" alt="Foto 1"> 
    <div class="texto">Eu te amo mais que palavras conseguem explicar. Você é o meu mundo e minha razão de sorrir todo dia.</div>

    <img class="foto" src="distancia.JPEG" alt="Foto 2">
    <div class="texto">Mesmo longe, nosso amor é forte. Vamos superar a distância, porque o que temos é verdadeiro.</div>

    <img class="foto" src="linda.JPEG" alt="Foto 3">
    <div class="texto">Você é perfeita, cada detalhe seu me encanta. É minha prioridade, meu tudo, minha princesa.</div>

    <img class="foto" src="crianca.JPEG" alt="Foto 4">
    <div class="texto">Obrigado por trazer à tona o meu eu criança. Você me faz voltar a sorrir de um jeito puro e verdadeiro. ❤️</div>
  </div>

  <script>
    function mostrarFotos() {
      document.querySelector('.page1').style.display = 'none';
      document.querySelector('.page2').style.display = 'flex';
    }
  </script>
</body>
</html>
