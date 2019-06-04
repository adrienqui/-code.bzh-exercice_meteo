# Exercice Meteo

## Introduction

Si l'installation à bien eu lieu on obtient un dossier meteo avec :

1. Un dossier `public/` correspondant au source non compilé
2. Un dossier `src/` correspondant au code source de notre application

Le dossier `src/` contient notre point d'entré principal, le fichier `main.js` dans lequel on retrouve notre instance de vue primaire qui charge le composant `App.vue`

> Noter l'usage du composant `components/HelloWorld.vue` dans `App.vue` ainsi que les avantages du format `.vue`, balise `template`, `import` etc.

## Créé le formulaire de recherche

1. Créé le fichier `components/Recherche.vue` sur le même principe que `components/HelloWorld.vue`
2. Ajouter le composant `Recherche.vue` dans `App.vue`
3. Dans `Recherche.vue` faire un formulaire de recherche (input text et submit) ou l'input submit est `disabled` tant que l'input text est vide
4. Au submit du formulaire, faire une méthode `recherche` qui interroge l'API  [OpenWeatherMap](https://openweathermap.org) sur un lieu (ex: Brest) et récupère les résultats au format JSON
5. Pour finir on fait remonter le resultat de notre recherche au composant parent `App.vue`

> **Note 1** : On s'inscrit sur openweathermap.org pour obtenir une clé d'API (https://home.openweathermap.org/api_keys) qu'on pourra stocker dans les data de `App.vue` puis transmettre à `Recherche.vue` avec un `props`

> **Note 2** : On utilise la fonction `fetch()`, qui retourne une `Promesse` et dont on traitera le resultat au format JSON avec la fonction `json()`

> **Note 3** : L'url appelé par `fetch()` sera la suivante `api.openweathermap.org/data/2.5/forecast?q={city name},{country code}` (voir la [documentation d'openweathermap](https://openweathermap.org/forecast5))

> **Note 4** : Pour faire remonter une information d'un composant enfant à un composant parent on utilisera la méthode `$emit`

Quand le travail est fini passer à l'étape suivante
```
$ git checkout step-2
```
