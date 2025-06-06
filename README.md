<!DOCTYPE html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Feliz Aniversário, meu amor!</title>
    <link
      href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap"
      rel="stylesheet"
    />
    <style>
      body {
        font-family: "Roboto", sans-serif;
        background-color: #c0392b;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 100vh;
        margin: 0;
        text-align: center;
        overflow: hidden;
      }

      h1 {
        font-size: 2.4em;
        color: #fff;
        margin-bottom: 20px;
      }

      #mensagem {
        display: none;
        font-size: 1.3em;
        color: #fff;
        margin-bottom: 30px;
        max-width: 600px;
        line-height: 1.6;
      }

      .botao {
        padding: 15px 30px;
        font-size: 1.2em;
        background-color: #fff;
        color: #c0392b;
        border: none;
        border-radius: 30px;
        cursor: pointer;
        font-weight: bold;
        transition: background 0.3s, transform 0.2s;
      }

      .botao:hover {
        background-color: #ffe0e0;
        transform: scale(1.05);
      }

      #presentinho {
        display: none;
        margin-top: 30px;
        cursor: pointer;
        width: 100px;
        transition: transform 0.3s;
      }

      #presentinho:hover {
        transform: scale(1.1);
      }

      #macaco {
        display: none;
        width: 120px;
        margin-top: 20px;
      }

      .balao {
        position: absolute;
        width: 30px;
        height: 40px;
        background-color: red;
        border-radius: 50%;
        opacity: 0.7;
        animation: subir 4s linear infinite;
      }

      @keyframes subir {
        0% {
          transform: translateY(0);
          opacity: 1;
        }
        100% {
          transform: translateY(-600px);
          opacity: 0;
        }
      }
    </style>
  </head>
  <body>
    <h1>Feliz Aniversário, meu amor! 🎁</h1>
    <button class="botao" onclick="mostrarMensagem()">Aperte</button>

    <p id="mensagem">
      Parabéns, meu amor! 💖<br /><br />
      Que seu dia seja cheio de sorrisos, carinho e alegria!<br />
      Você é uma pessoa incrível e merece tudo de melhor nesse mundo.<br />
      Eu te amo MUITO! 🐵💕
    </p>

    <img
      id="presentinho"
      src="https://th.bing.com/th/id/R.a87cc347e73a336112526e9d33239ea8?rik=4QiEZDG4DM5xAQ&riu=http%3a%2f%2fwww.pngall.com%2fwp-content%2fuploads%2f2016%2f03%2fGift-High-Quality-PNG.png&ehk=xQ1PzIHpnbaAoTGILBIyBMNPgjJWINMb01NRHq2EKdo%3d&risl=1&pid=ImgRaw&r=0"
      alt="Presente"
      onclick="soltarBaloes()"
    />

    <img
      id="macaco"
      src="https://www.pngarts.com/files/3/Cute-Cartoon-Monkey-Transparent-Images.png"
      alt="Macaco fofo"
    />

    <script>
      function mostrarMensagem() {
        document.getElementById("mensagem").style.display = "block";
        document.getElementById("presentinho").style.display = "block";
      }

      function soltarBaloes() {
        const macaquinho = document.getElementById("macaco");
        macaquinho.style.display = "block";

        for (let i = 0; i < 15; i++) {
          let balao = document.createElement("div");
          balao.classList.add("balao");
          balao.style.left = Math.random() * 90 + "vw";
          balao.style.backgroundColor = `hsl(${Math.random() * 360}, 70%, 70%)`;
          balao.style.animationDuration = Math.random() * 2 + 3 + "s";

          document.body.appendChild(balao);

          setTimeout(() => {
            balao.remove();
          }, 5000);
        }
      }
    </script>
  </body>
</html>
