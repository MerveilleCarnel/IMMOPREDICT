# 🏡 ImmoPredict - Prédiction du Prix au m² des Biens Immobiliers en France 🇫🇷

> Ce projet vise à prédire le **prix moyen au m²** de biens immobiliers en France à l'aide d'un modèle **Random Forest** déployé dans une interface **Streamlit**.

## 📌 Objectif

Permettre aux utilisateurs (particuliers ou professionnels) d’estimer le prix au m² d’un bien en fonction de ses caractéristiques géographiques et techniques (code postal, nombre de ventes, surface, etc.).

## 🛠️ Stack Technique

- **Langages** : Python
- **Modélisation** : Scikit-Learn (Random Forest)
- **Interface utilisateur** : Streamlit
- **Prétraitement** : pandas, NumPy,Matplotlib et Seaborn 
- **Sérialisation du modèle** : Joblib

---

## 🗃️ Données

Les données utilisées sont issues d’un **dataset immobilier réel (source: data.gouv)**, comprenant :
- Code postal,
- latitude/longitude
- INSEE_COM (int) : représente le code INSEE de la commune en fait, c’est un 
identifiant unique attribué à chaque commune française par l'Institut national de la 
statistique et des études économiques (INSEE). Il sert à identifier de manière précise et 
non ambiguë une commune, quelle que soit son évolution au fil du temps. 
- Année (int) : représente l’année d’étude du marché immobilier exemple : 2017 
- Propriétaire (int) : nombre de mutations (correspond à tout changement de propriétaire 
d'un bien immobilier). 
- NbMaisons (int) : nombre de maisons vendues. 
- NbApparts(int) : le nombre d'appartements vendus 
- Propmaison (float) : représente La proportion de ventes de maisons et d'appartements 
- Propappart (float): représente La proportion de ventes d'appartements 
- PrixMoyen (float) : Le prix moyen des biens vendus 
- Prixm2Moyen (float) : le prix moyen au mètre carré des biens vendus 
- SurfaceMoy(float) : représente la surface moyenne des biens vendus 

## 📈 Résultats

- Modèle sélectionné : **RandomForestRegressor**
- **Score R²** : ~0.72
- **MAE** : ~280 €/m²
- **Visualisations** : scatter plot des prédictions vs réels, analyse des résidus

## 🧪 Exemple d'utilisation

Lancer l'application localement :

```bash
streamlit run app.py
