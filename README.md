
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mercantil Araújo</title>
    <link rel="stylesheet" href="styles.css">
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY"></script>
    <script src="https://translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        nav {
            background-color: #444;
            color: white;
            padding: 10px;
        }
        nav a {
            color: white;
            margin: 0 15px;
            text-decoration: none;
        }
        .container {
            padding: 20px;
        }
        .map {
            height: 400px;
            width: 100%;
        }
        .section {
            margin-bottom: 40px;
        }
        .portfolio img {
            max-width: 100%;
            height: auto;
        }
    </style>
</head>
<body>
    <header>
        <h1>Mercantil Araújo</h1>
        <nav>
            <a href="#home">Início</a>
            <a href="#map">Mapa</a>
            <a href="#ads">Anúncios</a>
            <a href="#portfolio">Portfólio</a>
        </nav>
    </header>

    <div class="container">
        <div id="google_translate_element"></div>

        <section id="home" class="section">
            <h2>Bem-vindo ao Mercantil Araújo</h2>
            <p>Seu comércio de confiança para produtos e serviços de qualidade.</p>
            <p>Contato: (88)9 9693-2054 falar com Sr.Adriano</p>
            <p>Endereço: Rua Domingos Savio N°359 Bairro Pio XII em Juazeiro do Norte,CE-BR.</p>
        </section>

        <section id="map" class="section">
            <h2>Encontre-nos</h2>
            <div id="map" class="map"></div>
        </section>

        <section id="ads" class="section">
            <h2>Anúncios</h2>
            <div>
                <h3>Produto 1</h3>
                <p>Descrição do produto 1.</p>
            </div>
            <div>
                <h3>Produto 2</h3>
                <p>Descrição do produto 2.</p>
            </div>
        </section>

        <section id="portfolio" class="section">
            <h2>Portfólio</h2>
            <div class="portfolio">
                <img src="portfolio1.jpg" alt="Portfólio 1">
                <img src="portfolio2.jpg" alt="Portfólio 2">
            </div>
        </section>
    </div>

    <script>
        function initMap() {
            var mercantil = { lat: -23.550520, lng: -46.633308 }; // Coordenadas de exemplo
            var map = new google.maps.Map(document.getElementById('map'), {
                zoom: 15,
                center: mercantil
            });
            var marker = new google.maps.Marker({
                position: mercantil,
                map: map
            });
        }
        
        function googleTranslateElementInit() {
            new google.translate.TranslateElement({pageLanguage: 'pt'}, 'google_translate_element');
        }

        window.onload = function() {
            initMap();
        }
    </script>
</body>
</html>
