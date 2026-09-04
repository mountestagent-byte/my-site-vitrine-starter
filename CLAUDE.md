# Site vitrine — instructions du projet

Ce fichier est lu par Claude Code au début de **chaque** session.
C'est la mémoire du projet. Tout ce qui est écrit ici, tu n'auras pas à le répéter.

## Le projet

Un site vitrine d'une seule page, statique, pour présenter mon activité.
Il est publié sur GitHub Pages depuis la branche `main`, dossier racine.

- Public visé : dirigeants de petites entreprises qui veulent clarifier leur stratégie numérique
- Ce que le visiteur doit faire en arrivant : demander un rendez-vous de découverte
- Ton de voix : direct, chaleureux et rassurant

## Fichiers du dépôt

- `index.html` — le site. Seul fichier livré.
- `CLAUDE.md` + `design-system.md` — le contexte, chargés à chaque session.
- `assets/` — la marque (falcon or/cream/ink, lockup navy) et les images du site.
- `README.md`, `PROMPTS.md`, `BONUS.md` — matériel de l'atelier. À ne pas modifier
  et à ne pas traiter comme des specs produit.

## Commandes

Pas de build, pas de dépendances, pas de tests. Le site est du HTML statique servi tel quel.

- Prévisualiser : `open index.html` (ou `python3 -m http.server 8000` pour tester les ancres)
- Publier : commit + push sur `main`. GitHub Pages sert la racine, en ligne ~2 min plus tard.

## Design system

La source unique est @design-system.md — *RA Consulting, Brand Guidelines v1*.
Le résumé ci-dessous sert de garde-fou ; en cas d'écart, le fichier détaillé fait foi.

- **Fond** : midnight `#071426` par défaut, `#050F1D` pour les sections en creux.
  Les sections alternent entre les deux, séparées par une règle de 1px.
- **Accent** : l'or, et rien d'autre. `#BE9B48` sur midnight, `#E8C868` pour le texte
  accentué. **Une seule pastille or pleine par vue** ; tout le reste s'accentue en
  hairline or ou en texte or.
- **Texte** : cream `#FBF9F4`, secondaire à 72 %. Aucun gris neutre dans ce système.
- **Polices** : Instrument Serif (titres, tracking −0.02em), Geist (corps, 16px/1.6,
  mesure 64ch), Space Mono (eyebrows et labels, 11px, majuscules, 0.16em).
- **Rythme de section** : eyebrow mono → titre serif → standfirst Geist 300 → règle
  hairline → corps. Cet ordre, dans chaque section.
- **Espacement** : base 4 avec pas de 2 — 2 · 4 · 8 · 12 · 16 · 20 · 24 · 32 · 40 · 48 ·
  64 · 80 · 112 · 160. Padding de carte 24, gap de grille 24, rythme de section 112,
  container 1240, gouttière 64.
- **Rayons** : 2 · 3 (contrôles) · 6 · 10 (cartes) · 16.
- **Style** : sobre et instrumenté — petits rayons, hairlines, presque pas de
  profondeur. **Aucune ombre sur midnight**, la hairline fait le travail.
- **Interdits** : les emoji, un deuxième jeu d'icônes (Lucide 1.5px uniquement), tout
  dégradé hors des trois dégradés signature, le Title Case, les points d'exclamation.

> Si un `<!-- REMPLIS -->` de ce fichier est encore vide, demande-moi l'information
> avant d'écrire du contenu. N'invente pas.

## Règles de fabrication

- Un seul fichier `index.html`, CSS inclus dans une balise `<style>`. Pas de framework, pas de build.
- Pas de dépendance externe, sauf Google Fonts si le design system demande une police.
- Mobile, à vérifier en largeur 375px : aucun débordement horizontal, aucun texte
  sous 15px, zones cliquables (liens, boutons) d'au moins 44px de haut.
- Contraste : au moins 4.5:1 pour le corps de texte, au moins 3:1 pour les titres
  de 24px ou plus.
- Les images vont dans `assets/`, jamais ailleurs, et rien d'autre que des images.
- La marque : `assets/logo-mark-gold.png` sur midnight, `-cream` sur fond sombre,
  `-ink` sur papier. Une seule marque par surface, jamais sous 24px de haut,
  avec une marge libre de 0.5× sa hauteur.
- Chaque section du site a un `id` en minuscules, utilisable comme ancre.

## Ce que je ne veux pas

- Pas de faux témoignages, pas de faux logos clients, pas de chiffres inventés.
  Si une information manque, laisse un placeholder visible en majuscules.
- Pas de bandeau cookies, pas de popup, pas de compte à rebours.
- Pas de lorem ipsum : écris du vrai texte à partir de ce que je t'ai dit,
  ou laisse un placeholder explicite.

## Vérifier avant de dire que c'est fini

- La page s'ouvre sans erreur dans la console du navigateur.
- Les couleurs, polices et espacements viennent bien de `design-system.md`.
- Aucun placeholder oublié dans le rendu final.
