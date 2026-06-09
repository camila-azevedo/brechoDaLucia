<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brechó da Lúcia | Moda com Propósito</title>
    <!-- Fonte Google para um visual clean e moderno -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <!-- Ícones do FontAwesome para o Carrinho e Usuário -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* Cores Base e Reset Minimalista */
        :root {
            --verde-escuro: #2D4A3E; /* Tom principal sustentável */
            --verde-claro: #A3B899;
            --verde-suave: #E8EFE9;
            --texto-escuro: #2B2B2B;
            --branco: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }

        body {
            background-color: var(--branco);
            color: var(--texto-escuro);
        }

        /* Barra de Alerta Sustentável */
        .top-bar {
            background-color: var(--verde-escuro);
            color: var(--branco);
            text-align: center;
            padding: 8px;
            font-size: 0.85rem;
            letter-spacing: 1px;
        }

        /* Cabeçalho (Header) */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 5%;
            border-bottom: 1px solid var(--verde-suave);
            position: sticky;
            top: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(5px);
            z-index: 1000;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--verde-escuro);
            text-decoration: none;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        .nav-menu a {
            text-decoration: none;
            color: var(--texto-escuro);
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        .nav-menu a:hover {
            color: var(--verde-escuro);
        }

        .header-actions {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .action-btn {
            background: none;
            border: none;
            color: var(--texto-escuro);
            font-size: 1.2rem;
            cursor: pointer;
            position: relative;
            text-decoration: none;
            transition: color 0.3s;
        }

        .action-btn:hover {
            color: var(--verde-escuro);
        }

        /* Banner Principal com a Lúcia (Avatar) */
        .hero-section {
            background-color: var(--verde-suave);
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 60px 10%;
            min-height: 450px;
        }

        .hero-text {
            max-width: 50%;
        }

        .hero-text h1 {
            font-size: 2.8rem;
            color: var(--verde-escuro);
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero-text p {
            font-size: 1.1rem;
            margin-bottom: 30px;
            color: #555;
            line-height: 1.6;
        }

        .cta-btn {
            background-color: var(--verde-escuro);
            color: var(--branco);
            padding: 12px 30px;
            text-decoration: none;
            font-weight: 600;
            border-radius: 4px;
            transition: background 0.3s;
        }

        .cta-btn:hover {
            background-color: #1e332a;
        }

        /* Container do Avatar da Lúcia (SVG customizado em CSS) */
        .avatar-container {
            position: relative;
            width: 320px;
            height: 320px;
            background: var(--branco);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: flex-end;
            overflow: hidden;
            border: 4px solid var(--verde-claro);
        }

        /* Seção de Produtos (Catálogo) */
        .catalog-container {
            padding: 60px 5%;
        }

        .section-title {
            font-size: 1.8rem;
            color: var(--verde-escuro);
            margin-bottom: 40px;
            text-align: center;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .product-card {
            background: var(--branco);
            border: 1px solid var(--verde-suave);
            border-radius: 4px;
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
        }

        .product-image {
            width: 100%;
            height: 300px;
            background-color: #f9f9f9;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--verde-claro);
            font-size: 3rem;
        }

        .eco-tag {
            position: absolute;
            top: 15px;
            left: 15px;
            background-color: rgba(45, 74, 62, 0.9);
            color: var(--branco);
            padding: 4px 10px;
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            border-radius: 2px;
        }

        .product-info {
            padding: 20px;
        }

        .product-title {
            font-size: 1rem;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .product-meta {
            font-size: 0.85rem;
            color: #777;
            margin-bottom: 10px;
        }

        .product-price {
            font-size: 1.1rem;
            color: var(--verde-escuro);
            font-weight: 600;
        }

        /* Rodapé */
        footer {
            background-color: var(--verde-escuro);
            color: var(--branco);
            padding: 4px 5%;
            text-align: center;
            padding: 30px;
            font-size: 0.9rem;
            margin-top: 60px;
        }

        /* Responsividade */
        @media (max-width: 768px) {
            .hero-section {
                flex-direction: column-reverse;
                text-align: center;
                gap: 40px;
            }
            .hero-text {
                max-width: 100%;
            }
            .nav-menu {
                display: none; /* Em um sistema real, aqui entraria um menu sanduíche */
            }
        }
    </style>
</head>
<body>

    <!-- Barra de aviso sustentável -->
    <div class="top-bar">
        🌱 CADA PEÇA REUTILIZADA ECONOMIZA ATÉ 2.500 LITROS DE ÁGUA. COMPRE CONSCIENTE!
    </div>

    <!-- Cabeçalho -->
    <header>
        <a href="#" class="logo">brechó da lúcia.</a>
        
        <nav>
            <ul class="nav-menu">
                <li><a href="#">Novidades</a></li>
                <li><a href="#">Roupas</a></li>
                <li><a href="#">Acessórios</a></li>
                <li><a href="#">Pegada Ecológica</a></li>
            </ul>
        </nav>

        <div class="header-actions">
            <!-- Botão Entrar / Criar Conta -->
            <a href="#" class="action-btn" title="Entrar / Criar Conta">
                <i class="fa-regular fa-user"></i>
                <span style="font-size: 0.85rem; margin-left: 5px; font-weight: 300;">Entrar</span>
            </a>
            <!-- Botão Carrinho -->
            <button class="action-btn" title="Carrinho de Compras">
                <i class="fa-solid fa-bag-shopping"></i>
            </button>
        </div>
    </header>

    <!-- Seção de Destaque com o Avatar da Lúcia -->
    <section class="hero-section">
        <div class="hero-text">
            <h1>Moda circular com a curadoria da Lúcia.</h1>
            <p>Olá! Eu sou a Lúcia. Garimpei pessoalmente cada peça deste portal focado em minimalismo e consumo consciente. Estilo atemporal que respeita o planeta.</p>
            <a href="#catalogo" class="cta-btn">Explorar Garimpos</a>
        </div>

        <!-- Avatar Vetorial (SVG) Integrado da Lúcia (Mulher Negra, Estilo Minimalista) -->
        <div class="avatar-container">
            <svg width="280" height="280" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
                <!-- Círculo de Fundo -->
                <circle cx="100" cy="110" r="85" fill="#A3B899" opacity="0.3"/>
                <!-- Cabelo Afro Traseiro -->
                <circle cx="100" cy="85" r="50" fill="#1A1A1A"/>
                <circle cx="65" cy="80" r="30" fill="#1A1A1A"/>
                <circle cx="135" cy="80" r="30" fill="#1A1A1A"/>
                <!-- Pescoço -->
                <rect x="88" y="120" width="24" height="30" fill="#6B4423"/>
                <!-- Rosto (Pele Negra / Tom Quente) -->
                <circle cx="100" cy="95" r="42" fill="#7A4F2D"/>
                <!-- Olhos Minimalistas (Fechados/Sorrindo) -->
                <path d="M 78 95 Q 85 100 90 95" stroke="#1A1A1A" stroke-width="2.5" fill="none"/>
                <path d="M 110 95 Q 115 100 122 95" stroke="#1A1A1A" stroke-width="2.5" fill="none"/>
                <!-- Sorriso -->
                <path d="M 88 115 Q 100 125 112 115" stroke="#1A1A1A" stroke-width="2.5" fill="none"/>
                <!-- Óculos Minimalistas Redondos (Estilo Intelectual/Cult) -->
                <circle cx="83" cy="95" r="14" stroke="#2D4A3E" stroke-width="3" fill="none"/>
                <circle cx="117" cy="95" r="14" stroke="#2D4A3E" stroke-width="3" fill="none"/>
                <line x1="97" y1="95" x2="103" y2="95" stroke="#2D4A3E" stroke-width="3"/>
                <!-- Roupa (Blusa Gola Alta Verde Escuro Minimalista) -->
                <path d="M 50 160 Q 100 140 150 160 L 160 200 L 40 200 Z" fill="#2D4A3E"/>
                <rect x="82" y="140" width="36" height="15" fill="#2D4A3E" rx="3"/>
                <!-- Detalhe do Brinco de Argola Dourado -->
                <circle cx="56" cy="105" r="8" stroke="#D4AF37" stroke-width="2.5" fill="none"/>
                <circle cx="144" cy="105" r="8" stroke="#D4AF37" stroke-width="2.5" fill="none"/>
            </svg>
        </div>
    </section>

    <!-- Seção de Produtos / Catálogo -->
    <main class="catalog-container" id="catalogo">
        <h2 class="section-title">Garimpos Disponíveis</h2>
        
        <div class="products-grid">
            <!-- Produto 1 -->
            <div class="product-card">
                <span class="eco-tag">Economizou 2000L de água</span>
                <div class="product-image">
                    <i class="fa-solid fa-shirt"></i>
                </div>
                <div class="product-info">
                    <div class="product-meta">Tamanho M • Excelente Estado</div>
                    <h3 class="product-title">Blazer de Linho Off-White</h3>
                    <div class="product-price">R$ 89,00</div>
                </div>
            </div>

            <!-- Produto 2 -->
            <div class="product-card">
                <span class="eco-tag">100% Algodão Orgânico</span>
                <div class="product-image">
                    <i class="fa-solid fa-person-dress"></i>
                </div>
                <div class="product-info">
                    <div class="product-meta">Tamanho P • Nunca Usado</div>
                    <h3 class="product-title">Vestido Midi Oliva</h3>
                    <div class="product-price">R$ 120,00</div>
                </div>
            </div>

            <!-- Produto 3 -->
            <div class="product-card">
                <span class="eco-tag">Upcycling</span>
                <div class="product-image">
                    <i class="fa-solid fa-socks"></i>
                </div>
                <div class="product-info">
                    <div class="product-meta">Tamanho Único • Renovado</div>
                    <h3 class="product-title">Bolsa de Sarja Vintage</h3>
                    <div class="product-price">R$ 65,00</div>
                </div>
            </div>
        </div>
    </main>

    <!-- Rodapé -->
    <footer>
        <p>&copy; 2026 Brechó da Lúcia. Feito com amor, respeito ao meio ambiente e consciência circular. 🌍</p>
    </footer>

</body>
</html>
