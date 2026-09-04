# Design system détaillé

> Ce fichier est importé par `CLAUDE.md` via la ligne `@design-system.md`.
> Il est donc chargé au démarrage de chaque session, au même titre que le CLAUDE.md.
> Garde-le court : tout ce qui est ici consomme du contexte à chaque session.

## Couleurs

| Rôle | Valeur | Usage |
|---|---|---|
| primary | `#1a4d8f` | boutons principaux, liens, titres forts |
| accent | `#f59e0b` | un seul élément par écran, jamais deux |
| surface | `#f8fafc` | fond des cartes et des sections alternées |
| text | `#0f172a` | corps de texte |
| muted | `#64748b` | légendes, mentions, texte secondaire |

## Typographie

| Élément | Police | Taille | Graisse |
|---|---|---|---|
| Titre principal | Inter | 48px (32px mobile) | 700 |
| Titre de section | Inter | 32px (24px mobile) | 600 |
| Corps | Inter | 17px | 400 |
| Légende | Inter | 14px | 400 |

Hauteur de ligne : 1.6 pour le corps, 1.2 pour les titres.

## Espacements

Échelle de 8 : 8, 16, 24, 32, 48, 64, 96.
Padding vertical des sections : 96px en desktop, 48px en mobile.
Rayon des angles : 12px. Rayon des boutons : 8px.

## Composants

**Bouton principal** — fond `primary`, texte blanc, padding 12/24, rayon 8px.
Au survol : assombrir le fond de 10%. Pas d'animation de plus de 150ms.

**Carte** — fond `surface`, pas de bordure, ombre légère `0 1px 3px rgba(0,0,0,.08)`.

**Lien dans le texte** — couleur `primary`, souligné, souligné plus épais au survol.

## Ce que ce design system interdit

- Les dégradés, sauf sur le bloc d'en-tête.
- Plus de deux graisses de police sur une même page.
- Les ombres portées marquées.
