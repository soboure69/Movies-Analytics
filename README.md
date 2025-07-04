# Movies-Analytics
Phase 2 du Projet CinéData

# **Phase 2 : Data Analyst - Exploration et Visualisation**  

![](architecturephase.png)

## Introduction

**Objectif : Explorer et analyser les données en interrogeant l’API.**  

🔹 **Analyse Exploratoire des Données (EDA)** :  
- Utiliser le **SDK Python** pour requêter l’API et récupérer les données.  
- Identifier les tendances dans les notes des films.  
- Étudier les genres les plus populaires et les préférences des utilisateurs.  

🔹 **Construction d’une Data App avec Streamlit** :  
- Créer une **application interactive** qui permet de visualiser les tendances du cinéma.  
- Intégrer des **tableaux dynamiques** et des **graphiques interactifs**.  
- Offrir une **recherche avancée** des films en fonction des notes et des genres.  

**Livrables** :  
- Un notebook d'analyse exploratoire interactif.  
- Une **application web Streamlit** connectée à l’API qui présente, de manière interactive, les insights aux parties prenantes.

---

## Présentation de Jupyter Notebook

**Jupyter Notebook** est un environnement interactif très populaire dans le monde de la **Data Science**. Il permet d’écrire du code Python, de visualiser des graphiques, d’insérer des textes explicatifs (en Markdown), et de documenter une analyse de données de manière fluide et lisible.

---

### Pourquoi Jupyter Notebook est si populaire ?

🔹 **Interactivité totale** : Chaque cellule de code peut être exécutée indépendamment, ce qui permet d’explorer les données pas à pas.

🔹 **Documentation intégrée** : On peut facilement alterner entre du code Python et des explications en langage naturel (Markdown), ce qui en fait un excellent outil pédagogique et professionnel.

🔹 **Visualisation immédiate** : Les bibliothèques comme `matplotlib`, `seaborn` ou `plotly` s’intègrent parfaitement à Jupyter pour créer des visualisations dynamiques.

🔹 **Support riche** : Intègre du HTML, des tableaux interactifs, des widgets, etc. Parfait pour présenter un projet à un client ou à une équipe.

---

### Jupyter Notebook, un outil central pour le Data Analyst

Durant la phase 2, on utilise Jupyter Notebook pour :

- Charger et explorer les données extraites via le SDK (et donc indirectement via l’API).
- Réaliser une **analyse exploratoire** complète : tendances, corrélations, genres populaires...
- Visualiser les résultats sous forme de **graphiques** compréhensibles et exploitables.
- Créer un **notebook professionnel** .


---

## Mise en place de l’environnement d’analyse

Dans ce projet, **VSCode** est l'éditeur principal et chaque phase dans un répertoire Git dédié. Pour cette phase 2 (*Data Analyst – Exploration & Visualisation*), on  travaille dans un nouveau projet nommé `Movies-Analytics`

Voici les étapes pour bien démarrer :

### 1. Cloner le dépôt GitHub du projet

cloner le dépôt Git créé pour cette phase :

```bash
git clone https://github.com/soboure69/Movies-Analytics.git
cd Movies-Analytics
```

### 2. Créer et activer un environnement virtuel

Ensuite, configurer un environnement Python isolé pour gérer les dépendances :

```bash
python -m venv .venv
source .venv/bin/activate # linus
```

> Si Windows :  
> `.\.venv\Scripts\activate`

### 3. Ouvrir le projet dans VSCode

```bash
code .
```

 *"Sélectionner l'interpréteur Python"*, correspondant à  l'environnement `.venv`.

### 4. Créer le notebook


### 5. Installer le SDK `films_sdk_sbre`

Ce SDK permettra d’interagir avec l’API MovieLens.

```bash
pip install films_sdk_sbre
```

### 6. Lancer et configurer le Jupyter Notebook

Ouvre le fichier `.ipynb` dans VSCode. Installer Jupyter (avec `ipykernel`) si ce n'est pas le cas. 

---



---

## Familiarisation avec l'API dans un notebook 

Voir Fichier `Movies-Analytics/films_data_analysis.ipynb` 

## Visualisation des données

Voir Fichier `Movies-Analytics/films_dataviz.ipynb` 

## Intégration de l'API dans une application Streamlit

Streamlit est une bibliothèque open-source en Python qui permet de créer des applications web interactives pour la visualisation de données et le machine learning de manière rapide et simple. Il est particulièrement populaire auprès des Data Scientists, des ingénieurs et des chercheurs qui souhaitent partager leurs analyses et modèles sans avoir à développer des interfaces web complexes.

Avec Streamlit, il suffit de quelques lignes de code pour créer des applications avec des éléments interactifs comme des graphiques, des tables, des cartes, des curseurs, des boutons, etc. Le principal avantage de Streamlit est sa facilité d'utilisation : il transforme un script Python classique en une application web sans avoir besoin de connaître HTML, CSS ou JavaScript.

Voici quelques caractéristiques principales de Streamlit :
- **Simplicité** : Écrire une application Streamlit se fait généralement en quelques lignes de code.
- **Interactivité** : Il permet d'ajouter facilement des widgets interactifs (curseurs, boîtes de sélection, champs de texte, etc.).
- **Intégration facile avec des bibliothèques Python** : Il supporte des bibliothèques populaires telles que Matplotlib, Plotly, Pandas, et bien d’autres.
- **Mise à jour dynamique** : Les modifications apportées au code sont immédiatement visibles sans avoir à recharger la page.

C'est donc un outil idéal pour prototyper des applications de data science rapidement et les déployer de manière simple.

Pour utiliser *streamlit*, préalablement l'installer avec:

```bash
pip install streamlit
```

L'application Streamlit comprendra un fichier de point d'entrée, le fichier que Streamlit chargera en premier. Dans cette application, nous utiliserons ce fichier pour définir la configuration initiale et créer la navigation entre les pages/menus de l'application.


Pour afficher le lien direct vers la page IMDb d'un film ainsi que son image d'affiche, on a besoin d'un clé API OMDb.

1. Aller sur [http://www.omdbapi.com/apikey.aspx](http://www.omdbapi.com/apikey.aspx)
2. Demander une **clé gratuite (Personal Use Only)**
3. On reçoit un mail avec un lien comme :  
   `http://img.omdbapi.com/?i=.........&apikey=LA_CLE`

On peut donc créer une URL `poster_url` très facilement à partir de l’ID IMDb.

---

Le fichier `get_movie_poster.py` permet de générer le fichier "output/links_enriched.parquet" contenant pour chaque film son lien vers sa page IMDb ainsi que le lien de son image d'affiche.

## Déploiement de l'application sur Streamlit Community Cloud

---

# Compétences acquises dans cette phase du projet CinéData
 - Data Analytics
   - Requetage API en Python
   - Analyse EDA sur notebook
   - Visualisation avancée
 - Data App
   - App Streamlit interactive
   - Connexion dynamique API
   - Dashboarding temps réel
