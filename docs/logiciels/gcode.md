---
layout: default
title: Conversion G-code
parent: Fonctionnement des logiciels
nav_order: 3
---

# Conversion G-code

Cette étape transforme un fichier image ou vectoriel en une liste d'instructions de mouvement (G-code) que la machine peut exécuter.

---

## Processus de conversion

1. **Préparation de l'image** — Vectorisation ou conversion SVG
2. **Génération des trajectoires** — Calcul des chemins de déplacement
3. **Export G-code** — Fichier `.gcode` prêt à envoyer

---

## Outil utilisé

*(✏️ Quel logiciel utilisez-vous pour convertir les fichiers ? Inkscape, svg2gcode, un script Python... Décris le process.)*

---

## Exemple de G-code généré

```gcode
G0 X0 Y0       ; Aller à l'origine
M3             ; Baisser le stylo
G1 X50 Y0 F500 ; Tracer une ligne horizontale de 50mm
G1 X50 Y50     ; Tracer une ligne verticale de 50mm
M5             ; Lever le stylo
G0 X0 Y0       ; Retour origine
```

---

*(✏️ Ajoute des exemples de fichiers et des captures des résultats obtenus.)*
