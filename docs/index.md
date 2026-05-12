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

<div class="stats-grid fade-in-delay">
  <div class="stat-item">
    <span class="stat-num">2</span>
    <span class="stat-lbl">Axes de déplacement</span>
  </div>
  <div class="stat-item">
    <span class="stat-num">1</span>
    <span class="stat-lbl">Servo-moteur stylo</span>
  </div>
  <div class="stat-item">
    <span class="stat-num">4</span>
    <span class="stat-lbl">Membres d'équipe</span>
  </div>
  <div class="stat-item">
    <span class="stat-num">100%</span>
    <span class="stat-lbl">Conçu et fabriqué</span>
  </div>
</div>

## Présentation du projet

<div class="cards-grid">
  <div class="info-card reveal">
    <div class="card-icon">⚙️</div>
    <h3>Mécanique</h3>
    <p>Structure aluminium sur deux axes X/Y, guidages linéaires, courroies crantées et châssis imprimé en 3D.</p>
  </div>
  <div class="info-card reveal">
    <div class="card-icon">⚡</div>
    <h3>Électronique</h3>
    <p>ESP32-S3, drivers A4988, régulateur 5V et PCB conçu sous KiCad pour piloter les moteurs pas-à-pas.</p>
  </div>
  <div class="info-card reveal">
    <div class="card-icon">💻</div>
    <h3>Logiciel</h3>
    <p>Conversion de fichiers vectoriels en G-code, firmware Arduino et interface de contrôle de la machine.</p>
  </div>
</div>

> **En résumé :** La MachineThatDraw transforme un fichier numérique en tracé physique. L'utilisateur fournit une image vectorielle, la machine la convertit en instructions de déplacement et reproduit fidèlement le dessin sur papier.

---

## Modèle 3D interactif

<iframe
  height="500"
  width="100%"
  src="https://modelembedder.net/embed?did=f85f35a7b123fd4b19e50d84&wvm=v&wvmid=2973a15f91d351ab53681340&eid=c8cf3c6fac028151a842f9c9&elementType=ASSEMBLY"
  frameborder="0"
  allowfullscreen>
</iframe>

---

## Vidéo de démonstration

<div class="warn-box">
  <p>✏️ <strong>À compléter</strong> — Remplace <code>VOTRE_ID</code> par l'identifiant de ta vidéo YouTube.</p>
</div>

<iframe width="100%" height="440"
  src="https://www.youtube.com/embed/VOTRE_ID"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen>
</iframe>

---

## Poster du projet

<div class="poster-wrap">
  <img src="{{ '/assets/images/poster.svg' | relative_url }}" alt="Poster du projet Machine That Draw" style="width:100%;border-radius:12px;border:1px solid #e2e8f0;">
</div>

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
