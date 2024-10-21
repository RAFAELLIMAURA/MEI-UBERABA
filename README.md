<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Auxílio MEI e Calculadora de Receita</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: rgb(0, 255, 68);
            color: rgb(38, 0, 255);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            flex-direction: column;
        }

        /* Contêiner para os dois blocos */
        .main-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            width: 90%;
            max-width: 1200px; /* Limita a largura máxima da página */
            margin: 20px auto;
        }

        .container {
            background-color: rgb(247, 228, 20);
            padding: 20px;
            border-radius: 20px;
            width: 45%; /* Ajusta para caber dois blocos lado a lado */
            box-sizing: border-box;
            margin: 10px;
        }

        /* Estilos dos botões */
        .button-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
        }

        .button {
            text-decoration: none;
            font-weight: bold;
            color: white;
            background-color: rgb(13, 0, 255);
            padding: 8px 10px;
            border-radius: 8px;
            cursor: pointer;
            width: 48%;
            text-align: center;
            font-size: 14px;
            box-sizing: border-box;
        }

        .button:hover {
            background-color: rgb(0, 139, 2);
            color: rgb(26, 255, 0);
        }

        /* Estilos para o bloco da calculadora de receita */
        .calculadora-container {
            background-color: white;
            padding: 20px;
            border-radius: 20px;
            width: 45%;
            box-sizing: border-box;
            margin: 10px;
            color: black;
        }

        input {
            padding: 10px;
            margin: 5px 0;
            width: 80%;
            max-width: 300px;
        }

        button {
            padding: 10px;
            margin: 5px 0;
            width: 50%;
            background-color: yellow;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background-color: #f0c040;
        }

        /* Ajustes para dispositivos menores */
        @media (max-width: 768px) {
            .container, .calculadora-container {
                width: 100%;
            }

            .button {
                width: 45%;
            }
        }
    </style>
</head>

<body>
    <div class="main-container">
        <!-- Bloco do Auxílio MEI -->
        <div class="container">
            <h2>Auxílio ao Microempreendedor Individual</h2>
            <div class="button-container">
                <a href="https://www.gov.br/empresas-e-negocios/pt-br/empreendedor/quero-ser-mei" class="button">Abertura do MEI</a>
                <a href="https://www.gov.br/empresas-e-negocios/pt-br/empreendedor/servicos-para-mei/baixa-de-mei" class="button">Baixa do MEI</a>
                <a href="https://www.gov.br/empresas-e-negocios/pt-br/empreendedor/servicos-para-mei/atualizacao-cadastral-de-mei" class="button">Alteração do MEI</a>
                <a href="http://www8.receita.fazenda.gov.br/SimplesNacional/Aplicacoes/ATSPO/pgmei.app/Identificacao" class="button">Emissão do DAS</a>
                <a href="http://www8.receita.fazenda.gov.br/SimplesNacional/Aplicacoes/ATSPO/dasnsimei.app/Identificacao" class="button">Declaração do Imposto MEI</a>
                <a href="http://www8.receita.fazenda.gov.br/SimplesNacional/Servicos/Grupo.aspx?grp=19" class="button">Negociação MEI</a>
            </div>

            <h2>Serviço de Consultoria</h2>
            <div class="button-container">
                <a href="https://wa.me/5534988507154?text=Ol%C3%A1+preciso+de+auxilio+com+minha+empresa" class="button">Preciso de ajuda profissional</a>
            </div>

            <h2>Regularização Município de Uberaba</h2>
            <div class="button-container">
                <a href="http://www.uberaba.mg.gov.br/consultaPrevia/pages/page-login.xhtml?uri=/pages/page-main.xhtml" class="button">Consulta Prévia Uberaba</a>
                <a href="https://app.codiub.com.br/alvaras/pages/page-login.xhtml" class="button">Emissão do Alvará Uberaba</a>
                <a href="http://www.uberaba.mg.gov.br/portal/conteudo,43298" class="button">Consulta Declaração de Número</a>
            </div>

            <h2>Certidões Negativas</h2>
            <div class="button-container">
                <a href="https://iptu.uberaba.mg.gov.br/tributos/cnd/cnd.php" class="button">Certidão Negativa Uberaba</a>
                <a href="https://solucoes.receita.fazenda.gov.br/servicos/certidaointernet/pj/emitir" class="button">Certidão Negativa Federal</a>
                <a href="https://www2.fazenda.mg.gov.br/sol/ctrl/SOL/CDT/SERVICO_829?ACAO=INICIAR" class="button">Certidão Negativa Estadual-MG</a>
                <a href="https://consulta-crf.caixa.gov.br/consultacrf/pages/consultaEmpregador.jsf" class="button">Consulta Regularidade Empregador</a>
            </div>

            <h2>Emissor de Nota Fiscal MEI</h2>
            <div class="button-container">
                <a href="https://www.nfse.gov.br/EmissorNacional/Login?ReturnUrl=%2fEmissorNacional" class="button">Emissor de Nota Fiscal de Serviço MEI</a>
            </div>
        </div>

        <!-- Bloco da Calculadora de Receita -->
        <div class="calculadora-container">
            <h1>Receita MEI</h1>

            <label for="data">Data (DD/MM/AAAA):</label><br>
            <input type="date" id="data" /><br>

            <label for="receitaDiaria">Digite a Receita Diária (R$):</label><br>
            <input type="number" id="receitaDiaria" placeholder="Ex: 100" /><br>

            <div class="button-row">
                <button onclick="calcularReceita()">Somar Receita Diária</button>
                <button onclick="gerarRelatorio('mensal')">Gerar Relatório Mensal</button>
                <button onclick="gerarRelatorio('anual')">Gerar Relatório Anual</button>
                <button onclick="limparDados()">Limpar Dados</button>
            </div>

            <h2>Resultados do Dia:</h2>
            <p><strong>Receita Diária: R$</strong> <span id="receitaDiariaResultado">0</span></p>

            <h2>Total Acumulado:</h2>
            <p><strong>Total Acumulado Diário: R$</strong> <span id="totalDiarioAcumulado">0</span></p>
            <p><strong>Total Acumulado Mensal: R$</strong> <span id="totalMensalAcumulado">0</span></p>
            <p><strong>Total Acumulado Anual: R$</strong> <span id="totalAnualAcumulado">0</span></p>

            <div id="relatorio">
                <h2>Relatório de Receitas</h2>
                <p id="relatorioConteudo"></p>
            </div>
        </div>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <script>
        // Funções da calculadora (já implementadas anteriormente)
    </script>
</body>
</html>
