---
layout: default
title: Étude et choix techniques
parent: Introduction
nav_order: 3
---

# Étude et choix techniques

Avant de commencer la fabrication, nous avons étudié les différentes architectures possibles pour notre machine.

---

## 1. Architecture de la machine : le choix cartésien

Nous avons choisi une **architecture cartésienne pure** (un axe X qui se déplace de façon indépendante sur un axe Y). Ce choix offre :

- **Simplicité de contrôle** — Un déplacement en X ne sollicite que le moteur X.
- **Fiabilité géométrique** — L'équerrage à 90° est mécaniquement garanti.
- **Facilité de débogage** — Les axes étant découplés, les problèmes sont faciles à isoler.

---

## 2. Guidage et transmission

Le mouvement est transmis par des **courroies GT2** entraînées par des poulies crantées montées sur l'arbre des moteurs NEMA 17. Les guidages sont assurés par des tiges linéaires.

---

## 3. Motorisation (cahier des charges)

| Actionneur | Rôle | Imposé par l'école |
|---|---|---|
| 2× Moteur NEMA 17 | Déplacement axes X et Y | Oui |
| 1× Servo-moteur | Lever/baisser le stylo (axe Z) | Oui |

Les moteurs NEMA 17 offrent un couple de maintien largement suffisant pour déplacer un simple stylo, garantissant qu'aucune perte de pas ne surviendra.

---

## 4. Électronique choisie

| Composant | Rôle |
|---|---|
| ESP32-S3-UNO | Microcontrôleur principal, génère les signaux STEP/DIR |
| 2× A4988 | Drivers moteurs pas-à-pas |
| R-78E5.0-1.0 | Régulateur 12V → 5V pour l'alimentation logique |
| PCB sur-mesure | Intégration de tous les composants (KiCad 9) |

*(✏️ Complète avec les détails de vos choix et les alternatives que vous avez écartées.)*
