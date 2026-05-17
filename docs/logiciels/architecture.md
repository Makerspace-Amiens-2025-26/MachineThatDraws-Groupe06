---
layout: default
title: Architecture logicielle
parent: Fonctionnement des logiciels
nav_order: 1
---

# Architecture logicielle

La chaîne logicielle de la MachineThatDraw se décompose en deux grandes parties : la **génération du G-code** côté PC, et l'**interprétation** côté microcontrôleur.

---

## Flux de données

```
[PC]
  1. Fichier image ou vectoriel (SVG, PNG...)
  2. Logiciel de conversion → fichier G-code (.gcode)
  3. Envoi série (USB) vers l'ESP32

[ESP32]
  4. Réception du G-code
  5. Interprétation des commandes (G0, G1, M3, M5...)
  6. Génération des signaux STEP/DIR vers les A4988
  7. Les moteurs NEMA 17 déplacent la tête

[Mécanique]
  8. Le stylo trace le dessin sur la feuille
```

---

## Logiciels utilisés

| Outil | Rôle | Type |
|---|---|---|
| *(✏️)* | Conversion image → G-code | PC |
| Arduino IDE / PlatformIO | Développement firmware | PC |
| Terminal série | Envoi G-code | PC |

---

*(✏️ Décris en détail les logiciels que vous utilisez pour préparer les fichiers.)*
