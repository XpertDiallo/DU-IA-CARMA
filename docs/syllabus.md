# Documentation de la page syllabus

## Fichier source

La page syllabus est contenue dans `index.html`.

Elle est conçue comme une page statique autonome : la feuille de style, les données pédagogiques et le JavaScript de rendu sont inclus dans le même fichier.

## Objectif de la page

Présenter le contenu détaillé du DU IA Finance & Actuariat :

- structure par unités d'enseignement ;
- matières et volumes horaires ;
- programmes détaillés ;
- objectifs pédagogiques ;
- cas pratiques ;
- technologies et notions clés ;
- appel à candidature.

## Structure fonctionnelle

La page contient :

- un en-tête institutionnel CARMA ;
- un hero de présentation avec chiffres clés ;
- une navigation sticky par UE ;
- un champ de recherche ;
- des filtres par domaine ;
- des fiches de cours extensibles ;
- un bloc de contact candidature ;
- un pied de page CARMA.

## Unités d'enseignement documentées

- UE0 : Fondamentaux de Programmation.
- UE1 : Fondamentaux de l'Intelligence Artificielle.
- UE2 : IA Appliquée à la Finance.
- UE3 : IA Appliquée à l'Actuariat.
- UE4 : Big Data & Infrastructure Cloud.
- UE5 : Éthique, Réglementation & Gouvernance IA.
- UE6 : Projet de Fin de Diplôme.

## Données pédagogiques

Les contenus sont déclarés dans le tableau JavaScript `syllabus`.

Chaque UE contient :

- `id` : ancre de navigation ;
- `badge` : code UE ;
- `title` : titre de l'UE ;
- `period` : volume horaire et période ;
- `color` : classe visuelle ;
- `courses` : liste des matières.

Chaque matière contient :

- `title` ;
- `time` ;
- `categories` ;
- `description` ;
- `program` ;
- `outcomes` ;
- `case` ;
- `technologies`.

## Maintenance

Pour modifier une matière :

1. Ouvrir `index.html`.
2. Chercher `const syllabus = [`.
3. Modifier l'objet de la matière concernée.
4. Vérifier la page dans un navigateur.

Pour ajouter une matière :

1. Ajouter un nouvel objet dans le tableau `courses` de l'UE correspondante.
2. Renseigner au minimum `title`, `time`, `categories`, `description`, `program`, `outcomes` et `technologies`.

## Contrôles recommandés

Après modification :

- vérifier que la recherche fonctionne ;
- vérifier que les filtres affichent les bonnes matières ;
- vérifier que les liens d'ancrage UE0 à UE6 mènent aux bonnes sections ;
- rechercher toute ancienne référence institutionnelle avant publication.
