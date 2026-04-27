---
layout: default
title: Électronique & PCB
nav_order: 3
---

# Électronique & PCB

Conception du circuit imprimé réalisée sous **KiCad 9** par notre équipe.

## Architecture du circuit

<div class="schema-block">

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 820 440" width="100%" style="max-width:820px;display:block;margin:0 auto" font-family="Inter,system-ui,sans-serif">
  <defs>
    <linearGradient id="ig" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#6366f1"/>
      <stop offset="100%" style="stop-color:#4f46e5"/>
    </linearGradient>
    <linearGradient id="dg" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0f172a"/>
      <stop offset="100%" style="stop-color:#1e293b"/>
    </linearGradient>
    <marker id="arr" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto">
      <polygon points="0 0, 8 3, 0 6" fill="#6366f1"/>
    </marker>
    <marker id="arrg" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto">
      <polygon points="0 0, 8 3, 0 6" fill="#10b981"/>
    </marker>
    <marker id="arro" markerWidth="8" markerHeight="6" refX="7" refY="3" orient="auto">
      <polygon points="0 0, 8 3, 0 6" fill="#f59e0b"/>
    </marker>
  </defs>

  <!-- Fond -->
  <rect width="820" height="440" fill="#f8fafc" rx="14"/>

  <!-- ── ALIMENTATION ── -->
  <!-- Barrel Jack -->
  <rect x="20" y="175" width="110" height="70" rx="10" fill="url(#dg)" stroke="#334155" stroke-width="1.5"/>
  <text x="75" y="204" text-anchor="middle" font-size="11" font-weight="700" fill="white">Barrel Jack</text>
  <text x="75" y="220" text-anchor="middle" font-size="10" fill="#94a3b8">J1</text>
  <text x="75" y="235" text-anchor="middle" font-size="10" fill="#f59e0b">12V DC</text>

  <!-- Régulateur -->
  <rect x="175" y="155" width="120" height="90" rx="10" fill="url(#dg)" stroke="#334155" stroke-width="1.5"/>
  <text x="235" y="184" text-anchor="middle" font-size="11" font-weight="700" fill="white">R-78E5.0</text>
  <text x="235" y="200" text-anchor="middle" font-size="10" fill="#94a3b8">Régulateur 5V/1A</text>
  <text x="235" y="218" text-anchor="middle" font-size="10" fill="#f59e0b">12V → 5V</text>
  <text x="235" y="234" text-anchor="middle" font-size="9" fill="#64748b">U2</text>

  <!-- Flèche Barrel → Régulateur -->
  <line x1="130" y1="210" x2="173" y2="210" stroke="#f59e0b" stroke-width="2" marker-end="url(#arro)"/>
  <text x="152" y="204" text-anchor="middle" font-size="9" fill="#f59e0b">12V</text>

  <!-- Condensateurs -->
  <rect x="175" y="270" width="120" height="55" rx="8" fill="#f1f5f9" stroke="#e2e8f0" stroke-width="1.5"/>
  <text x="235" y="295" text-anchor="middle" font-size="10" font-weight="600" fill="#475569">Condensateurs</text>
  <text x="235" y="311" text-anchor="middle" font-size="9" fill="#94a3b8">C1 10µF · C2 100µF · C3 10µF</text>

  <!-- ── ESP32-S3-UNO ── -->
  <rect x="340" y="130" width="160" height="170" rx="12" fill="url(#ig)" stroke="rgba(99,102,241,0.4)" stroke-width="2"/>
  <rect x="348" y="138" width="144" height="154" rx="9" fill="rgba(0,0,0,0.25)"/>
  <text x="420" y="175" text-anchor="middle" font-size="13" font-weight="800" fill="white">ESP32-S3</text>
  <text x="420" y="193" text-anchor="middle" font-size="11" font-weight="600" fill="#c7d2fe">UNO</text>
  <text x="420" y="215" text-anchor="middle" font-size="9" fill="rgba(255,255,255,0.5)">Microcontrôleur</text>
  <text x="420" y="232" text-anchor="middle" font-size="9" fill="rgba(255,255,255,0.5)">U1</text>
  <!-- Pins -->
  <line x1="356" y1="255" x2="356" y2="255"/>
  <text x="420" y="260" text-anchor="middle" font-size="8.5" fill="#a5b4fc">GPIO → STEP/DIR</text>
  <text x="420" y="274" text-anchor="middle" font-size="8.5" fill="#a5b4fc">PWM → Servo</text>

  <!-- Flèche Régulateur → ESP32 -->
  <line x1="295" y1="195" x2="338" y2="195" stroke="#10b981" stroke-width="2" marker-end="url(#arrg)"/>
  <text x="317" y="188" text-anchor="middle" font-size="9" fill="#10b981">5V</text>

  <!-- ── DRIVERS A4988 ── -->
  <!-- Driver 1 -->
  <rect x="560" y="100" width="135" height="100" rx="10" fill="url(#dg)" stroke="#334155" stroke-width="1.5"/>
  <text x="627" y="132" text-anchor="middle" font-size="12" font-weight="700" fill="white">A4988</text>
  <text x="627" y="150" text-anchor="middle" font-size="10" fill="#94a3b8">Driver Moteur X</text>
  <text x="627" y="167" text-anchor="middle" font-size="9" fill="#64748b">A1 — STEP/DIR</text>
  <text x="627" y="183" text-anchor="middle" font-size="9" fill="#f59e0b">12V logique</text>

  <!-- Driver 2 -->
  <rect x="560" y="240" width="135" height="100" rx="10" fill="url(#dg)" stroke="#334155" stroke-width="1.5"/>
  <text x="627" y="272" text-anchor="middle" font-size="12" font-weight="700" fill="white">A4988</text>
  <text x="627" y="290" text-anchor="middle" font-size="10" fill="#94a3b8">Driver Moteur Y</text>
  <text x="627" y="307" text-anchor="middle" font-size="9" fill="#64748b">A2 — STEP/DIR</text>
  <text x="627" y="323" text-anchor="middle" font-size="9" fill="#f59e0b">12V logique</text>

  <!-- Flèches ESP32 → Drivers -->
  <line x1="500" y1="175" x2="558" y2="155" stroke="#6366f1" stroke-width="1.8" marker-end="url(#arr)"/>
  <text x="527" y="158" text-anchor="middle" font-size="8.5" fill="#6366f1">STEP/DIR</text>
  <line x1="500" y1="245" x2="558" y2="285" stroke="#6366f1" stroke-width="1.8" marker-end="url(#arr)"/>
  <text x="527" y="275" text-anchor="middle" font-size="8.5" fill="#6366f1">STEP/DIR</text>

  <!-- ── MOTEURS ── -->
  <!-- Moteur X -->
  <rect x="748" y="100" width="58" height="60" rx="8" fill="#f1f5f9" stroke="#e2e8f0" stroke-width="1.5"/>
  <text x="777" y="126" text-anchor="middle" font-size="9.5" font-weight="700" fill="#1e293b">Moteur</text>
  <text x="777" y="142" text-anchor="middle" font-size="9" fill="#475569">X — J2</text>

  <!-- Moteur Y -->
  <rect x="748" y="240" width="58" height="60" rx="8" fill="#f1f5f9" stroke="#e2e8f0" stroke-width="1.5"/>
  <text x="777" y="266" text-anchor="middle" font-size="9.5" font-weight="700" fill="#1e293b">Moteur</text>
  <text x="777" y="282" text-anchor="middle" font-size="9" fill="#475569">Y — J3</text>

  <!-- Flèches Drivers → Moteurs -->
  <line x1="695" y1="140" x2="746" y2="133" stroke="#10b981" stroke-width="1.8" marker-end="url(#arrg)"/>
  <line x1="695" y1="285" x2="746" y2="272" stroke="#10b981" stroke-width="1.8" marker-end="url(#arrg)"/>

  <!-- ── SERVO ── -->
  <rect x="560" y="380" width="135" height="46" rx="8" fill="#f1f5f9" stroke="#e2e8f0" stroke-width="1.5"/>
  <text x="627" y="400" text-anchor="middle" font-size="10" font-weight="700" fill="#1e293b">Servo-moteur stylo</text>
  <text x="627" y="416" text-anchor="middle" font-size="9" fill="#475569">PWM depuis ESP32</text>

  <!-- Flèche ESP32 → Servo -->
  <line x1="460" y1="295" x2="558" y2="395" stroke="#6366f1" stroke-width="1.5" stroke-dasharray="5,3" marker-end="url(#arr)"/>
  <text x="500" y="365" text-anchor="middle" font-size="8.5" fill="#6366f1">PWM</text>

  <!-- Légende -->
  <rect x="20" y="375" width="290" height="52" rx="8" fill="#f1f5f9" stroke="#e2e8f0" stroke-width="1"/>
  <line x1="32" y1="395" x2="55" y2="395" stroke="#6366f1" stroke-width="2" marker-end="url(#arr)"/>
  <text x="62" y="398" font-size="10" fill="#475569">Signal logique (GPIO)</text>
  <line x1="32" y1="413" x2="55" y2="413" stroke="#10b981" stroke-width="2" marker-end="url(#arrg)"/>
  <text x="62" y="417" font-size="10" fill="#475569">Puissance moteur</text>
  <line x1="165" y1="395" x2="188" y2="395" stroke="#f59e0b" stroke-width="2" marker-end="url(#arro)"/>
  <text x="195" y="398" font-size="10" fill="#475569">Alimentation</text>
</svg>

</div>

---

## Composants principaux

<div class="bom-cards">
  <div class="bom-card">
    <div class="bom-ref">U1</div>
    <div class="bom-info">
      <div class="bom-name">ESP32-S3-UNO</div>
      <div class="bom-desc">Microcontrôleur principal — génère les signaux STEP/DIR pour les drivers et le PWM pour le servo</div>
    </div>
  </div>
  <div class="bom-card">
    <div class="bom-ref">A1 / A2</div>
    <div class="bom-info">
      <div class="bom-name">Module A4988</div>
      <div class="bom-desc">Drivers de moteurs pas-à-pas pour les axes X et Y — tension logique 5V, puissance 12V</div>
    </div>
  </div>
  <div class="bom-card">
    <div class="bom-ref">U2</div>
    <div class="bom-info">
      <div class="bom-name">R-78E5.0-1.0</div>
      <div class="bom-desc">Régulateur DC/DC — convertit le 12V d'entrée en 5V/1A pour l'ESP32 et la logique</div>
    </div>
  </div>
  <div class="bom-card">
    <div class="bom-ref">J1</div>
    <div class="bom-info">
      <div class="bom-name">Barrel Jack Switch</div>
      <div class="bom-desc">Connecteur d'alimentation principal 12V DC avec interrupteur intégré</div>
    </div>
  </div>
  <div class="bom-card">
    <div class="bom-ref">J2 / J3</div>
    <div class="bom-info">
      <div class="bom-name">Conn_01x04</div>
      <div class="bom-desc">Connecteurs 4 broches pour les moteurs pas-à-pas X et Y</div>
    </div>
  </div>
  <div class="bom-card">
    <div class="bom-ref">C1–C5</div>
    <div class="bom-info">
      <div class="bom-name">Condensateurs de filtrage</div>
      <div class="bom-desc">10µF × 2, 100µF × 1 — filtrage des alimentations pour stabilité des drivers</div>
    </div>
  </div>
</div>

---

## Tableau des connexions

| Référence | Composant | Broche | Connecté à |
|-----------|-----------|--------|-----------|
| U1 | ESP32-S3-UNO | GPIO STEP/DIR | A1 (moteur X) |
| U1 | ESP32-S3-UNO | GPIO STEP/DIR | A2 (moteur Y) |
| U1 | ESP32-S3-UNO | PWM | Servo-moteur stylo |
| A1/A2 | A4988 | VMOT | 12V (J1) |
| A1/A2 | A4988 | VDD | 5V (U2) |
| U2 | R-78E5.0 | Vin | 12V (J1) |
| U2 | R-78E5.0 | Vout | 5V → U1, A1, A2 |
| J2 | Conn 4 broches | 1–4 | Moteur pas-à-pas X |
| J3 | Conn 4 broches | 1–4 | Moteur pas-à-pas Y |

---

## Fichiers KiCad

> Les fichiers sources du PCB sont disponibles dans le dossier `project/ECAD/` du dépôt GitHub.

[Voir les fichiers sur GitHub](https://github.com/Makerspace-Amiens-2025-26){: .btn .btn-outline target="_blank" }
