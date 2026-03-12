# ETL-Project-World-GDP
# Présentation

Ce projet vise à automatiser la collecte et le traitement des données relatives au Produit Intérieur Brut (PIB/GDP) nominal des pays à travers le monde. Il permet d'extraire des données économiques brutes depuis le web, de les normaliser dans une unité commune (milliards de dollars) et de les stocker pour des requêtes ultérieures.

# Fonctionnement du code

Le pipeline est structuré autour des trois piliers du Data Engineering :

- Extraction : Utilisation du Web Scraping pour récupérer les données de la liste des pays par PIB sur Wikipédia.

- Transformation :
  - Conversion des données textuelles en formats numériques exploitables.
  - Conversion des valeurs de millions en milliards de dollars (Billions) pour une meilleure lisibilité.
  - Arrondi des résultats à deux décimales.

- Chargement :
  - Sauvegarde des données transformées dans un fichier Countries_by_GDP.csv.
  - Archivage dans une base de données SQL (World_Economies.db) sous forme de table.

# Outils utilisés
- Langage : Python.
- Bibliothèques principales :
  - Pandas et NumPy pour la manipulation des données.
  - BeautifulSoup et Requests pour l'extraction des données web.
  - SQLite3 pour la gestion de la base de données.
- IDE : Visual Studio Code.

# Comment lancer le projet
1. Téléchargez le fichier etl_project_gdp.py.
2. Installez les dépendances nécessaires : pip install pandas beautifulsoup4 requests.
3. Exécutez le script : python etl_project_gdp.py.
4. Le script générera automatiquement un fichier de log (etl_project_log.txt) pour suivre l'état de l'exécution.
