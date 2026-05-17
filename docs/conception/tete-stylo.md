---
layout: default
title: Tête porte-stylo
parent: Conception CAO
nav_order: 4
---

# Tête porte-stylo

La tête porte-stylo est la pièce terminale de la machine. Elle est fixée sur le chariot X et embarque le servo-moteur qui contrôle le contact du stylo avec le papier.

---

## Vue CAO

*(✏️ Ajoute une capture OnShape de la tête porte-stylo — vue éclatée si possible)*

---

## Fonctionnement

Le servo-moteur reçoit un signal PWM de l'ESP32. Deux angles sont programmés :

| Position | Angle servo | Commande G-code |
|---|---|---|
| Stylo levé | *(✏️ ex : 90°)* | `M5` |
| Stylo baissé | *(✏️ ex : 50°)* | `M3` |

---

## Conception

*(✏️ Comment le stylo est-il maintenu ? Clip, serrage, manchon imprimé ? Comment le bras du servo transmet-il le mouvement au stylo ?)*

---

## Pièces CAO

| Pièce | Matériau | Description |
|---|---|---|
| Corps de la tête | *(✏️ PETG)* | *(✏️ Support principal, fixation sur chariot X)* |
| Bras servo | *(✏️ PLA)* | *(✏️ Convertit la rotation du servo en translation du stylo)* |
| Manchon stylo | *(✏️ PLA)* | *(✏️ Maintien du stylo — adapté au diamètre utilisé)* |

---

## Compatibilité

*(✏️ Quels types de stylos ou feutres peuvent être utilisés ? Ø du manchon ? Poids maximal supporté ?)*

---

## Photos

*(✏️ Ajoute des photos de la tête assemblée et du stylo en position haute/basse)*
