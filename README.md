# Projet-ATT-jehda : AT&T Spam Detector

Projet de groupe Jedha (Fullstack IA) : détecter automatiquement les SMS de spam à partir de leur seul contenu, avec un ou plusieurs modèles de deep learning.

## Données

`src/spam.csv` : 5 572 SMS étiquetés `ham` / `spam` ([source](https://full-stack-bigdata-datasets.s3.eu-west-3.amazonaws.com/Deep+Learning/project/spam.csv)).
⚠️ Encodage **latin-1**.

## Installation

```bash
git clone https://github.com/MaquiZard05/Projet-ATT-jehda.git
cd Projet-ATT-jehda
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Dans VS Code, choisir le kernel `.venv`.

## Notebooks, dans l'ordre

| # | Notebook | Entrée | Sortie | Responsable |
|---|---|---|---|---|
| 0 | `01-AT&T_spam_detector.ipynb` | énoncé | — | — |
| 1 | `02-Template_1_preparation_donnees.ipynb` | `src/spam.csv` | `src/train.csv`, `src/val.csv`, `src/test.csv` | … |
| 2 | Modèle simple : embeddings + petit réseau | les 3 CSV | modèle + scores | … |
| 3 | Transfer learning : modèle Hugging Face | les 3 CSV | modèle + scores | … |
| 4 | Évaluation et conclusion | les scores | tableau final | … |

## Résultats

Classe spam minoritaire (environ 13 %) : on compare les modèles sur le **F1** et le **recall** de la classe spam, pas seulement l'accuracy.

| Modèle | Accuracy | Précision spam | Recall spam | F1 spam |
|---|---|---|---|---|
| … | | | | |

## Règles de travail en groupe

- **Un notebook = un responsable** : on ne modifie pas le notebook d'un autre (les conflits Git sur les `.ipynb` sont très pénibles).
- **Une branche par tâche** (`prep-donnees`, `modele-embeddings`…), jamais de commit direct sur `main`.
- On fusionne dans `main` par **Pull Request**, relue par un autre membre.
- `git pull` avant de commencer à travailler.
- Les modèles entraînés ne vont **pas** sur GitHub (voir `.gitignore`).

## Équipe

- …
