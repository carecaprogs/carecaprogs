<h1 align="left">Hey 👋 What's up?</h1>

###

<p align="left">Olá! Meu nome é Daniel Monteiro.</p>

###

<h2 align="left">About me</h2>

###

<p align="left">🔹 Linguagens principais: PHP, JavaScript, NodeJS e SQL<br>🔹 Interesse em back-end, front-end e banco de dados<br>🌟 Sempre buscando criar soluções inteligentes e bem estruturadas</p>

###

<h2 align="left">I code with</h2>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" height="40" alt="nodejs logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" height="40" alt="php logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="40" alt="mysql logo"  />
</div>

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <link rel="icon" href="img/logo.png" type="image/png">
    <meta charset="UTF-8">
    <title>Login</title>
    <style>
        /* Configurações Globais */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        /* Estilos do Body */
        body {
            background-image: url('img/VERITAS.png');
            color: #e0e0e0; /* Cinza claro */
            display: flex;
            justify-content: flex-start; /* Alinha à esquerda */
            align-items: center;
            height: 100vh;
            padding-left: 350px; /* Ajuste a distância da esquerda */
        }

        /* Estilos do Título */
        h2 {
            color: #4caf50; /* Verde */
        }

        /* Estilos dos Inputs e Botões */
        input, button, select {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #333;
            background-color: #333; /* Fundo de inputs preto */
            color: #fff; /* Texto branco */
            position: relative; /* Necessário para o efeito de sublinhado */
            outline: none; /* Remove a borda de foco padrão */
            transition: background-color 0.3s ease; /* Transição para o hover */
        }

        input:focus, select:focus, button:hover {
            background-color: #444; /* Altera a cor de fundo ao focar ou passar o mouse */
        }

        button {
            background-color: #4caf50; /* Cor inicial do botão */
            border: none;
            cursor: pointer;
        }

        button:hover {
            background-color: #388e3c; /* Verde mais escuro ao passar o mouse */
        }

        /* Efeito de sublinhado */
        input::after, button::after, select::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: -5px; /* Posição logo abaixo do elemento */
            width: 0;
            height: 2px;
            background-color: #00ff8c; /* Cor do sublinhado verde neon */
            transition: width 0.3s ease, left 0.3s ease; /* Transição suave */
        }

        input:focus::after, button:hover::after, select:focus::after {
            width: 100%; /* Expande o sublinhado ao focar ou passar o mouse */
            left: 0;
        }


        /* Estilos do Container de Login */
        .login-container {
            background-color: #1e1e1e; /* Fundo mais escuro */
            padding: 100px 20px 20px; /* Mantém o padding ao redor */
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
            width: 300px; /* Largura */
            height: auto; /* Ajuste automático da altura */
            position: relative; /* Necessário para posicionar a imagem */
            overflow: hidden; /* Para ocultar parte da imagem se necessário */
            display: flex; /* Usar flexbox para centralizar o conteúdo */
            flex-direction: column; /* Coluna para os elementos */
            align-items: center; /* Alinhamento central */
        }

        /* Imagem de Fundo do Container */
        .login-container::before {
            content: '';
            background-image: url('img/img_login.png');
            background-size: cover; /* Ajusta a imagem para cobrir a área */
            background-position: center; /* Centraliza a imagem */
            position: absolute; /* Faz com que a imagem fique sobre a caixa */
            top: 0; /* Começa no topo */
            left: 0;
            right: 0;
            height: 180px; /* Altura da imagem */
            z-index: 0; /* Coloca a imagem atrás do conteúdo */
        }

        /* Estilo do Título Dentro do Container */
        .login-container h2 {
            position: relative; /* Para garantir que o título fique acima da imagem */
            z-index: 1; /* Coloca o texto acima da imagem */
            margin-top: 60px; /* Para espaçamento abaixo da imagem */
        }

        /* Estilos do Formulário */
        form {
            width: 100%; /* A largura do formulário ocupa 100% da caixa */
            display: flex;
            flex-direction: column; /* Coluna para os elementos do formulário */
            z-index: 1; /* Garante que o formulário esteja acima da imagem */
        }

        label {
            margin-top: 10px; /* Espaçamento entre o título e os campos */
        }

        /* Estilos dos Links */
        a {
            color: #fff; /* Cor branca */
            text-decoration: none; /* Remove o sublinhado */
        }

        a:hover {
            text-decoration: underline; /* Adiciona sublinhado ao passar o mouse */
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2></h2>
        <form method="POST"> 
            <label>Usuário</label>
            <input type="text" name="usuario" required>
            <label>Senha</label>
            <input type="password" name="senha" required>
            <button type="submit" name="login">Entrar</button>
        </form>
        <a href="recuperar_senha.php">Esqueceu a senha?</a>
    </div>
</body>
</html>

###
