---
layout: default
title: Présentation générale
parent: Introduction
nav_order: 1
---

# Présentation générale

Bienvenue dans la documentation officielle du **Groupe 06** de MachineThatDraws. Ce projet est réalisé au sein du MakerSpace d'UniLaSalle Amiens dans le cadre d'un projet académique. Notre machine est un traceur vectoriel automatisé capable de dessiner sur une surface de travail.

---

## Qu'est-ce que la MachineThatDraw ?

La MachineThatDraw est une machine à dessiner à commande numérique (CNC) de type cartésien. Elle déplace un stylo sur deux axes (X et Y) pour reproduire fidèlement n'importe quel fichier vectoriel ou image numérique sur une feuille de papier.

Le flux de traitement est le suivant :

```
Fichier numérique → Conversion G-code → Firmware ESP32 → Moteurs → Tracé physique
```

---

## Architecture générale

<div class="cards-grid">
  <div class="info-card">
    <div class="card-icon">🔩</div>
    <h3>Structure mécanique</h3>
    <p>Châssis cartésien avec deux axes indépendants. Les pièces structurelles sont imprimées en 3D.</p>
  </div>
  <div class="info-card">
    <div class="card-icon">🖥️</div>
    <h3>Contrôleur</h3>
    <p>Microcontrôleur ESP32-S3-UNO couplé à deux drivers A4988 pour piloter les moteurs NEMA 17.</p>
  </div>
  <div class="info-card">
    <div class="card-icon">📐</div>
    <h3>Zone de dessin</h3>
    <p>Surface de travail adaptée à la feuille A4. Le stylo est levé/baissé par un servo-moteur.</p>
  </div>
</div>

---

## Modèle 3D

Notre modèle 3D est disponible sur OnShape :

<a href="https://cad.onshape.com/documents/f85f35a7b123fd4b19e50d84/w/c95c821d145ea73101043f36/e/c8cf3c6fac028151a842f9c9" target="_blank" class="btn btn-primary">Ouvrir le modèle OnShape ↗</a>

---

*(✏️ Ajoute ici une photo ou capture de la machine finale)*
