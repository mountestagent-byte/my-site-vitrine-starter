# Les prompts de l'atelier

Copie-les un par un. Ne saute pas d'étape : chaque itération s'appuie sur la précédente.

---

## Avant tout — vérifier que le contexte est chargé

Tape dans Claude Code :

```
/context
```

Sous **Memory files**, tu dois voir `CLAUDE.md`. S'il n'y est pas, Claude ne le lit pas,
et tout le reste sera générique. Corrige avant de continuer.

---

## Itération 1 — le prompt fondateur

```
Lis CLAUDE.md et design-system.md, puis remplace index.html par la page
d'accueil de mon activité.

Structure : en-tête avec mon nom et ma promesse en une phrase, section
"ce que je fais" en trois blocs, section "pour qui", section "me contacter".

Applique strictement le design system : les couleurs, les polices et
l'échelle d'espacement viennent de là, pas de tes préférences.

Écris le contenu à partir des informations du CLAUDE.md. Pour tout ce qui
manque, mets un placeholder en majuscules entre crochets.
```

Ouvre ensuite `index.html` dans ton navigateur. Regarde. Ne corrige rien encore.

---

## Itération 2 — la critique

C'est l'étape que tout le monde saute, et c'est celle qui change tout.

```
Regarde le rendu avec un œil critique et dis-moi les trois choses les plus
faibles de cette page, du point de vue d'un visiteur qui la découvre en
5 secondes. Ne corrige rien pour l'instant, propose seulement.
```

Choisis ce que tu retiens, puis :

```
Applique les points 1 et 3. Laisse le 2 de côté.
```

---

## Itération 3 — le mobile et la finition

```
Passe la page en revue en largeur 375px : rien ne doit déborder, aucun
texte ne doit descendre sous 15px, les zones cliquables font au moins 44px
de haut. Corrige ce qui ne va pas.
```

---

## Le contexte qui manquait

Quand une correction revient une deuxième fois, elle n'a rien à faire dans le chat :
elle doit aller dans le `CLAUDE.md`.

```
Ajoute cette règle à CLAUDE.md pour que tu la respectes dans toutes les
sessions à venir : [ta règle]
```

C'est ça, le context engineering. Rien de plus.

---

## Mise en ligne

```
Fais un commit de tout le travail avec un message clair, puis pousse sur main.
```

Puis, sur GitHub : **Settings → Pages → Source : Deploy from a branch → main / (root) → Save**.
Deux minutes plus tard, ton site est en ligne à l'adresse affichée sur cette même page.

---

## Le filet de sécurité

Si une itération casse tout :

```
/rewind
```

Ça ramène le code **et** la conversation au point de contrôle précédent.
Personne ne perd son travail dans cet atelier.
