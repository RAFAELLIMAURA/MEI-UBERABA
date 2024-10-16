<DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Auxilio ao Microempreendedor Individual</title>
    <link rel="stylesheet" type="text/css" href="style.css">
    <script src="script.js"></script>
  </head>
  <style>
    body {
      background-color: rgb(0, 255, 68);
      color: rgb(38, 0, 255);
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      text-align: center;
      flex-direction: column;
    }

    .container {
      background-color: rgb(247, 228, 20);
      padding: 20px;
      border-radius: 20px;
      width: 90%;
      max-width: 400px; /* Limita a largura para caber bem em dispositivos móveis */
      margin: 20px;
    }

    /* Estilos para os botões */
    .button-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center; /* Centraliza os botões */
      gap: 10px; /* Espaçamento entre botões */
    }

    .button {
      text-decoration: none;
      font-weight: bold;
      color: white;
      background-color: rgb(13, 0, 255);
      padding: 8px 10px; /* Reduz o padding para diminuir os botões */
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease-in-out;
      width: 48%; /* Ajusta a largura para caber dois botões lado a lado */
      box-sizing: border-box;
      font-size: 12px; /* Reduz o tamanho da fonte */
    }

    .button:hover {
      background-color: rgb(0, 139, 2);
      color: rgb(26, 255, 0);
    }

    /* Ajustes para telas menores */
    @media (max-width: 768px) {
      .button {
        width: 45%; /* Mantém dois botões lado a lado em telas menores */
      }
    }
  </style>

  <body>
    <div class="container">
      <h1>Auxilio ao Microempreendedor Individual</h1>

      
