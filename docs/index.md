---
layout: home
title: Accueil
nav_order: 1
permalink: /
---

<div class="home-hero">
  <div class="home-hero-inner">
    <span class="home-badge">Makerspace Amiens · Groupe 06 · 2025-2026</span>
    <h1 class="home-title">Machine That Draw</h1>
    <p class="home-sub">Machine dessinatrice à commande numérique — conçue et fabriquée de A à Z par 4 étudiants.</p>
    <div class="home-btns">
      <a href="{{ site.baseurl }}/objectifs" class="btn btn-primary">Découvrir le projet →</a>
      <a href="https://cad.onshape.com/documents/f85f35a7b123fd4b19e50d84/w/c95c821d145ea73101043f36/e/c8cf3c6fac028151a842f9c9" target="_blank" class="btn btn-outline">Modèle 3D OnShape ↗</a>
      <a href="https://github.com/Makerspace-Amiens-2025-26/MachineThatDraws-Groupe06" target="_blank" class="btn btn-outline">GitHub ↗</a>
    </div>
  </div>
</div>

---

## Le projet

La **MachineThatDraw** est un traceur vectoriel automatisé conçu dans le cadre du projet MakerSpace 2025-2026. Elle reproduit n'importe quel fichier numérique sous forme de tracé physique sur papier.

<div class="cards-grid">
  <div class="info-card">
    <span class="card-icon">⚙️</span>
    <h3>Mécanique</h3>
    <p>Structure cartésienne X/Y, guidages linéaires, courroies GT2 et pièces imprimées en 3D.</p>
  </div>
  <div class="info-card">
    <span class="card-icon">⚡</span>
    <h3>Électronique</h3>
    <p>ESP32-S3-UNO, drivers A4988, PCB sur-mesure conçu sous KiCad 9.</p>
  </div>
  <div class="info-card">
    <span class="card-icon">💻</span>
    <h3>Logiciel</h3>
    <p>Conversion vectorielle en G-code et firmware pour piloter les moteurs pas-à-pas.</p>
  </div>
</div>

---

## Modèle 3D

<div class="model-viewer-wrap">
  <model-viewer
    src="https://makerspace-amiens-2025-26.github.io/MachineThatDraws-Groupe06/assets/models/machine.gltf"
    camera-controls
    auto-rotate
    auto-rotate-delay="1000"
    rotation-per-second="20deg"
    shadow-intensity="1"
    environment-image="neutral"
    alt="Modèle 3D Machine That Draw"
    style="width:100%;height:520px;border-radius:12px;background:#0d1117;">
  </model-viewer>
</div>

---

## L'équipe

<div class="team-grid">
  <div class="team-card">
    <div class="team-av">AA</div>
    <div class="team-name">Avsin ATAC</div>
  </div>
  <div class="team-card">
    <div class="team-av">PV</div>
    <div class="team-name">Pierre VILLAIN</div>
  </div>
  <div class="team-card">
    <div class="team-av">DM</div>
    <div class="team-name">Djaher MADIALI</div>
  </div>
  <div class="team-card">
    <div class="team-av">EV</div>
    <div class="team-name">Emilien VITRY-LHOTTE</div>
  </div>
</div>
