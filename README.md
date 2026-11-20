# Cantera dans le navigateur

[![Lancer avec Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/vincentrobin/cantera-binder/main?urlpath=lab%2Ftree%2F00_demarrage.ipynb)

Un environnement Python et Cantera pour travailler dans JupyterLab, sans installation sur son ordinateur et sans compte à créer.

## Démarrer

1. Cliquer sur **Lancer avec Binder** ci-dessus. Le premier démarrage peut prendre plusieurs minutes, le temps de construire l'environnement.
2. Dans le notebook `00_demarrage.ipynb`, choisir **Run → Run All Cells** pour exécuter l'exemple complet. Pour avancer cellule par cellule, utiliser **Maj + Entrée**.
3. Modifier les paramètres et relancer les cellules concernées. Le noyau à utiliser est **Python 3 (ipykernel)**.

Le notebook calcule la température adiabatique d'équilibre d'un mélange méthane/air, puis la trace en fonction de la richesse. Les hypothèses et les unités sont précisées dans le notebook. Ce calcul d'équilibre ne fournit ni vitesse de flamme ni délai d'auto-inflammation.

## Utiliser ses propres fichiers

- Pour créer un notebook : **File → New → Notebook**, puis choisir le noyau Python 3.
- Pour importer un notebook, un mécanisme YAML ou des données : utiliser le bouton **Upload Files** (flèche vers le haut) dans l'explorateur de fichiers à gauche, ou y glisser les fichiers.
- Les fichiers importés sont utilisables depuis les notebooks du même dossier. Par exemple : `ct.Solution("mon_mecanisme.yaml")`.

Les anciens mécanismes CTI/XML doivent être convertis au format YAML pour Cantera 3.2. Importer un ancien notebook ne garantit pas sa compatibilité avec cette version.

## Sauvegarder son travail

**Les fichiers de la session sont temporaires. Les enregistrer dans JupyterLab ne les conserve pas après la suppression de la session.**

Avant de quitter, enregistrer le notebook (**Ctrl + S**, ou **Cmd + S** sur Mac), puis faire un clic droit sur son nom dans l'explorateur et choisir **Download**. Faire de même pour les mécanismes, données et résultats à conserver. Le notebook d'exemple produit `resultats_equilibre.csv` et `temperature_equilibre.png` dans son dossier.

Chaque lancement démarre une session indépendante à partir du dépôt GitHub. Les modifications faites dans Binder ne modifient pas ce dépôt.

## Versions et limites

- Python **3.12**, Cantera **3.2.0** ; NumPy, Matplotlib, pandas, JupyterLab et ipykernel sont installés depuis **conda-forge**. La version de Cantera est fixée dans `environment.yml` ; toutes les dépendances transitives ne sont pas figées.
- Binder est un service gratuit à ressources limitées, adapté aux essais et aux exercices courts. Sa disponibilité et la durée de la session ne sont pas garanties. Télécharger régulièrement son travail ; éviter les calculs longs ou les grandes études paramétriques.
- Utiliser uniquement des fichiers non confidentiels dans ce service public.

[Documentation de Cantera 3.2](https://cantera.org/3.2/) · [Règles d'utilisation de Binder](https://mybinder.readthedocs.io/en/latest/about/user-guidelines.html)
