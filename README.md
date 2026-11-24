# TP 2 — « L'IA lit 40 ans d'images de ma ville »

Entraîner un modèle de Machine Learning à reconnaître le bâti, puis l'appliquer à 40 ans d'archives d'images satellites Landsat.

Le TP se déroule entièrement dans **Google Colab** : aucune installation n'est nécessaire sur votre ordinateur. Il vous faut seulement un navigateur web (Chrome de préférence) et un compte Google.

---

## Ouvrir le notebook dans Google Colab

### Étape 1 — Se connecter à son compte Google

1. Allez sur [https://colab.research.google.com](https://colab.research.google.com).
2. Cliquez sur **Se connecter** (en haut à droite) et connectez-vous avec votre compte Google (Gmail).
   - Pas de compte Google ? Créez-en un gratuitement sur [https://accounts.google.com/signup](https://accounts.google.com/signup).

### Étape 2 — Importer le notebook depuis GitHub

1. Une fois connecté, la fenêtre **Ouvrir un notebook** s'affiche. Si elle n'apparaît pas, cliquez sur **Fichier → Ouvrir un notebook**.
2. Choisissez l'onglet **GitHub**.
3. Dans le champ de recherche, collez l'adresse du dépôt :
   ```
   https://github.com/allamed/TP-ML
   ```
   puis appuyez sur **Entrée** (ou cliquez sur la loupe).
4. Cliquez sur le fichier **`TP2_IA_etalement_urbain.ipynb`** dans la liste. Le notebook s'ouvre.

> **Raccourci :** vous pouvez aussi ouvrir directement ce lien après vous être connecté :
> [https://colab.research.google.com/github/allamed/TP-ML/blob/main/TP2_IA_etalement_urbain.ipynb](https://colab.research.google.com/github/allamed/TP-ML/blob/main/TP2_IA_etalement_urbain.ipynb)

### Étape 3 — Enregistrer votre propre copie

Le notebook ouvert depuis GitHub est en lecture seule : vos modifications ne seront pas conservées.

1. Cliquez sur **Fichier → Enregistrer une copie dans Drive**.
2. Une nouvelle copie s'ouvre dans un nouvel onglet. **Travaillez dans cette copie.** Elle est rangée dans votre Google Drive, dans le dossier **Colab Notebooks**.

### Étape 4 — Lancer le notebook

1. Cliquez sur **Connecter** (en haut à droite) pour démarrer une machine Colab gratuite.
2. Exécutez les cellules **une par une, dans l'ordre**, en cliquant sur le bouton ▶ à gauche de chaque cellule (ou avec **Maj + Entrée**).
3. La première cellule de code installe les bibliothèques nécessaires (environ 1 minute).
   - Si Colab affiche « *Ce notebook n'a pas été créé par Google* », cliquez sur **Exécuter quand même**.
   - Si Colab propose de **redémarrer la session** après l'installation, acceptez, puis reprenez à la cellule suivante.

---

## Conseils

- **Changer de ville :** modifiez la variable `NOM_ZONE` (et la zone associée) dans la cellule prévue à cet effet, puis réexécutez les cellules suivantes.
- **Session déconnectée ?** Colab coupe la machine après une période d'inactivité. Cliquez sur **Exécution → Tout exécuter** pour tout relancer.
- **Récupérer les résultats :** à l'étape 10, les fichiers produits (`.tif` et `.csv`) apparaissent dans le panneau **Fichiers** (icône 📁 à gauche). Faites un clic droit sur un fichier → **Télécharger**. Ces fichiers sont effacés à la fermeture de la session : pensez à les télécharger avant de partir.
