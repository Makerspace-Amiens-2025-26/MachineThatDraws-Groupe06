---
layout: default
title: 4. Tests & Mise au point
parent: Étapes de fabrication
nav_order: 4
---

# 4. Tests & Mise au point

Une fois la machine assemblée et câblée, nous avons validé le fonctionnement axe par axe avant de lancer les premiers tracés.

---

## Tests réalisés

| Test | Résultat | Observations |
|---|---|---|
| Alimentation 12V / 5V | ✅ / ❌ | *(✏️ à compléter)* |
| Mouvement axe X (aller-retour) | ✅ / ❌ | *(✏️ à compléter)* |
| Mouvement axe Y (aller-retour) | ✅ / ❌ | *(✏️ à compléter)* |
| Lever du stylo (M5) | ✅ / ❌ | *(✏️ à compléter)* |
| Baisser du stylo (M3) | ✅ / ❌ | *(✏️ à compléter)* |
| Tracé d'un carré G-code | ✅ / ❌ | *(✏️ à compléter)* |
| Précision sur 100 mm | ✅ / ❌ | *(✏️ ex : erreur de ±1 mm)* |

---

## Calibration

| Paramètre | Valeur mesurée | Valeur cible |
|---|---|---|
| Pas/mm axe X | *(✏️)* pas/mm | *(✏️ ex : 80 pas/mm)* |
| Pas/mm axe Y | *(✏️)* pas/mm | *(✏️ ex : 80 pas/mm)* |
| Vitesse max (G1) | *(✏️)* mm/min | *(✏️ ex : 3000 mm/min)* |
| Angle servo stylo levé | *(✏️)* ° | *(✏️ ex : 90°)* |
| Angle servo stylo baissé | *(✏️)* ° | *(✏️ ex : 50°)* |

> **Formule pas/mm :** `pas/mm = (pas_moteur × micro-pas) / (pas_courroie × dents_poulie)`
> Exemple pour GT2 20 dents, 1/16 micro-pas, NEMA 200 pas/tour : `(200 × 16) / (2 × 20) = 80 pas/mm`

---

## Résultats

*(✏️ Décris la qualité du premier tracé — trait régulier ? Dérive ? Saut de pas ?)*

---

## Photos et vidéos des tests

*(✏️ Ajoute ici des photos des premiers dessins réalisés et/ou une vidéo de la machine en fonctionnement)*
