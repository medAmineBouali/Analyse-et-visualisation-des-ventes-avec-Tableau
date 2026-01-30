# 📊 Dashboard d’Analyse de la Répartition des Ventes (Tableau)

## 📋 Présentation du Projet

Ce projet consiste en la création d'un outil d'aide à la décision interactif permettant d'analyser les performances commerciales d'une entreprise. L'objectif est de transformer des données brutes (ventes, retours, satisfaction client) en insights exploitables pour piloter la stratégie commerciale.

### 🔑 Indicateurs Clés (KPIs) :

* **Commandes totales :** 7 859
* **Montant total des ventes :** 2 312 514,08 
* **Focus Géographique :** Europe (Allemagne, France, Italie, etc.)

---

## 🏗️ Architecture des Données

### Sources de données

Le projet s'appuie sur quatre tables principales : **Achats, Évaluations, Retours** et **Personnes**.

### Logique de préparation (Modélisation)

Pour garantir l'intégrité des données et la précision des calculs, la structure suivante a été mise en place :

* **Jointures physiques (LEFT JOIN) :** Entre les *Achats* et les *Évaluations/Retours* pour conserver l'historique complet des ventes, même sans retour ou évaluation.
* **Jointure interne (INNER JOIN) :** Entre les *Achats* et les *Personnes* pour l'affectation géographique.
* **Relation Logique :** Utilisée entre les *Achats* et les *Évaluations* pour maintenir la granularité au niveau de la commande et éviter les doublons lors des agrégations (ex: moyenne de satisfaction).

---

## 💡 Fonctionnalités Avancées & Calculs

Le dashboard intègre des calculs complexes pour enrichir l'analyse :

* **Calcul de ROI :** Analyse du pourcentage de profit par rapport au montant des ventes.
* **Éco-taxe Dynamique :** Champ conditionnel appliquant une taxe de 5 % sur la catégorie "Technologie", excluant les produits identifiés comme "Recyclés".
* **Simulation de Croissance :** Utilisation d'un **Paramètre** (`% accroissement profit`) permettant à l'utilisateur de simuler un profit ajusté en temps réel.
* **Hiérarchies Interactives :** Navigation fluide du pays vers la ville, et de la catégorie de produit vers l'article précis.

---

## 🎮 Instructions d'Utilisation

1. **Exploration Géographique :** Utilisez la carte interactive pour identifier les zones de profit. La taille des bulles représente le volume de ventes et la couleur indique la rentabilité (ROI).
2. **Filtrage Contextuel :** Les filtres à droite permettent de segmenter les données par **Date (Trimestre)**, **Pays**, **Région** et **Segment de clientèle**.
3. **Analyse des Tendances :** Le graphique "Targets and Forecasts" permet de comparer les ventes réelles par rapport à la moyenne cible de 24 000 $.

---

## 📁 Contenu du Dépôt

Tous les fichiers sont fournis au format **.twbx** (Packaged Workbook) incluant les sources de données :

* `Dashboard.twbx` : Le tableau de bord final interactif.
* `Visualisations_de_base.twbx` : Analyse exploratoire initiale.
* `Visualisations_avancées_interactivité.twbx` : Graphiques complexes et paramètres.
* `Tableaux_Reporting.twbx` : Rapports détaillés et mise en forme conditionnelle.
