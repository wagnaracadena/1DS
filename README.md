<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DocsFácil</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background: #f5f8fc;
            color: #14213d;
        }

        /* TOPO */
        header {
            height: 105px;
            background: white;
            display: flex;
            align-items: center;
            padding: 0 50px;
            gap: 35px;
            border-bottom: 1px solid #e5eaf2;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-right: 70px;
        }

        .logo-icon {
            width: 43px;
            height: 48px;
            background: #1670e8;
            border-radius: 5px;
            position: relative;
        }

        .logo-icon::after {
            content: "☰";
            color: white;
            position: absolute;
            font-size: 22px;
            left: 10px;
            top: 10px;
        }

        .logo h1 {
            font-size: 30px;
            color: #13213c;
        }

        .logo h1 span {
            color: #1670e8;
        }

        .logo small {
            display: block;
            font-size: 10px;
            color: #555;
        }

        nav {
            display: flex;
            gap: 35px;
            height: 100%;
            align-items: center;
        }

        nav a {
            text-decoration: none;
            color: #111827;
            font-size: 16px;
        }

        nav a:first-child {
            color: #0869e8;
            border-bottom: 3px solid #0869e8;
            height: 100%;
            display: flex;
            align-items: center;
        }

        .search {
            margin-left: auto;
            width: 325px;
            height: 48px;
            border: 1px solid #d5dce7;
            border-radius: 12px;
            display: flex;
            align-items: center;
            padding: 0 20px;
            color: #8b95a7;
        }

        .search span {
            margin-left: auto;
            font-size: 20px;
        }

        .user {
            width: 43px;
            height: 43px;
            border-radius: 50%;
            background: #1874e8;
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 22px;
        }

        /* ÁREA PRINCIPAL */
        main {
            padding: 40px;
        }

        .hero {
            min-height: 470px;
            border-radius: 15px;
            background: linear-gradient(120deg, #eef6ff, #dcecff);
            display: flex;
            align-items: center;
            padding: 60px;
            overflow: hidden;
        }

        .hero-text {
            width: 48%;
        }

        .hero-text h2 {
            font-size: 40px;
            line-height: 1.25;
            margin-bottom: 25px;
        }

        .hero-text h2 span {
            color: #1472e8;
        }

        .hero-text p {
            font-size: 20px;
            line-height: 1.6;
            color: #59677d;
            margin-bottom: 35px;
        }

        button {
            border: none;
            padding: 17px 27px;
            border-radius: 10px;
            font-size: 16px;
            cursor: pointer;
        }

        .upload {
            background: #1670e8;
            color: white;
            margin-right: 20px;
        }

        .folder {
            background: white;
            color: #1670e8;
            border: 1px solid #1670e8;
        }

        /* ILUSTRAÇÃO */
        .illustration {
            width: 52%;
            height: 350px;
            position: relative;
        }

        .screen {
            width: 510px;
            height: 310px;
            background: white;
            border: 10px solid #1765c9;
            border-radius: 12px;
            position: absolute;
            right: 20px;
            top: 20px;
            box-shadow: 0 15px 30px #a9c7ec;
        }

        .screen-content {
            padding: 30px;
        }

        .line {
            height: 12px;
            background: #e5eaf2;
            border-radius: 5px;
            margin-bottom: 20px;
            width: 70%;
        }

        .line.short {
            width: 40%;
        }

        .folder-icon {
            position: absolute;
            bottom: 0;
            left: 80px;
            width: 180px;
            height: 120px;
            background: #086ee5;
            border-radius: 10px;
        }

        .file {
            position: absolute;
            width: 105px;
            height: 125px;
            background: white;
            border-radius: 8px;
            bottom: 35px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 22px;
            box-shadow: 0 5px 20px #b8c9df;
        }

        .pdf {
            right: 220px;
            color: #e53935;
        }

        .word {
            right: 100px;
            color: #1670e8;
        }

        .excel {
            right: -20px;
            color: #159447;
        }

        /* DOCUMENTOS */
        .documents {
            background: white;
            margin-top: 25px;
            padding: 30px;
            border-radius: 15px;
            display: grid;
            grid-template-columns: 250px 1fr 330px;
            gap: 35px;
        }

        .categories h3,
        .recent h3,
        .security h3 {
            margin-bottom: 25px;
        }

        .category {
            padding: 14px;
            margin-bottom: 8px;
            border-radius: 10px;
        }

        .category.active {
            background: #eaf3ff;
            color: #086ee5;
        }

        .document {
            display: flex;
            align-items: center;
            padding: 17px 0;
            border-bottom: 1px solid #edf0f5;
        }

        .document-icon {
            width: 40px;
            font-size: 25px;
            margin-right: 18px;
        }

        .document strong {
            display: block;
            margin-bottom: 5px;
        }

        .document small {
            color: #788397;
        }

        .size {
            margin-left: auto;
            color: #667085;
        }

        /* SEGURANÇA */
        .security-box {
            background: #f5f9ff;
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 20px;
        }

        .security-box h4 {
            margin-bottom: 10px;
        }

        .storage {
            margin-top: 20px;
        }

        .bar {
            height: 9px;
            background: #e4eaf2;
            border-radius: 10px;
            margin-top: 15px;
        }

        .bar div {
            width: 48%;
            height: 100%;
            background: #1670e8;
            border-radius: 10px;
        }

        @media (max-width: 900px) {
            nav {
                display: none;
            }

            .hero {
                padding: 30px;
            }

            .hero-text {
                width: 100%;
            }

            .illustration {
                display: none;
            }

            .documents {
                grid-template-columns: 1fr;
            }

            .search {
                display: none;
            }
        }
    </style>
</head>

<body>

<header>

    <div class="logo">
        <div class="logo-icon"></div>

        <div>
            <h1>Docs<span>Fácil</span></h1>
            <small>Seja bem-vindo ao site de Documentos, sempre com você.</small>
        </div>
    </div>

    <nav>
        <a href="#">Início</a>
        <a href="#">Meus Documentos</a>
        <a href="#">Compartilhados</a>
        <a href="#">Favoritos</a>
        <a href="#">Lixeira</a>
    </nav>

    <div class="search">
        Buscar documentos...
        <span>⌕</span>
    </div>

    <div class="user">👤</div>

</header>


<main>

    <section class="hero">

        <div class="hero-text">

            <h2>
                Organize, armazene<br>
                e compartilhe documentos
                <span>de forma simples e segura.</span>
            </h2>

            <p>
                Acesse seus arquivos de qualquer lugar
                e a qualquer momento.
            </p>

            <button class="upload">
                ☁ Enviar documento
            </button>

            <button class="folder">
                📁 Criar pasta
            </button>

        </div>


        <div class="illustration">

            <div class="screen">
                <div class="screen-content">
                    <div class="line short"></div>
                    <div class="line"></div>
                    <div class="line"></div>
                    <div class="line short"></div>
                    <div class="line"></div>
                </div>
            </div>

            <div class="folder-icon"></div>

            <div class="file pdf">PDF</div>
            <div class="file word">W</div>
            <div class="file excel">X</div>

        </div>

    </section>


    <section class="documents">

        <div class="categories">

            <h3>📁 Categorias</h3>

            <div class="category active">
                📄 Todos os documentos
            </div>

            <div class="category">
                ◷ Recentes
            </div>

            <div class="category">
                👥 Compartilhados comigo
            </div>

            <div class="category">
                ☆ Favoritos
            </div>

            <div class="category">
                🗑 Lixeira
            </div>

        </div>


        <div class="recent">

            <h3>◷ Documentos recentes</h3>

            <div class="document">
                <div class="document-icon">🟦</div>
                <div>
                    <strong>Relatório de atividades.docx</strong>
                    <small>Editado hoje às 10:30</small>
                </div>
                <div class="size">2.4 MB</div>
            </div>

            <div class="document">
                <div class="document-icon">📕</div>
                <div>
                    <strong>Contrato_Serviços.pdf</strong>
                    <small>Editado ontem às 15:45</small>
                </div>
                <div class="size">1.1 MB</div>
            </div>

            <div class="document">
                <div class="document-icon">🟩</div>
                <div>
                    <strong>Planilha Financeira.xlsx</strong>
                    <small>Editado em 22/05/2024</small>
                </div>
                <div class="size">842 KB</div>
            </div>

            <div class="document">
                <div class="document-icon">📁</div>
                <div>
                    <strong>Apresentações</strong>
                    <small>Última alteração em 20/05/2024</small>
                </div>
            </div>

        </div>


        <div class="security">

            <div class="security-box">

                <h3>🔒 Seus documentos estão seguros</h3>

                <p>
                    Usamos criptografia avançada
                    para proteger seus arquivos.
                </p>

            </div>


            <div class="security-box storage">

                <h3>Armazenamento</h3>

                <p>7.2 GB usados de 15 GB</p>

                <div class="bar">
                    <div></div>
                </div>

                <br>

                <a href="#">Fazer upgrade →</a>

            </div>

        </div>

    </section>

</main>

</body>
</html>
