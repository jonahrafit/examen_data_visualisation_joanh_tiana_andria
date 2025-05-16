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
4. Maintenance imprévisible	Timeline + scatter plot	Fréquence des pannes vs calendrier
5. Insatisfaction client	Word cloud ou gauge chart	Analyse des retours clients
6. Itinéraires sous-optimaux	Carte interactive avec flux (geoJSON)	Visualisation des trajets + alternatives
7. Émissions CO₂ élevées	Bubble chart ou diagramme radar	Émissions par véhicule/type de ligne

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

## Maintenance imprévisible
🔍 Ce qu’il faut  
✅ Source
Nombre de pannes, historique des réparations
- Cahier de maintenance - Atelier mécanique interne  
📋 Comment les obtenir
- Demander au responsable technique les rapports de panne ou entretien ?  
💡 Astuce
Suggérer à l’entreprise de tenir un tableau Excel à remplir chaque semaine (bon
pour eux aussi)

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

## Itinéraires sous-optimaux🔍 Ce qu’il faut
✅ Source  
Distance réelle vs distance optimale  
- Cartographie des trajets (Google Maps, OpenStreetMap) - Tracés GPS si
disponibles  
📋 Comment les obtenir - Comparer les itinéraires parcourus à la carte - Observer si des détours inutiles ? sont faits
💡 Astuce  
Utiliser Google Maps pour simuler le chemin le plus court et comparer avec le trajet
réel observé  

## Émissions CO₂ élevées
🔍 Ce qu’il faut  
✅ Source  
Volume de carburant utilisé × coefficient CO₂
- Données de consommation (voir #2)  
📋 Comment les obtenir ? - Utiliser la formule : 1L essence ≈ 2,68 kg CO₂ 1L gasoil ≈ 2,64 kg CO₂  
💡 Astuce Tu n’as besoin que de la consommation pour estimer les émissions  

# Proposition de graphiques modernes adaptés à vos 7 problèmes
| Problème                  | Graphique moderne / interactif      | Pourquoi / usage principal                                  |
|---------------------------|-----------------------------------|------------------------------------------------------------|
| 1. Retards fréquents      | Calendar Heatmap                  | Voir la fréquence des retards jour par jour sur un calendrier |
| 2. Coûts de carburant élevés | Multi-line Chart                | Comparer l’évolution du carburant par ligne dans le temps   |
| 3. Taux d’occupation faible | Stacked Bar Chart               | Visualiser proportions des niveaux de remplissage par ligne |
| 4. Maintenance imprévisible | Timeline + Force-Directed Graph | Visualiser pannes dans le temps + relations entre types de pannes |
| 5. Insatisfaction client  | Word Cloud                       | Visualiser mots clés / types de plaintes fréquentes         |
| 6. Itinéraires sous-optimaux | Sankey Diagram                | Visualiser flux des trajets et alternatives entre arrêts    |
| 7. Émissions CO₂ élevées  | Treemap ou Radial Bar Chart      | Montrer les émissions par ligne ou bus avec tailles relatives |
