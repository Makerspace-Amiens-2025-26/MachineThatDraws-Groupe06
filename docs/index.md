---
layout: home
title: Accueil
nav_order: 1
permalink: /
---

<div class="hero-banner fade-in">
  <div class="hero-tag">Groupe 06 · Makerspace Amiens · 2025-2026</div>
  <h1 class="hero-title">Machine That Draw</h1>
  <p class="hero-desc">Machine dessinatrice à commande numérique — conception, fabrication et programmation réalisées intégralement par notre équipe d'étudiants.</p>
  <div class="hero-btns">
    <a href="https://cad.onshape.com/documents/f85f35a7b123fd4b19e50d84/w/c95c821d145ea73101043f36/e/c8cf3c6fac028151a842f9c9?renderMode=0&uiState=69e8b76c98f18e0d22950a4f" target="_blank" class="btn btn-primary">Modèle 3D OnShape ↗</a>
    <a href="https://github.com/Makerspace-Amiens-2025-26/MachineThatDraws-Groupe06" target="_blank" class="btn btn-outline">Code source GitHub ↗</a>
  </div>
</div>

---

## Introduction

Premièrement, notre projet consiste à concevoir une machine automatisée qui est capable d'écrire et de dessiner avec précision sur une surface plane ce qu'on lui programme. Il s'agit donc d'un projet qui va combiner de la mécanique, de l'électronique mais aussi de la programmation.

> **Notre Mission :** Transformer un simple fichier numérique en un tracé physique fluide et précis grâce à la MachineThatDraw.

---

## Contexte du projet

Dans le cadre du projet MakerSpace 2025-2026, nous devons créer une machine fonctionnelle qui puisse répondre à une problématique de fabrication numérique. La MachineThatDraw est notre réponse pour explorer le contrôle des mouvements sur les axes X et Y.

<div class="cards-grid">
  <div class="info-card reveal">
    <div class="card-icon">⚙️</div>
    <h3>Mécanique</h3>
    <p>Structure sur deux axes X/Y, guidages linéaires, courroies crantées et châssis.</p>
  </div>
  <div class="info-card reveal">
    <div class="card-icon">⚡</div>
    <h3>Électronique</h3>
    <p>ESP32-S3, drivers A4988, PCB conçu sous KiCad pour piloter les moteurs pas-à-pas.</p>
  </div>
  <div class="info-card reveal">
    <div class="card-icon">💻</div>
    <h3>Logiciel</h3>
    <p>Conversion de fichiers vectoriels en G-code et firmware pour contrôler la machine.</p>
  </div>
</div>

---

## Objectifs

- **Automatisation** : Créer un système capable de reproduire des formes de manière autonome.
- **Précision** : Assurer un mouvement fluide des moteurs pour un rendu propre.
- **Polyvalence** : Permettre l'utilisation de différents types de stylos ou feutres.

> **Le petit plus :** Nous visons une compatibilité avec plusieurs types de supports (papier, carton, bois léger...).

---

## Objectifs techniques

| Objectif | Description |
|----------|-------------|
| Axes de déplacement | 2 axes X/Y avec moteurs pas-à-pas |
| Contrôle du stylo | Servo-moteur pour lever/baisser le stylo |
| Format d'entrée | Fichier vectoriel converti en G-code |
| Microcontrôleur | ESP32-S3-UNO |
| Dimensions max | *(✏️ à compléter)* |
| Vitesse de tracé | *(✏️ à compléter)* |

---

## L'équipe

<div class="team-grid">
  <div class="team-card reveal">
    <div class="team-av">AV</div>
    <div class="team-name">Avsin ATAC</div>
    <div class="team-role">Site · Rapport · Vidéo</div>
  </div>
  <div class="team-card reveal">
    <div class="team-av">PI</div>
    <div class="team-name">Pierre VILLAIN</div>
    <div class="team-role">Électronique</div>
  </div>
  <div class="team-card reveal">
    <div class="team-av">DJ</div>
    <div class="team-name">Djhaer MADIALI</div>
    <div class="team-role">Programmation</div>
  </div>
  <div class="team-card reveal">
    <div class="team-av">EM</div>
    <div class="team-name">Emilien VITRY-LHOTTE</div>
    <div class="team-role">Fabrication</div>
  </div>
</div>
