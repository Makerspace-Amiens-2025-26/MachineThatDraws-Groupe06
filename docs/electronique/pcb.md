---
layout: default
title: Routage du PCB
parent: Électronique & PCB
nav_order: 2
---

# Routage du PCB

Le PCB a été routé sous **KiCad 9**. Il regroupe tous les composants sur une carte sur-mesure adaptée à la machine.

---

## Choix de conception

- PCB **double couche** pour simplifier le routage des alimentations
- Séparation des plans d'alimentation (12V / 5V / GND)
- Connecteurs déportés pour les moteurs et le servo

---

## Dimensions et caractéristiques

| Paramètre | Valeur |
|---|---|
| Dimensions | *(à compléter)* mm × *(à compléter)* mm |
| Nombre de couches | 2 |
| Épaisseur cuivre | 1 oz |
| Épaisseur carte | 1.6 mm |

---

## Vue du routage

![Routage PCB KiCad]({{ site.baseurl }}/assets/images/pcb.png)

---

## Fichiers sources

Les fichiers KiCad sont disponibles dans le dossier `project/ECAD/` du dépôt :

<a href="https://github.com/Makerspace-Amiens-2025-26/MachineThatDraws-Groupe06" target="_blank" class="btn btn-outline">Voir sur GitHub ↗</a>
