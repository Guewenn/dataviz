# 🚅 SNCF DataViz : Tourisme Durable & Mobilité Douce

![Statut du projet](https://img.shields.io/badge/Status-Completed-success)
![Techno](https://img.shields.io/badge/Stack-HTML%20%7C%20JS%20%7C%20Leaflet-blue)
![Course](https://img.shields.io/badge/Projet-DataVisualization-emerald)

> **Comment la donnée ferroviaire peut-elle révéler le potentiel touristique des territoires et favoriser la mobilité douce ?**

Ce projet explore l'intermodalité (Train + Vélo) en croisant les données ouvertes de la SNCF avec celles du tourisme français (Patrimoine Vivant, Labels Qualité, Randonnées).

---

## 🌍 Démonstration

👉 **[Voir le projet en ligne](https://guewenn.mennegaut.mmi-velizy.fr/Dataviz2/)**

---

## ✨ Fonctionnalités Clés

### 🗺️ Cartographie Interactive
- Visualisation de **3000+ gares** françaises (Hubs TGV vs Gares locales).
- Affichage des points d'intérêt : Artisans (EPV), Sites Qualité Tourisme™, Randonnées.
- **Mode "Créa"** : Superposition d'une maquette artistique sur la carte technique.

### 💎 Algorithme "Pépites"
Un algorithme spatial identifie automatiquement les gares à fort potentiel :
1. Analyse la densité de sites touristiques dans un rayon de 10km.
2. Attribue un score pondéré (Bonus pour les petites gares locales).
3. Génère un **Top 15** des destinations à découvrir.

### 🚲 Calcul d'Itinéraire (Le "Dernier Kilomètre")
- Intégration de l'API **OSRM** pour le routage vélo.
- Calcul de la distance réelle et du temps de trajet entre la gare et le site touristique.
- Visualisation des pistes cyclables existantes (GeoJSON).

### 📊 DataViz Connectée (Brushing & Linking)
- Graphiques dynamiques (**Chart.js**) synchronisés avec la carte.
- **Drill-down** : Cliquer sur une barre du graphique (ex: "Verrerie") filtre automatiquement la carte pour n'afficher que cette catégorie.

---

## 🛠️ Stack Technique

Ce projet est réalisé en **Vanilla JS** (ES6+) sans framework lourd, pour une performance maximale.

| Technologie | Usage |
|:--- |:--- |
| **Leaflet.js** | Moteur de carte interactif |
| **Turf.js** | Analyse géospatiale avancée (Distances, Point-in-Polygon) |
| **Chart.js** | Graphiques statistiques interactifs |
| **Tailwind CSS** | Design system et mise en page responsive |
| **SNCF API** | Récupération des prochains départs en temps réel |
| **OSRM API** | Calcul d'itinéraires cyclables |

---

## 📂 Structure des Données

Le projet ingère et nettoie plusieurs sources de données hétérogènes :

* `gares2.json` : Référentiel des gares voyageurs.
* `entreprises-epv.json` : Entreprises du Patrimoine Vivant (Artisanat d'excellence).
* `etablissements-labellises...json` : Label d'état Qualité Tourisme™.
* `datatourisme-tour.csv` : Circuits et randonnées (Parsing CSV manuel).
* `france.geojson` : Tracés des aménagements cyclables.

---

## 💻 Installation & Usage

1. **Cloner le dépôt**
   ```bash
   git clone [https://github.com/ton-username/sncf-dataviz.git](https://github.com/Guewenn/sncf-dataviz.git)
   cd sncf-dataviz
