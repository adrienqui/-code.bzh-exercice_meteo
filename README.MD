# Exercice Meteo

## Introduction

Suite à l'étape 1 on dispose d'un objet `meteo` dans `App.vue` contenant le resultat json de notre recherche réalisée par le composant `Recherche.vue`

## Afficher les données

1. Créé le fichier `components/Meteo.vue`
2. Ajouter le composant `Meteo.vue` dans `App.vue`
3. Dans `Meteo.vue` faire un encart donnant les informations contenu dans `meteo.city` de `App.vue` (utiliser `props`)
4. Toujours dans `Meteo.vue` faire la liste des prévisions météo à venir (`meteo.list`) et pour chaque prévision afficher la date, la température, le taux d'humidité ainsi qu'une description

> **Note** : Pour comprendre comment les données sont structuré dans `meteo` on pourra s'aider de la [documentation d'openweathermap](https://openweathermap.org/forecast5)

Quand le travail est fini passer à l'étape suivante
```
$ git checkout step-3
```
