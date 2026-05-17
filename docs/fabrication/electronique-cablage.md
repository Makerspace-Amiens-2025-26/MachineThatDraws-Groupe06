---
layout: default
title: 3. Électronique & Câblage
parent: Étapes de fabrication
nav_order: 3
---

# 3. Électronique & Câblage

Cette étape couvre la soudure des composants sur le PCB et le câblage complet de la machine.

---

## Étapes de montage

1. **Soudure des composants** sur le PCB — résistances, condensateurs, connecteurs
2. **Test des tensions** avant connexion : 12 V en entrée, 5 V en sortie du régulateur R-78E
3. **Réglage du courant des A4988** — potentiomètre Vref selon le courant nominal des NEMA 17
4. **Connexion des drivers A4988** aux moteurs via les connecteurs déportés
5. **Câblage du servo-moteur** sur la broche PWM de l'ESP32
6. **Upload du firmware** et test axe par axe

---

## Brochage ESP32-S3-UNO

| Signal | Broche ESP32 | Connecté à |
|---|---|---|
| STEP moteur X | *(✏️ ex : GPIO 14)* | A4988 #1 — STEP |
| DIR moteur X | *(✏️ ex : GPIO 13)* | A4988 #1 — DIR |
| STEP moteur Y | *(✏️ ex : GPIO 27)* | A4988 #2 — STEP |
| DIR moteur Y | *(✏️ ex : GPIO 26)* | A4988 #2 — DIR |
| PWM servo | *(✏️ ex : GPIO 12)* | Servo-moteur signal |
| 5V | 5V | VDD des A4988, servo |
| GND | GND | Masse commune |

---

## Réglage du courant A4988

Le courant de phase des NEMA 17 est ajusté via la tension Vref sur le potentiomètre de chaque driver.

| Paramètre | Valeur |
|---|---|
| Courant nominal NEMA 17 | *(✏️ ex : 1.2 A)* |
| Vref visée | *(✏️ ex : 0.6 V pour 1.2 A)* |
| Formule | Vref = I_max × 8 × R_sense |

---

## Difficultés rencontrées

*(✏️ Courts-circuits, mauvaise soudure, A4988 qui chauffe, moteur qui vibre sans bouger ?)*

---

## Photos du câblage

*(✏️ Ajoute des photos du PCB soudé et du câblage final)*
