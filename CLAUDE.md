# Site vitrine — instructions du projet

Ce fichier est lu par Claude Code au début de **chaque** session.
C'est la mémoire du projet. Tout ce qui est écrit ici, tu n'auras pas à le répéter.

## Le projet

Un site vitrine d'une seule page, statique, pour présenter mon activité.
Il est publié sur GitHub Pages depuis la branche `main`, dossier racine.

- Public visé : <!-- REMPLIS : à qui s'adresse ce site ? -->
- Ce que le visiteur doit faire en arrivant : <!-- REMPLIS : me contacter ? prendre RDV ? -->
- Ton de voix : <!-- REMPLIS : sobre et institutionnel / direct et chaleureux / technique -->

## Design system

<!--
  ⬇️ C'EST LE BLOC LE PLUS IMPORTANT DU FICHIER.
  Recopie ici les valeurs de TON design system créé dans Claude Design.
  Claude Code cherche cette section avant de choisir ses propres couleurs :
  ton design system passe avant ses préférences, et ton prompt passe avant les deux.
  Remplace chaque valeur d'exemple. Ne laisse aucun placeholder.
-->

- Colors: primary `#1a4d8f`, accent `#f59e0b`, surface `#f8fafc`, text `#0f172a`
- Typography: Inter for body, Inter for headings
- Spacing: 8px scale, 12px border radius
- Style: <!-- REMPLIS : anguleux ou arrondi, dense ou aéré, plat ou avec ombres -->

Pour la version détaillée (composants, états, tons secondaires) : @design-system.md

## Règles de fabrication

- Un seul fichier `index.html`, CSS inclus dans une balise `<style>`. Pas de framework, pas de build.
- Pas de dépendance externe, sauf Google Fonts si le design system demande une police.
- Le site doit être lisible sur mobile : teste toujours en largeur 375px.
- Contraste minimum AA sur tous les textes.
- Les images vont dans `assets/`, jamais ailleurs.
- Chaque section du site a un `id` en minuscules, utilisable comme ancre.

## Ce que je ne veux pas

- Pas de faux témoignages, pas de faux logos clients, pas de chiffres inventés.
  Si une information manque, laisse un placeholder visible en majuscules.
- Pas de bandeau cookies, pas de popup, pas de compte à rebours.
- Pas de lorem ipsum : écris du vrai texte à partir de ce que je t'ai dit,
  ou laisse un placeholder explicite.

## Vérifier avant de dire que c'est fini

- La page s'ouvre sans erreur dans la console du navigateur.
- Les couleurs utilisées sont bien celles du design system ci-dessus.
- Aucun placeholder oublié dans le rendu final.
