---
layout: default
title: Conversion G-code
parent: Fonctionnement des logiciels
nav_order: 3
---

# Conversion G-code

Avant d'envoyer un dessin à la machine, le fichier source doit être converti en une liste d'instructions G-code que le firmware peut interpréter.

---

## Processus de conversion

1. **Préparation du fichier source** — Dessin vectoriel (SVG) ou image bitmap (PNG, JPG)
2. **Vectorisation** — Si le fichier est une image bitmap, on le convertit d'abord en SVG
3. **Génération des trajectoires** — Le logiciel calcule l'ordre de parcours des contours
4. **Export G-code** — Fichier `.gcode` prêt à être envoyé en série à l'ESP32

---

## Outil utilisé

| Logiciel | Rôle | Plateforme |
|---|---|---|
| *(✏️ ex : Inkscape + extension Inkscape-to-GCode)* | Conversion SVG → G-code | PC |
| *(✏️ ex : svg2gcode)* | *(✏️)* | *(✏️)* |
| *(✏️ ex : Script Python maison)* | *(✏️)* | *(✏️)* |

*(✏️ Décris précisément comment vous préparez un fichier — les réglages utilisés, les unités, les dimensions.)*

---

## Exemple de G-code généré

```gcode
G0 X0 Y0         ; Aller à l'origine
M3               ; Baisser le stylo
G1 X50 Y0 F800   ; Ligne horizontale 50 mm
G1 X50 Y50       ; Ligne verticale 50 mm
G1 X0 Y50        ; Ligne horizontale retour
G1 X0 Y0         ; Fermer le carré
M5               ; Lever le stylo
G0 X0 Y0         ; Retour origine
```

---

## Paramètres importants à régler dans le logiciel

| Paramètre | Valeur conseillée |
|---|---|
| Unités | mm |
| Vitesse d'avance (F) | *(✏️ ex : 800 mm/min)* |
| Profondeur de passe | N/A (axe Z = servo) |
| Commande stylo baissé | `M3` |
| Commande stylo levé | `M5` |

---

## Résultats obtenus

*(✏️ Montre des exemples de dessins produits par la machine — photos des tracés sur papier)*
