---
layout: default
title: Firmware ESP32
parent: Fonctionnement des logiciels
nav_order: 2
---

# Firmware ESP32

Le firmware tourne sur l'ESP32-S3-UNO et interprète les commandes G-code reçues en série pour piloter les deux drivers A4988 et le servo.

---

## Commandes G-code supportées

| Commande | Action |
|---|---|
| `G0 X__ Y__` | Déplacement rapide sans tracé (stylo levé) |
| `G1 X__ Y__ F__` | Déplacement avec tracé (stylo baissé) |
| `M3` | Baisser le stylo |
| `M5` | Lever le stylo |
| `G28` | *(✏️ Retour à l'origine — si implémenté)* |

---

## Code principal

```cpp
// Machine That Draw — Groupe 06
// Makerspace Amiens 2025-2026

#include <Stepper.h>
#include <Servo.h>

const int STEPS = 200;
Stepper motorX(STEPS, 8, 9, 10, 11);
Stepper motorY(STEPS, 4, 5, 6, 7);
Servo penServo;

void setup() {
  Serial.begin(115200);
  motorX.setSpeed(60);
  motorY.setSpeed(60);
  penServo.attach(12);
  penServo.write(90); // Stylo levé
}

void loop() {
  if (Serial.available()) {
    String cmd = Serial.readStringUntil('\n');
    parseGCode(cmd);
  }
}
```

*(✏️ Ajoute ici la fonction `parseGCode()` avec votre implémentation réelle)*

---

## Paramètres de calibration

| Paramètre | Valeur |
|---|---|
| Pas/mm axe X | *(✏️ ex : 80 pas/mm)* |
| Pas/mm axe Y | *(✏️ ex : 80 pas/mm)* |
| Vitesse déplacement rapide (G0) | *(✏️ ex : 5000 mm/min)* |
| Vitesse tracé (G1) | *(✏️ ex : 2000 mm/min)* |
| Angle servo stylo levé | *(✏️ ex : 90°)* |
| Angle servo stylo baissé | *(✏️ ex : 50°)* |
| Délai après commande servo | *(✏️ ex : 200 ms)* |

---

## Environnement de développement

| Outil | Version |
|---|---|
| IDE | *(✏️ ex : Arduino IDE 2.x / PlatformIO)* |
| Bibliothèque Stepper | *(✏️ ex : Arduino built-in)* |
| Bibliothèque Servo | *(✏️ ex : Arduino built-in)* |
| Port série | 115200 bauds |
