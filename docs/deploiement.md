# Déploiement

## Structure du dépôt

```text
.
├── index.html
├── cal.html
├── README.md
└── docs/
    ├── syllabus.md
    ├── calendrier.md
    └── deploiement.md
```

## Publication GitHub Pages

Le site peut être publié depuis la branche `main`, dossier racine.

Dans GitHub :

1. Aller dans `Settings`.
2. Ouvrir `Pages`.
3. Sélectionner `Deploy from a branch`.
4. Choisir la branche `main`.
5. Choisir le dossier `/root`.
6. Enregistrer.

Les pages attendues sont :

- `/index.html` pour le syllabus ;
- `/cal.html` pour le calendrier.

## Vérification locale

Depuis le dossier du projet :

```bash
python -m http.server 8000
```

Puis ouvrir :

```text
http://localhost:8000/index.html
http://localhost:8000/cal.html
```

## Points de vigilance

- Les fichiers sont autonomes : ne pas supprimer les blocs `<style>` et `<script>`.
- Les données pédagogiques sont dans les constantes JavaScript des pages.
- Les anciennes références institutionnelles ne doivent pas être réintroduites.
- Avant publication, vérifier les deux pages sur desktop et mobile.
