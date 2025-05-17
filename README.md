# 🎯 Objectif du projet
Visualiser et analyser les données de l’entreprise fictive TransMada afin d’identifier et corriger 7 problèmes majeurs à l’aide de la Data Visualisation et de D3.js.

## 🧩 Étapes principales
1. Slide de présentation (structure recommandée en 8-10 slides)
Slide	Contenu
1. Introduction	Présentation de l’entreprise fictive TransMada et objectif du projet
2. Problèmes identifiés	Liste des 7 problèmes avec icônes/illustrations
3. Objectifs de la data visualisation	Pourquoi et comment on va visualiser ces problèmes
4. Jeux de données	Source, type (temps, géographique, qualitatif), structure (format JSON/CSV)
5-11. Visualisations	Une slide par problème avec un graphique D3.js + une analyse
12. Synthèse	Résumé des insights et recommandations
13. Conclusion	Impact de la data viz + suites possibles

##  📊 Idées de graphiques D3.js pour chaque problème
Problème	Type de graphique (D3.js)	Description
1. Retards fréquents	Bar chart ou heatmap temporelle	Retards par heure, jour ou ligne
2. Coûts de carburant élevés	Line chart ou area chart	Évolution du coût par mois/trajet
3. Taux d’occupation faible	Donut chart ou histogramme	Répartition du taux par ligne ou bus
4. Insatisfaction client	Word cloud ou gauge chart	Analyse des retours clients
5. Analyse des pannes par météo
6. Analyse de la demande par type de véhicule

# Comment obtenir les données réelles dans un cas concret ?
## Retards fréquents
🔍 Ce qu’il faut Heure de départ prévue vs réelle  
✅ Source - Registre manuel des chauffeurs - Application GPS si disponible - Planning
hebdomadaire des trajets  
📋 Comment les obtenir ?  
Demander à l'entreprise les fiches horaires  
Installer une app GPS simple sur quelques trajets tests  
💡 Astuce Même sans app, tu peux faire un relevé manuel pendant 3 jours avec des étudiants
bénévoles

## Coût du carburant élevé
🔍 Ce qu’il faut Carburant consommé par trajet  
✅ Source - Factures carburant - Carnet de bord des chauffeurs  
📋 Comment les obtenir ?  
- Demander les tickets de station-service
- Interroger les chauffeurs (ou chefs de
ligne)
💡 Astuce Comparer consommation selon la distance et le remplissage (efficience)

## Taux d’occupation faible
🔍 Ce qu’il faut
Nombre de passagers vs capacité  
✅ Source
- Observations manuelles - Ticketing si automatisé (rare à Mada)  
📋 Comment les obtenir ?   - Faire un relevé par ligne et par tranche horaire (ex. matin vs soir)
Utiliser un formulaire Google simple sur smartphone pour noter à chaque arrêt
💡 Astuce



## Insatisfaction des clients
🔍 Ce qu’il faut  
✅ Source
Nombre de plaintes, motifs, évaluations  
- Réseaux sociaux (commentaires) - Enquêtes auprès des usagers  
📋 Comment les obtenir
- Distribuer un petit questionnaire papier ou Google Form à bord ou à l'arrêt ?   
💡 Astuce  
Demander des évaluations de 1 à 5 sur : ponctualité, confort, comportement
chauffeur, propreté  

## 🚧 Analyse des pannes par météo
🔍 Ce qu’il faut
Pannes signalées (Oui / Non)

Conditions météo (pluie, ensoleillé, orage, température…)

Date des trajets

✅ Source
Historique des pannes (rapports de maintenance)

Données météo journalières (API météo comme OpenWeather, WeatherAPI, ou relevés locaux)

Planning des trajets (pour croiser les dates)

📋 Comment les obtenir ?
Associer chaque trajet à la météo du jour (via une API météo par date et localisation)

Ajouter une colonne Météo (pluie, soleil, etc.) et Température dans les données

Filtrer tous les trajets avec Panne = Oui puis analyser par météo

💡 Astuce
Pour une première analyse, utilisez simplement la date et une ville centrale (ex: Tana) pour récupérer la météo quotidienne.

Si plusieurs lignes couvrent des zones éloignées, affinez par localisation GPS (si disponible).

## 🚐 Analyse de la demande par type de véhicule
🔍 Ce qu’il faut
Nombre de passagers par trajet

Capacité du véhicule

Type de véhicule (catégorie : 5, 7, 9, +9 places)

Taux de remplissage (%)

✅ Source
Fiches journalières de trajets

Base de données des véhicules (modèle, capacité)

Historique de location ou de réservation si disponible

📋 Comment les obtenir ?
Ajouter une colonne Catégorie_Véhicule selon la capacité (ex: 5 places → “petit”, >9 → “grand”)

Regrouper les trajets par Catégorie_Véhicule et calculer la demande (passagers, trajets, taux de remplissage)

Croiser avec les jours de la semaine ou les lignes pour détecter des préférences

💡 Astuce
Utilisez des couleurs ou des formes différentes pour visualiser les préférences par catégorie dans un bar chart groupé

Si certaines catégories sont très peu utilisées, envisagez de les redéployer ou de les vendre



# Proposition de graphiques modernes adaptés à vos 6 problèmes
| Problème                  | Graphique moderne / interactif      | Pourquoi / usage principal                                  |
|---------------------------|-----------------------------------|------------------------------------------------------------|
| 1. Retards fréquents      | Calendar Heatmap                  | Voir la fréquence des retards jour par jour sur un calendrier |
| 2. Coûts de carburant élevés | Multi-line Chart                | Comparer l’évolution du carburant par ligne dans le temps   |
| 3. Taux d’occupation faible | Stacked Bar Chart               | Visualiser proportions des niveaux de remplissage par ligne ||
| 4. Insatisfaction client  | Word Cloud                       | Visualiser mots clés / types de plaintes fréquentes         |
|5. Analyse des pannes par météo | 	Scatter Plot + Color Map          | Étudier la corrélation entre météo (pluie, chaleur...) et pannes par véhicule ou par ligne     |
| 6. Analyse de la demande par type de véhicule | Grouped Bar Chart     | Comparer la demande client selon les types de véhicules (5, 7, 9, +9 places) |
