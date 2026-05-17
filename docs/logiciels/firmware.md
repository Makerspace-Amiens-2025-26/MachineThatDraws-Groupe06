---
layout: default
title: Firmware ESP32
parent: Fonctionnement des logiciels
nav_order: 2
---

# Firmware ESP32

Le firmware est le programme qui tourne sur l'ESP32-S3-UNO et interprète les commandes G-code pour piloter les moteurs.

---

## Commandes G-code supportées

| Commande | Action |
|---|---|
| `G0 X__ Y__` | Déplacement rapide sans tracé (stylo levé) |
| `G1 X__ Y__` | Déplacement avec tracé (stylo baissé) |
| `M3` | Baisser le stylo |
| `M5` | Lever le stylo |

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

---

## Calibration

*(✏️ Paramètres de calibration — pas/mm, vitesse, accélération.)*
