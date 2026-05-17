---
layout: default
title: Liste des composants
parent: Électronique & PCB
nav_order: 3
---

# Liste des composants (BOM)

Liste complète des composants utilisés sur le PCB de la MachineThatDraw.

---

## Tableau des composants

| Référence | Composant | Valeur / Modèle | Quantité |
|---|---|---|---|
| U1 | Microcontrôleur | ESP32-S3-UNO | 1 |
| A1, A2 | Driver moteur | A4988 | 2 |
| U2 | Régulateur DC/DC | R-78E5.0-1.0 | 1 |
| J1 | Connecteur alim. | Barrel Jack Switch | 1 |
| J2, J3 | Connecteur moteur | Conn_01x04 | 2 |
| C1, C2 | Condensateur | 10µF, 100µF | 2 |
| M1 | Servo-moteur | SG90 / MG90S | 1 |

---

## Connexions

| Référence | Broche | Connecté à |
|---|---|---|
| U1 | GPIO STEP/DIR | A4988 #1 (Moteur X) |
| U1 | GPIO STEP/DIR | A4988 #2 (Moteur Y) |
| U1 | PWM | Servo-moteur |
| A1/A2 | VMOT | 12V (J1) |
| A1/A2 | VDD | 5V (U2) |
| U2 | Vin | 12V (J1) |
| U2 | Vout | 5V → U1, A1, A2 |
