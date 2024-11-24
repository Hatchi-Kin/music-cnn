# Music Genre Classification

Ce projet vise à classifier les genres musicaux en utilisant un réseau de neurones convolutifs (CNN) personnalisé, entraîné sur des spectrogrammes de chansons. Le projet est divisé en plusieurs parties, chacune contenue dans différents dossiers.

## Structure du Projet

- **preprocessing**: Contient des notebooks Jupyter (`.ipynb`) utilisés pour le prétraitement des données du projet MegaPi. Ces scripts créent la base de données de tous les fichiers audio utilisés pour le projet.
  - `01_pickles.ipynb`: Création de fichiers pickle.
  - `02_full_extraction.ipynb`: Extraction complète des données.
  - `03_add_top5.ipynb`: Ajout des 5 genres principaux.
  - `04_insert_into_milvus.ipynb`: Insertion des données dans Milvus.
  - `05_take_it_for_a_spin.ipynb`: Test des données.
  - `07_metadata_into_sqlite.ipynb`: Insertion des métadonnées dans une base de données SQLite.

- **beat_openl3**: Contient le code pour créer un dataset au format `ImageFolder` de PyTorch et entraîner un CNN personnalisé pour détecter les genres musicaux dans les chansons basées sur des spectrogrammes. Il enregistre également le processus d'entraînement dans MLflow.
  - `01_authenticated_mlflow.ipynb`: Authentification avec MLflow.
  - `02_create_dataset.ipynb`: Création du dataset.
  - `03_create_spectrograms_dataset.ipynb`: Création du dataset de spectrogrammes.
  - `04_train_music_net.COLAB.ipynb` et `04_train_music_net.LOCAL.ipynb`: Entraînement du réseau de neurones sur Colab et en local.
  - `05_inference_with_best_model.ipynb`: Inférence avec le meilleur modèle.
  - `06_test_model.ipynb`: Test du modèle.

- **utils**: Contient des utilitaires liés au modèle OpenL3 pré-entraîné que nous essayons de surpasser avec notre propre modèle.

## Installation

Pour installer les dépendances, exécutez :

```sh
pip install -r requirements.txt
```

## Utilisation

1. Prétraitement des données :
   - Exécutez les notebooks dans le dossier `preprocessing` pour préparer les données.

2. Création du dataset et entraînement du modèle :
   - Exécutez les notebooks dans le dossier `beat_openl3` pour créer le dataset de spectrogrammes et entraîner le modèle.

3. Inférence et test :
   - Utilisez les notebooks `05_inference_with_best_model.ipynb` et `06_test_model.ipynb` pour effectuer des inférences et tester le modèle.
