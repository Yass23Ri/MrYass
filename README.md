<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Armoire 3D Statique</title>
    <!-- Lien vers Font Awesome pour les icônes -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Réinitialisation des styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Arrière-plan avec logos miniatures */
        body {
            font-family: Arial, sans-serif;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="50" height="50"><text x="50%" y="50%" dominant-baseline="middle" text-anchor="middle" font-size="20" fill="rgba(255, 255, 255, 0.1)">🎵</text></svg>'),
                        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="50" height="50"><text x="50%" y="50%" dominant-baseline="middle" text-anchor="middle" font-size="20" fill="rgba(255, 0, 0, 0.1)">▶️</text></svg>'),
                        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" width="50" height="50"><text x="50%" y="50%" dominant-baseline="middle" text-anchor="middle" font-size="20" fill="rgba(0, 136, 204, 0.1)">✈️</text></svg>'),
                        linear-gradient(135deg, #1e3c72, #2a5298); /* Dégradé bleu */
            background-size: 50px 50px; /* Taille des logos miniatures */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            perspective: 1000px; /* Perspective pour l'effet 3D */
        }

        /* Conteneur de l'armoire */
        .armoire {
            position: relative;
            width: 300px;
            height: 400px;
            transform-style: preserve-3d; /* Conserve la 3D */
            transform: rotateY(20deg); /* Rotation légère pour voir l'effet 3D */
        }

        /* Face avant de l'armoire */
        .face {
            position: absolute;
            width: 100%;
            height: 100%;
            background-color: rgba(208, 208, 208, 0.9); /* Fond semi-transparent */
            border: 2px solid #ccc;
            border-radius: 10px;
            display: flex;
            flex-direction: column;
            justify-content: space-around;
            align-items: center;
            padding: 20px;
            backface-visibility: hidden; /* Cache la face arrière */
            transform: translateZ(50px); /* Avance la face avant */
        }

        /* Tiroirs en 3D */
        .tiroir {
            width: 80%;
            height: 20%;
            border: 1px solid #999;
            border-radius: 5px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            transform-style: preserve-3d;
            transform: translateZ(20px); /* Effet 3D pour les tiroirs */
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Ombre pour le relief */
        }

        /* Couleurs personnalisées pour les tiroirs */
        .tiroir.youtube {
            background-color: #ff0000; /* Rouge pour YouTube */
        }

        .tiroir.tiktok {
            background-color: #000000; /* Noir pour TikTok */
        }

        .tiroir.telegram {
            background-color: #0088cc; /* Bleu pour Telegram */
        }

        /* Texte et icônes des tiroirs */
        .tiroir a {
            text-decoration: none;
            color: white; /* Texte en blanc pour contraster */
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 100%;
            gap: 10px; /* Espace entre l'icône et le texte */
        }

        /* Style des icônes */
        .tiroir i {
            font-size: 24px; /* Taille des icônes */
        }

        /* Effet de relief au survol */
        .tiroir:hover {
            transform: translateZ(30px); /* Effet 3D plus prononcé au survol */
        }
    </style>
</head>
<body>
    <!-- Conteneur de l'armoire -->
    <div class="armoire">
        <!-- Face avant de l'armoire -->
        <div class="face">
            <!-- Tiroir TikTok -->
            <div class="tiroir tiktok">
                <a href="https://www.tiktok.com/@.mr_yass" target="_blank">
                    <i class="fab fa-tiktok"></i> <!-- Icône TikTok -->
                    TikTok
                </a>
            </div>
            <!-- Tiroir YouTube -->
            <div class="tiroir youtube">
                <a href="https://youtube.com/@authentiquekingyass?si=rUYRu2s3DQtK5P_2" target="_blank">
                    <i class="fab fa-youtube"></i> <!-- Icône YouTube -->
                    YouTube
                </a>
            </div>
            <!-- Tiroir Telegram -->
            <div class="tiroir telegram">
                <a href="https://t.me/MrYass225" target="_blank">
                    <i class="fab fa-telegram"></i> <!-- Icône Telegram -->
                    Telegram
                </a>
            </div>
        </div>
    </div>
</body>
</html>
