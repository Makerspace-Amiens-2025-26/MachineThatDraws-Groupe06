---
layout: default
title: Documentation Technique
nav_order: 7
---

# Documentation Technique

## ⚙️ Fonctionnement de la machine

La machine utilise **deux axes (X et Y)** pour déplacer le stylo sur la surface. Un troisième mécanisme (servo-moteur) permet de lever et baisser le stylo.

### Flux de données

```
Image → Vectorisation → G-code → Arduino → Moteurs → Dessin
```

---

## 💻 Partie Logicielle

### Code principal Arduino

```cpp
// Machine That Draw — Groupe 06
// Makerspace Amiens 2025-2026

#include <Stepper.h>

// ✏️ Remplace par tes vraies broches
const int STEPS = 200;
Stepper motorX(STEPS, 8, 9, 10, 11);
Stepper motorY(STEPS, 4, 5, 6, 7);

void setup() {
  Serial.begin(9600);
  motorX.setSpeed(60);
  motorY.setSpeed(60);
}

void loop() {
  if (Serial.available()) {
    String cmd = Serial.readStringUntil('\n');
    parseGCode(cmd);
  }
}
```

### Interpréteur G-code

```cpp
void parseGCode(String cmd) {
  // ✏️ Remplace par votre vrai code
  if (cmd.startsWith("G1")) {
    int xVal = cmd.substring(cmd.indexOf('X') + 1).toInt();
    int yVal = cmd.substring(cmd.indexOf('Y') + 1).toInt();
    motorX.step(xVal);
    motorY.step(yVal);
  }
}
```

---

## 🔌 Schéma électronique

*(✏️ Ajoute ici une photo ou image de ton schéma de câblage)*

<!-- ![Schéma électronique](/assets/images/schema.png) -->

---

## 📋 Brochage Arduino

| Broche | Connexion |
|--------|-----------|
| D4–D7 | Moteur Y |
| D8–D11 | Moteur X |
| D12 | Servo stylo |
| 5V / GND | Alimentation |

---

## 📦 Liste des matériaux (BOM)

| Composant | Référence | Quantité | Prix unitaire |
|-----------|-----------|----------|---------------|
| *(✏️)* | *(✏️)* | *(✏️)* | *(✏️)* |
| *(✏️)* | *(✏️)* | *(✏️)* | *(✏️)* |

---

## 🔗 Ressources utiles

- [Documentation Arduino](https://docs.arduino.cc)
- [OnShape — notre modèle](#)
- [GitHub du projet](https://github.com/Makerspace-Amiens-2025-26)