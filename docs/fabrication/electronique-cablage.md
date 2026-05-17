---
layout: default
title: 3. Électronique & Câblage
parent: Étapes de fabrication
nav_order: 3
---

# 3. Électronique & Câblage

Cette étape couvre le montage et le câblage de l'ensemble électronique de la machine.

---

## Étapes de montage

1. **Soudure des composants** sur le PCB sur-mesure
2. **Test des tensions** (12V entrée, 5V régulé)
3. **Connexion des drivers A4988** aux moteurs NEMA 17
4. **Câblage du servo-moteur** sur la broche PWM de l'ESP32
5. **Tests de fonctionnement** moteur par moteur

---

## Brochage ESP32-S3-UNO

| Broche | Connexion |
|---|---|
| GPIO (STEP/DIR) | Driver A4988 — Moteur X |
| GPIO (STEP/DIR) | Driver A4988 — Moteur Y |
| PWM | Servo-moteur stylo |
| 5V / GND | Alimentation logique |

---

## Difficultés rencontrées

*(✏️ Problèmes de câblage, courts-circuits, problèmes d'alimentation ?)*

---

*(✏️ Ajoute des photos du câblage et de la carte)*
