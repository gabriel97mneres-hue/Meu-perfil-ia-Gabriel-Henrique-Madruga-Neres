<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minerando Dados | Estudante de I.A.</title>
    <meta name="description" content="Portfólio de estudante de Inteligência Artificial com projetos em Python e Machine Learning. Estilo Minecraft Blocky.">
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts - VT323 para Pixel Font, Inter para Corpo -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&family=VT323&display=swap" rel="stylesheet">
    
    <style>
        /* Variáveis de Cores Temáticas */
        :root {
            --color-grass: #4CAF50; /* Verde Grama */
            --color-dirt: #8D6E63;  /* Marrom Terra */
            --color-stone: #607D8B; /* Cinza Pedra */
            --color-redstone: #F44336; /* Vermelho Redstone */
            --color-sky: #03A9F4; /* Azul Céu */
            --color-bg-dark: #212121; /* Fundo Escuro para contraste */
        }

        /* Classes Customizadas para a Estética Minecraft */
        .font-pixel {
            font-family: 'VT323', monospace;
            text-shadow: 2px 2px 0 var(--color-bg-dark); /* Simula a espessura do pixel */
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--color-bg-dark);
            color: white;
            /* Fundo sutil de "pedra/terra" pixelizada */
            background-image: repeating-linear-gradient(45deg, rgba(255,255,255,.05) 0px, rgba(255,255,255,.05) 1px, transparent 1px, transparent 10px), repeating-linear-gradient(135deg, rgba(0,0,0,.1) 0px, rgba(0,0,0,.1) 1px, transparent 1px, transparent 10px);
        }

        .blocky {
            border: 4px solid var(--color-bg-dark);
            box-shadow: 6px 6px 0px 0px rgba(0, 0, 0, 0.7);
            border-radius: 0; /* Remover cantos arredondados do Tailwind */
        }
        
        .blocky-btn {
            @apply font-pixel text-lg sm:text-xl py-3 px-6 transition-all duration-100 ease-in-out;
            border: 4px solid #111827; /* Darker border */
            box-shadow: 4px 4px 0px 0px rgba(0, 0, 0, 0.9);
            transform: translate(0, 0);
        }

        /* Efeito de Clique/Mineração no Botão */
        .blocky-btn:active {
            box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.9);
            transform: translate(4px, 4px);
        }

        /* Customização para a Navbar */
        .navbar-block {
            border-bottom: 4px solid var(--color-redstone);
        }
        
        /* Estilo para Linha do Tempo (Mapa) */
        .timeline-item::before {
            content: '⛏'; /* Picareta como ícone de ponto */
            @apply absolute left-[-2rem] top-1 text-2xl;
        }

        /* Pseudo-elemento para o Avatar de Bloco (simulação) */
        .avatar-block {
            width: 150px;
            height: 150px;
            background-color: var(--color-sky);
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16"><rect width="16" height="16" fill="%2303A9F4"/><rect x="4" y="2" width="8" height="4" fill="%238D6E63"/><rect x="6" y="7" width="2" height="2" fill="%23212121"/><rect x="10" y="7" width="2" height="2" fill="%23212121"/><rect x="4" y="11" width="8" height="2" fill="%23F44336"/></svg>');
            background-size: 100% 100%;
            border: 4px solid var(--color-dirt);
            box-shadow: 8px 8px 0px 0px rgba(0, 0, 0, 0.7);
        }

        /* Ícones em SVG simples e pixelizados */
        .icon-block {
            width: 40px;
            height: 40px;
            @apply flex items-center justify-center p-1.5 blocky text-lg;
        }

    </style>
</head>

<body>

    <!-- Navegação (Navbar Block) -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 navbar-block">
        <nav class="container mx-auto max-w-5xl px-4 py-4 flex justify-between items-center">
            <a href="#hero" class="text-2xl font-pixel text-orange-400 hover:text-red-600 transition duration-150">/home/IA_Student</a>
            <div class="hidden md:flex space-x-4">
                <a href="#inventario" class="text-gray-300 hover:text-white font-inter">Inventário</a>
                <a href="#projetos" class="text-gray-300 hover:text-white font-inter">Mesa de Trabalho</a>
                <a href="#jornada" class="text-gray-300 hover:text-white font-inter">Mapa</a>
                <a href="#contato" class="text-orange-400 hover:text-red-600 font-inter font-bold">Comando</a>
            </div>
            <!-- Menu Hamburguer para Mobile (simplificado) -->
            <button id="menu-toggle" class="md:hidden text-white text-3xl font-pixel px-2 py-1 blocky bg-gray-700">≡</button>
        </nav>
        <!-- Menu Mobile -->
        <div id="mobile-menu" class="hidden md:hidden bg-gray-800 py-2 border-t-2 border-red-600">
            <a href="#inventario" class="block px-4 py-2 hover:bg-gray-700">Inventário</a>
            <a href="#projetos" class="block px-4 py-2 hover:bg-gray-700">Mesa de Trabalho</a>
            <a href="#jornada" class="block px-4 py-2 hover:bg-gray-700">Mapa</a>
            <a href="#contato" class="block px-4 py-2 text-red-400 hover:bg-gray-700">Comando</a>
        </div>
    </header>

    <!-- 1. O Bloco Inicial (Hero Section) -->
    <section id="hero" class="min-h-screen flex items-center justify-center text-center bg-green-600 border-b-8 border-amber-800 p-8">
        <div class="max-w-4xl mx-auto p-6 bg-gray-700 blocky">
            
            <div class="mx-auto mb-6 avatar-block" role="img" aria-label="Avatar pixelizado do estudante de I.A."></div>

            <h1 class="text-4xl sm:text-6xl font-pixel mb-4 text-orange-300 leading-tight blocky p-2 bg-gray-900/50">
                MINERANDO DADOS, <br> CONSTRUINDO INTELIGÊNCIA.
            </h1>
            <h2 class="text-lg sm:text-2xl mb-8 text-gray-200">
                Estudante de I.A. – Próximo Bloco: Seu Projeto.
            </h2>
            
            <!-- CTA Primário -->
            <a href="#projetos" class="inline-block bg-red-600 text-white blocky-btn hover:bg-red-700">
                ⛏ INICIAR MINERAÇÃO (VER PROJETOS)
            </a>
            
            <a href="#contato" class="inline-block bg-sky-500 text-white blocky-btn hover:bg-sky-600 mt-4 md:mt-0 md:ml-4">
                📦 QUEBRAR BLOCO (CONTATO)
            </a>
        </div>
    </section>

    <!-- 2. O Inventário (Sobre o Estudante / Habilidades) -->
    <section id="inventario" class="py-16 bg-amber-800 border-b-8 border-gray-700 p-4">
        <div class="container mx-auto max-w-5xl">
            <h2 class="text-3xl sm:text-5xl font-pixel mb-10 text-yellow-200 text-center">
                MEU INVENTÁRIO DE CONHECIMENTO
            </h2>
            
            <p class="text-center text-gray-200 mb-12 max-w-3xl mx-auto">
                Assim como um minerador precisa das ferramentas certas, eu carrego os **blocos de código** e os **minérios raros** necessários para construir soluções eficientes em I.A.
            </p>

            <div class="grid md:grid-cols-2 gap-8">
                <!-- Itens de Ferramenta (Linguagens/Frameworks) -->
                <div class="p-6 bg-gray-700 blocky border-4 border-gray-900">
                    <h3 class="text-2xl font-pixel mb-4 text-green-300">
                        ITENS DE FERRAMENTA (Stack)
                    </h3>
                    <ul class="space-y-3">
                        <li class="flex items-center">
                            <span class="icon-block bg-sky-500 text-white mr-3">🐍</span> 
                            <span class="font-bold">Python:</span> Picareta principal para Machine Learning.
                        </li>
                        <li class="flex items-center">
                            <span class="icon-block bg-red-600 text-white mr-3">⛶</span> 
                            <span class="font-bold">TensorFlow/PyTorch:</span> Bloco de Comando para Redes Neurais.
                        </li>
                        <li class="flex items-center">
                            <span class="icon-block bg-yellow-600 text-white mr-3">📊</span> 
                            <span class="font-bold">Pandas/Numpy:</span> Pá de Ferro para Limpeza e Preparação de Dados.
                        </li>
                        <li class="flex items-center">
                            <span class="icon-block bg-green-800 text-white mr-3">💾</span> 
                            <span class="font-bold">SQL:</span> Minério Raro para Gerenciamento de Bancos de Dados.
                        </li>
                    </ul>
                </div>

                <!-- Minérios Raros (Soft Skills) -->
                <div class="p-6 bg-gray-700 blocky border-4 border-gray-900">
                    <h3 class="text-2xl font-pixel mb-4 text-green-300">
                        MINÉRIOS RAROS (Soft Skills)
                    </h3>
                    <ul class="space-y-3">
                        <li class="flex items-center">
                            <span class="icon-block bg-white text-black mr-3">💡</span> 
                            <span class="font-bold">Aprendizado Rápido:</span> Nova Receita de Crafting em minutos.
                        </li>
                        <li class="flex items-center">
                            <span class="icon-block bg-orange-400 text-white mr-3">🗺</span> 
                            <span class="font-bold">Resolução de Problemas:</span> Encontrando o caminho no bioma mais complexo.
                        </li>
                        <li class="flex items-center">
                            <span class="icon-block bg-blue-400 text-white mr-3">🤝</span> 
                            <span class="font-bold">Trabalho em Equipe:</span> Construindo Megastruturas em conjunto.
                        </li>
                        <li class="flex items-center">
                            <span class="icon-block bg-purple-600 text-white mr-3">⚙</span> 
                            <span class="font-bold">Otimização:</span> Transformando carvão em bloco de diamante.
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- 3. A Mesa de Trabalho (Projetos / Portfólio) -->
    <section id="projetos" class="py-16 bg-gray-900 border-b-8 border-red-600 p-4">
        <div class="container mx-auto max-w-5xl">
            <h2 class="text-3xl sm:text-5xl font-pixel mb-12 text-sky-400 text-center">
                MINHAS CRIAÇÕES NA MESA DE TRABALHO
            </h2>
            
            <div class="grid md:grid-cols-3 gap-8">
                <!-- Projeto 1: Sistema de Proteção Griefer -->
                <div class="p-6 bg-gray-700 blocky border-4 border-orange-400/50">
                    <h3 class="text-2xl font-pixel mb-3 text-orange-400">
                        Sistema de Proteção Griefer
                    </h3>
                    <p class="text-sm text-gray-300 mb-4">
                        Classificador de texto para identificar e filtrar spam ou linguagem nociva (griefers) em fóruns ou chats, utilizando Processamento de Linguagem Natural (NLP).
                    </p>
                    <div class="text-xs bg-gray-800 p-2 mb-4 blocky">
                        <span class="font-bold text-green-300">Blocos Utilizados (Stack):</span> Python, NLTK, Scikit-learn, FastAPI.
                    </div>
                    <a href="#" class="block w-full text-center bg-green-600 text-white blocky-btn text-base hover:bg-green-700 mb-2">
                        Ver a Construção (GitHub)
                    </a>
                    <a href="#" class="block w-full text-center bg-gray-500 text-white blocky-btn text-base hover:bg-gray-600">
                        Ver o Resultado (Demo)
                    </a>
                </div>

                <!-- Projeto 2: Otimizador de Rota de Comércio -->
                <div class="p-6 bg-gray-700 blocky border-4 border-orange-400/50">
                    <h3 class="text-2xl font-pixel mb-3 text-orange-400">
                        Otimizador de Rota de Comércio
                    </h3>
                    <p class="text-sm text-gray-300 mb-4">
                        Algoritmo de Machine Learning (Regressão) para prever a rota de comércio mais eficiente para vilagers, minimizando tempo e recursos (Travelling Salesman Problem).
                    </p>
                    <div class="text-xs bg-gray-800 p-2 mb-4 blocky">
                        <span class="font-bold text-green-300">Blocos Utilizados (Stack):</span> Python, Pandas, Matplotlib, Algoritmos de Otimização.
                    </div>
                    <a href="#" class="block w-full text-center bg-green-600 text-white blocky-btn text-base hover:bg-green-700 mb-2">
                        Ver a Construção (GitHub)
                    </a>
                    <a href="#" class="block w-full text-center bg-gray-500 text-white blocky-btn text-base hover:bg-gray-600">
                        Ver o Resultado (Demo)
                    </a>
                </div>

                <!-- Projeto 3: Reconhecimento de Blocos (Visão Computacional) -->
                <div class="p-6 bg-gray-700 blocky border-4 border-orange-400/50">
                    <h3 class="text-2xl font-pixel mb-3 text-orange-400">
                        Reconhecimento de Blocos
                    </h3>
                    <p class="text-sm text-gray-300 mb-4">
                        Modelo de Visão Computacional (CNN) treinado para identificar e classificar diferentes tipos de blocos (grama, pedra, areia) a partir de imagens pixelizadas.
                    </p>
                    <div class="text-xs bg-gray-800 p-2 mb-4 blocky">
                        <span class="font-bold text-green-300">Blocos Utilizados (Stack):</span> TensorFlow, Keras, OpenCV, Jupyter Notebooks.
                    </div>
                    <a href="#" class="block w-full text-center bg-green-600 text-white blocky-btn text-base hover:bg-green-700 mb-2">
                        Ver a Construção (GitHub)
                    </a>
                    <a href="#" class="block w-full text-center bg-gray-500 text-white blocky-btn text-base hover:bg-gray-600">
                        Ver o Resultado (Demo)
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- 4. As Redstone Lamps (Filosofia de Aprendizado) -->
    <section id="filosofia" class="py-16 bg-amber-800 border-b-8 border-green-600 p-4">
        <div class="container mx-auto max-w-5xl">
            <h2 class="text-3xl sm:text-5xl font-pixel mb-10 text-red-400 text-center">
                REDSTONE ACIONADA (FILOSOFIA)
            </h2>
            <div class="p-8 bg-gray-700 blocky border-4 border-red-600/70">
                <h3 class="text-xl font-pixel mb-4 text-green-300">
                    COMO EU CONSTRUO MEU CONHECIMENTO
                </h3>
                <p class="text-lg text-gray-200">
                    Em I.A., cada falha é um experimento e cada bug é um bloco que foi colocado no lugar errado. Minha filosofia é que o **aprendizado é um loop de feedback contínuo**, como a lógica da Redstone. Eu não paro de construir e refatorar até que o circuito (o modelo) esteja funcionando com máxima eficiência. Estou sempre buscando novos *mods* (bibliotecas) e *texturas* (abordagens) para melhorar minhas criações. A curiosidade é meu combustível, e o código é a minha **picareta de diamante**.
                </p>
            </div>
        </div>
    </section>

    <!-- 5. O Mapa (Jornada e Próximos Passos) -->
    <section id="jornada" class="py-16 bg-gray-900 border-b-8 border-gray-700 p-4">
        <div class="container mx-auto max-w-5xl">
            <h2 class="text-3xl sm:text-5xl font-pixel mb-12 text-sky-400 text-center">
                EXPLORANDO O MAPA DE CARREIRA
            </h2>

            <!-- Linha do Tempo Pixelizada -->
            <div class="relative pl-8 md:pl-12">
                <!-- Linha Vertical -->
                <div class="absolute left-0 top-0 h-full w-2 bg-gray-700 blocky"></div>
                
                <div class="space-y-12">
                    
                    <!-- Fase 1 -->
                    <div class="relative timeline-item p-4 bg-amber-800 blocky border-4 border-dirt">
                        <p class="font-pixel text-xl text-yellow-200 mb-1">Fase 1: O Bloco de Terra</p>
                        <p class="text-sm text-gray-200">
                            **Curso Básico de I.A. & Fundamentos de Python.** Aprendizado da sintaxe e estruturas básicas. Colocando os primeiros blocos no mundo da programação.
                        </p>
                    </div>

                    <!-- Fase 2 -->
                    <div class="relative timeline-item p-4 bg-gray-700 blocky border-4 border-stone">
                        <p class="font-pixel text-xl text-yellow-200 mb-1">Fase 2: Encontrando o Carvão</p>
                        <p class="text-sm text-gray-200">
                            **Machine Learning Clássico & Projetos Supervisionados.** Implementação de modelos básicos (Regressão, Classificação). Ganhando a primeira experiência prática.
                        </p>
                    </div>

                    <!-- Fase 3 -->
                    <div class="relative timeline-item p-4 bg-green-600 blocky border-4 border-grass">
                        <p class="font-pixel text-xl text-yellow-200 mb-1">Fase 3: O Primeiro Diamante</p>
                        <p class="text-sm text-gray-200">
                            **Deep Learning & Visão Computacional/NLP.** Trabalhando com Redes Neurais e projetos mais complexos (como os do Portfólio). Construindo ferramentas avançadas.
                        </p>
                    </div>

                    <!-- Próximo Bloco (Objetivo) -->
                    <div class="relative timeline-item p-4 bg-red-600 blocky border-4 border-redstone">
                        <p class="font-pixel text-xl text-yellow-200 mb-1">PRÓXIMO BLOCO: Portal!</p>
                        <p class="text-lg font-bold text-white">
                            Busca ativa por Estágio, Mentoria ou Oportunidade de Projeto em tempo integral para aplicar e expandir minhas habilidades de I.A.
                        </p>
                    </div>

                </div>
            </div>
        </div>
    </section>

    <!-- 6. O Bloco de Comando (CTA Final / Contato) -->
    <section id="contato" class="py-16 bg-amber-800 p-4">
        <div class="container mx-auto max-w-4xl">
            <h2 class="text-3xl sm:text-5xl font-pixel mb-12 text-red-400 text-center">
                EXECUTE O COMANDO (CONECTE-SE)
            </h2>

            <div class="p-8 bg-gray-700 blocky border-4 border-sky-400">
                <p class="text-lg text-gray-200 mb-6 text-center">
                    Pronto para me adicionar ao seu time e construir o futuro com I.A.? Deixe sua mensagem abaixo!
                </p>

                <form id="contact-form" class="space-y-4">
                    <!-- Campo Nome -->
                    <div>
                        <label for="name" class="block text-gray-200 font-pixel mb-1">Bloco (Nome):</label>
                        <input type="text" id="name" name="name" required
                               class="w-full p-3 bg-gray-800 text-white blocky border-2 border-gray-900 focus:border-sky-400">
                    </div>

                    <!-- Campo Email -->
                    <div>
                        <label for="email" class="block text-gray-200 font-pixel mb-1">Redstone (Email):</label>
                        <input type="email" id="email" name="email" required
                               class="w-full p-3 bg-gray-800 text-white blocky border-2 border-gray-900 focus:border-sky-400">
                    </div>

                    <!-- Campo Mensagem -->
                    <div>
                        <label for="message" class="block text-gray-200 font-pixel mb-1">Mensagem (Comando):</label>
                        <textarea id="message" name="message" rows="4" required
                                  class="w-full p-3 bg-gray-800 text-white blocky border-2 border-gray-900 focus:border-sky-400"></textarea>
                    </div>

                    <!-- CTA de Envio -->
                    <button type="submit" class="w-full bg-red-600 text-white blocky-btn hover:bg-red-700 mt-4">
                        ENVIAR MENSAGEM (COMANDAR) 🚀
                    </button>
                    <div id="form-message" class="mt-4 text-center font-pixel text-lg hidden"></div>
                </form>

                <!-- Informações de Contato / Links -->
                <div class="mt-8 pt-4 border-t-2 border-sky-400/50 text-center">
                    <h3 class="font-pixel text-xl mb-3 text-sky-400">Portal & Baús Pessoais</h3>
                    <div class="flex justify-center space-x-6">
                        <a href="https://linkedin.com/in/seuperfil" target="_blank" class="text-white hover:text-sky-400 transition-colors duration-150">
                            <span class="text-3xl">🔗</span> LinkedIn (Portal)
                        </a>
                        <a href="https://github.com/seuusuario" target="_blank" class="text-white hover:text-sky-400 transition-colors duration-150">
                            <span class="text-3xl">📦</span> GitHub (Baú de Código)
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer class="bg-gray-900 py-4 text-center font-pixel text-sm text-gray-500">
        <p>Copyright &copy; 2025 Minerando Dados. Landing Page construída com blocos e código.</p>
    </footer>

    <script>
        // JavaScript para interatividade (Menu Mobile e Formulario)

        document.addEventListener('DOMContentLoaded', () => {
            const menuToggle = document.getElementById('menu-toggle');
            const mobileMenu = document.getElementById('mobile-menu');
            const form = document.getElementById('contact-form');
            const formMessage = document.getElementById('form-message');

            // 1. Menu Mobile
            menuToggle.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });
            
            // Fechar menu mobile ao clicar em um link
            mobileMenu.querySelectorAll('a').forEach(link => {
                link.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                });
            });


            // 2. Validação e Simulação de Envio de Formulário (Boas Práticas de LP)
            form.addEventListener('submit', async (e) => {
                e.preventDefault();
                
                // Simulação de delay de envio (para feedback visual)
                const submitButton = form.querySelector('button[type="submit"]');
                const originalText = submitButton.textContent;
                
                submitButton.textContent = 'EXECUTANDO COMANDO...';
                submitButton.disabled = true;

                await new Promise(resolve => setTimeout(resolve, 1500)); // Espera 1.5s

                // Exibe a mensagem de sucesso
                formMessage.classList.remove('hidden');
                formMessage.classList.remove('text-red-400');
                formMessage.classList.add('text-green-300');
                formMessage.textContent = '✅ Comando Executado! Mensagem enviada com sucesso.';

                // Restaura o botão
                submitButton.textContent = originalText;
                submitButton.disabled = false;
                form.reset();

                // Esconde a mensagem após 5 segundos
                setTimeout(() => {
                    formMessage.classList.add('hidden');
                }, 5000);
            });
        });
    </script>
</body>
</html>
