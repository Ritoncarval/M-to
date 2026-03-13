🌅 Chasseur de Lumière — Sunrise & Sunset Predictor
Une application web minimaliste et intelligente conçue pour les photographes de paysage. Elle prédit la qualité visuelle et photographique d'un lever ou coucher de soleil sur une échelle de 1 à 5 étoiles, en croisant des données météorologiques précises avec l'analyse d'une intelligence artificielle.

✨ Fonctionnalités clés
Prévisions Météorologiques Ciblées : Ne se contente pas d'une météo globale. Le script isole l'heure exacte de l'événement (lever/coucher) et analyse la répartition exacte des couches nuageuses (basses, moyennes, hautes/cirrus).

Analyse IA Experte : Utilise Google Gemini (2.5 Flash) configuré avec un prompt strict de photographe professionnel pour juger la qualité de la lumière.

Interface Dynamique & Immersive : L'arrière-plan (halo lumineux) réagit et change d'ambiance en fonction du score généré par l'IA (du gris tempête pour 1 étoile au rouge flamboyant pour 5 étoiles).

Recherche de lieux universelle : Barre de recherche avec autocomplétion mondiale et bouton de détection GPS intégré.

Zéro Base de Données : Application 100% "front-end" (HTML/CSS/JS vanille). Aucune installation requise, s'exécute directement dans le navigateur.

🛠️ Technologies Utilisées
Front-end : HTML5, CSS3 (variables, CSS Grid, animations keyframes), Vanilla JavaScript.

API Météo : Open-Meteo (Gratuit, Open-Source, sans clé API requise) pour le Geocoding et la prévision météo heure par heure.

API Intelligence Artificielle : Google Gemini API (Modèle gemini-2.5-flash).

🧠 L'Algorithme : La Règle d'Or Météorologique
Plutôt que de laisser l'IA "deviner" la météo, le code agit comme un entonnoir de précision. Il transmet les pourcentages exacts de chaque couche nuageuse à l'IA avec ces règles strictes :

Nuages Bas (Épais/Opaques) : S'ils dominent (>50%), la lumière rasante est bloquée. Le ciel sera gris. Score = 1 ou 2.

Nuages Hauts/Cirrus (Fins) : S'ils sont présents (30% à 80%) sans nuages bas pour bloquer le soleil à l'horizon, le ciel s'embrasera (rouge, rose, violet). Score = 4 ou 5.

Ciel Dégagé (0%) : Ciel bleu et clair, mais sans texture pour accrocher la lumière. Score = 3.

L'IA rédige ensuite son verdict et force sa réponse dans un format JSON strict pour être traité par l'interface.

🚀 Installation & Utilisation
Ce projet ne nécessite aucun serveur (Node.js, PHP, etc.).

Cloner ou télécharger le projet sur votre ordinateur.

Obtenir une clé API Gemini :

Rendez-vous sur Google AI Studio.

Connectez-vous et générez une clé API gratuite.

Lancer l'application :

Ouvrez simplement le fichier soleil.html dans n'importe quel navigateur web moderne (Chrome, Safari, Firefox).

Collez votre clé API dans le champ prévu à cet effet (elle sera sauvegardée localement de façon sécurisée dans votre navigateur via localStorage).

Cherchez une ville, choisissez une date, et analysez le ciel !

🔒 Sécurité et Confidentialité
La clé API Google Gemini est requise pour faire fonctionner l'intelligence artificielle. Cette clé n'est transmise à aucun serveur tiers. Elle est stockée exclusivement dans le localStorage de votre navigateur et est envoyée directement aux serveurs officiels de Google lors de l'analyse.

Projet propulsé par l'IA et la passion de la photographie de paysage.