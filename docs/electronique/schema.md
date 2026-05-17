---
layout: default
title: Schéma électronique
parent: Électronique & PCB
nav_order: 1
---

# Schéma électronique

Le schéma électronique a été conçu sous **KiCad 9**. Il regroupe l'ensemble des composants de la carte de contrôle.

---

## Architecture du circuit

```
Alimentation 12V (Barrel Jack)
        │
        ├─── Régulateur R-78E5.0 ──→ 5V → ESP32-S3-UNO
        │
        ├─── Driver A4988 #1 ──→ Moteur NEMA 17 (Axe X)
        │
        └─── Driver A4988 #2 ──→ Moteur NEMA 17 (Axe Y)

ESP32-S3-UNO
        ├─── GPIO STEP/DIR ──→ A4988 #1 (Axe X)
        ├─── GPIO STEP/DIR ──→ A4988 #2 (Axe Y)
        └─── PWM ──────────→ Servo-moteur stylo
```

---

## Composants principaux

<div class="bom-cards">
  <div class="bom-card">
    <div class="bom-ref">U1</div>
    <div class="bom-info">
      <div class="bom-name">ESP32-S3-UNO</div>
      <div class="bom-desc">Microcontrôleur principal — génère les signaux STEP/DIR et le PWM servo</div>
    </div>
  </div>
  <div class="bom-card">
    <div class="bom-ref">A1/A2</div>
    <div class="bom-info">
      <div class="bom-name">Module A4988</div>
      <div class="bom-desc">Drivers moteurs pas-à-pas — 5V logique, 12V puissance</div>
    </div>
  </div>
  <div class="bom-card">
    <div class="bom-ref">U2</div>
    <div class="bom-info">
      <div class="bom-name">R-78E5.0-1.0</div>
      <div class="bom-desc">Régulateur DC/DC — convertit 12V en 5V/1A</div>
    </div>
  </div>
  <div class="bom-card">
    <div class="bom-ref">J1</div>
    <div class="bom-info">
      <div class="bom-name">Barrel Jack</div>
      <div class="bom-desc">Connecteur alimentation 12V DC avec interrupteur</div>
    </div>
  </div>
</div>

---

*(✏️ Ajoute ici une capture du schéma KiCad)*
