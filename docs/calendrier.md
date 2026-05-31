# Documentation de la page calendrier

## Fichier source

La page calendrier est contenue dans `cal.html`.

Elle est conçue comme une page statique autonome : styles, scripts et données calendaires sont intégrés directement dans le fichier HTML.

## Objectif de la page

Présenter le planning pédagogique complet de la promotion 2026-2027 :

- cours du soir ;
- rendus de projets ;
- suivis et soutenances ;
- jours fériés ;
- vacances ;
- navigation mensuelle.

## Structure fonctionnelle

La page contient :

- un en-tête institutionnel CARMA ;
- un hero avec informations pratiques ;
- un bloc de prochains jalons ;
- une navigation sticky par mois ;
- un champ de recherche ;
- des filtres par UE et par type d'événement ;
- une légende de couleurs ;
- des calendriers mensuels générés en JavaScript ;
- un panneau de détail cliquable par journée ;
- un pied de page CARMA.

## Période couverte

Le calendrier couvre :

- octobre 2026 ;
- novembre 2026 ;
- décembre 2026 ;
- janvier 2027 ;
- février 2027 ;
- mars 2027 ;
- avril 2027 ;
- mai 2027 ;
- juin 2027.

## Données intégrées

Les données principales sont déclarées dans trois constantes JavaScript :

- `months` : liste des mois affichés.
- `eventSource` : événements pédagogiques.
- `specialSource` : jours fériés et vacances.

Le fichier contient :

- 163 événements pédagogiques ;
- 8 éléments spéciaux de calendrier.

## Format des événements

Chaque ligne de `eventSource` suit le format :

```text
YYYY-MM-DD|type|badge|titre|intervenant|horaire|liens
```

Exemple :

```text
2026-10-05|python|UE0|Python pour la Data Science|Prof. Python|18h30-21h|Rejoindre,Replay
```

## Format des éléments spéciaux

Chaque ligne de `specialSource` suit le format :

```text
YYYY-MM-DD|type|titre
```

Exemple :

```text
2026-11-01|ferie|Toussaint
```

Les vacances de Noël sont étendues automatiquement par le JavaScript pour couvrir la période affichée.

## Maintenance

Pour ajouter un cours :

1. Ouvrir `cal.html`.
2. Chercher `const eventSource`.
3. Ajouter une ligne au format attendu.
4. Vérifier le rendu du mois concerné.

Pour ajouter un jour férié :

1. Chercher `const specialSource`.
2. Ajouter une ligne `YYYY-MM-DD|ferie|Nom`.

Pour ajouter un mois :

1. Ajouter le mois dans `months`.
2. Ajouter les événements correspondants dans `eventSource`.

## Contrôles recommandés

Après modification :

- vérifier le comptage d'événements affiché ;
- tester la recherche ;
- tester les filtres UE0 à UE5, Rendus et Fériés ;
- cliquer sur une journée avec événement pour vérifier le panneau de détail ;
- vérifier l'affichage mobile grâce au défilement horizontal des tableaux.
