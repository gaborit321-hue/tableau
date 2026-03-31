# Le Tableau

Tableau de bord personnel — PWA mobile installable.

## Fichiers

```
index.html      → app principale
sw.js           → service worker (cache + mise à jour)
manifest.json   → config PWA (icône, nom, couleurs)
logo.png        → icône de l'app
```

## Déploiement sur GitHub Pages

1. Crée un repo GitHub (ex: `le-tableau`)
2. Upload les 4 fichiers : `index.html`, `sw.js`, `manifest.json`, `logo.png`
3. Va dans **Settings → Pages → Source → main / root**
4. Ton app est live sur `https://[ton-username].github.io/le-tableau/`

## Installer sur mobile (Chrome)

1. Ouvre l'URL sur Chrome mobile
2. Menu ⋮ → **Ajouter à l'écran d'accueil**
3. L'app s'installe comme une app native

## Mettre à jour l'app

Après chaque modification, incrémente la version dans `sw.js` :
```js
const VERSION = 'v2'; // v1 → v2 → v3 ...
```
Cela force Chrome à remplacer l'ancien cache.

## Fonctionnalités

- **Objectif du jour** — cap quotidien avec anneau de countdown
- **Planning** — programme journalier avec prochaine échéance en temps réel
- **Énergie** — niveau d'énergie 1→5 avec indicateur coloré
- **Le Code** — 5 piliers de discipline en lecture permanente
- **Citation du jour** — rotation Jack London / Peaky Blinders
- **7 jours** — historique consultable des 7 derniers jours
- Tout sauvegardé localement, remis à zéro chaque jour
