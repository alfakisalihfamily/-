<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>شجرة عائلة آل الفكي صالح</title>
<link href="https://fonts.googleapis.com/css2?family=Amiri:ital,wght@0,400;0,700;1,400&family=Noto+Naskh+Arabic:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #4a9eda;
    --gold-light: #7ec8f0;
    --gold-dark: #1e5f8a;
    --ink: #060c14;
    --parchment: #d8eaf5;
    --parchment-dark: #b8d4e8;
    --brown: #0e2b3d;
    --brown-mid: #1e4c6b;
    --cream: #eef5fd;
    --red-accent: #1a4e8b;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'Noto Naskh Arabic', serif;
    background: var(--ink);
    color: var(--parchment);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* === BACKGROUND === */
  .bg-layer {
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse at 20% 20%, rgba(201,168,76,0.08) 0%, transparent 60%),
      radial-gradient(ellipse at 80% 80%, rgba(139,26,26,0.07) 0%, transparent 60%),
      linear-gradient(160deg, #060c14 0%, #081828 50%, #040a10 100%);
    z-index: 0;
  }

  .bg-pattern {
    position: fixed;
    inset: 0;
    background-image:
      repeating-linear-gradient(45deg, rgba(201,168,76,0.03) 0px, rgba(201,168,76,0.03) 1px, transparent 1px, transparent 40px),
      repeating-linear-gradient(-45deg, rgba(201,168,76,0.03) 0px, rgba(201,168,76,0.03) 1px, transparent 1px, transparent 40px);
    z-index: 0;
  }

  /* === HEADER === */
  header {
    position: relative;
    z-index: 10;
    text-align: center;
    padding: 60px 20px 40px;
  }

  .ornament-top {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;
    margin-bottom: 24px;
  }

  .ornament-line {
    height: 1px;
    width: 120px;
    background: linear-gradient(to left, transparent, var(--gold), transparent);
  }

  .ornament-diamond {
    width: 10px;
    height: 10px;
    background: var(--gold);
    transform: rotate(45deg);
  }

  .header-badge {
    display: inline-block;
    border: 1px solid var(--gold-dark);
    border-radius: 2px;
    padding: 4px 20px;
    font-size: 11px;
    letter-spacing: 3px;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 18px;
    background: rgba(201,168,76,0.05);
  }

  h1 {
    font-family: 'Amiri', serif;
    font-size: clamp(2.4rem, 6vw, 4.5rem);
    font-weight: 700;
    color: var(--gold-light);
    line-height: 1.2;
    text-shadow: 0 2px 20px rgba(201,168,76,0.4);
    margin-bottom: 12px;
    animation: fadeDown 1s ease both;
  }

  .subtitle {
    font-size: 1.1rem;
    color: rgba(245,237,216,0.6);
    letter-spacing: 1px;
    animation: fadeDown 1s ease 0.2s both;
  }

  @keyframes fadeDown {
    from { opacity: 0; transform: translateY(-20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* === DIVIDER === */
  .section-divider {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    margin: 32px auto;
    max-width: 500px;
  }

  .div-line {
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, transparent, var(--gold-dark));
  }

  .div-line.right {
    background: linear-gradient(to left, transparent, var(--gold-dark));
  }

  .div-ornament {
    font-size: 18px;
    color: var(--gold);
  }

  /* === TREE CONTAINER === */
  .tree-section {
    position: relative;
    z-index: 10;
    padding: 0 20px 60px;
    max-width: 1100px;
    margin: 0 auto;
  }

  .tree-wrapper {
    overflow-x: auto;
    padding-bottom: 20px;
  }

  /* === TREE SVG LINES === */
  .tree-svg {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
    pointer-events: none;
    z-index: 1;
  }

  /* === TREE LAYOUT === */
  .tree-root {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
  }

  .level {
    display: flex;
    justify-content: center;
    gap: 20px;
    position: relative;
    width: 100%;
    flex-wrap: wrap;
  }

  /* vertical connector */
  .v-connector {
    width: 2px;
    height: 40px;
    background: linear-gradient(to bottom, var(--gold-dark), var(--gold));
    margin: 0 auto;
    position: relative;
  }

  .v-connector::after {
    content: '';
    position: absolute;
    bottom: -4px;
    left: 50%;
    transform: translateX(-50%);
    width: 8px;
    height: 8px;
    background: var(--gold);
    border-radius: 50%;
  }

  /* horizontal connector bar */
  .h-connector {
    position: relative;
    height: 2px;
    background: linear-gradient(to right, var(--gold-dark), var(--gold), var(--gold-dark));
    margin: 0 60px;
  }

  .connector-row {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
  }

  .h-bar-wrapper {
    width: 80%;
    max-width: 700px;
    position: relative;
    margin: 0 auto;
  }

  /* === CARD === */
  .card {
    position: relative;
    background: linear-gradient(135deg, rgba(20,14,4,0.95) 0%, rgba(30,20,8,0.95) 100%);
    border: 1px solid var(--gold-dark);
    border-radius: 3px;
    padding: 18px 22px;
    min-width: 180px;
    max-width: 220px;
    text-align: center;
    cursor: pointer;
    transition: all 0.35s ease;
    animation: fadeIn 0.8s ease both;
    box-shadow:
      0 0 0 1px rgba(201,168,76,0.08),
      0 4px 24px rgba(0,0,0,0.6),
      inset 0 1px 0 rgba(201,168,76,0.12);
    z-index: 5;
  }

  .card::before {
    content: '';
    position: absolute;
    inset: 3px;
    border: 1px solid rgba(201,168,76,0.08);
    border-radius: 2px;
    pointer-events: none;
  }

  .card:hover {
    border-color: var(--gold);
    box-shadow:
      0 0 0 1px rgba(201,168,76,0.2),
      0 8px 32px rgba(0,0,0,0.7),
      0 0 20px rgba(201,168,76,0.12),
      inset 0 1px 0 rgba(201,168,76,0.2);
    transform: translateY(-3px);
  }

  .card.root-card {
    min-width: 220px;
    max-width: 260px;
    border-color: var(--gold);
    background: linear-gradient(135deg, rgba(40,26,8,0.98) 0%, rgba(25,16,4,0.98) 100%);
    box-shadow:
      0 0 0 1px rgba(201,168,76,0.2),
      0 8px 40px rgba(0,0,0,0.7),
      0 0 30px rgba(201,168,76,0.1);
  }

  .card-icon {
    font-size: 24px;
    margin-bottom: 8px;
    display: block;
  }

  .card-name {
    font-family: 'Amiri', serif;
    font-size: 1.15rem;
    font-weight: 700;
    color: var(--gold-light);
    line-height: 1.3;
  }

  .root-card .card-name {
    font-size: 1.35rem;
    color: var(--gold-light);
  }

  .card-title {
    font-size: 0.72rem;
    color: rgba(201,168,76,0.6);
    letter-spacing: 1px;
    margin-top: 5px;
    text-transform: uppercase;
  }

  .card-detail {
    margin-top: 10px;
    padding-top: 10px;
    border-top: 1px solid rgba(201,168,76,0.12);
    font-size: 0.78rem;
    color: rgba(245,237,216,0.55);
    line-height: 1.6;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: scale(0.94); }
    to { opacity: 1; transform: scale(1); }
  }

  /* === BRANCH CHILDREN === */
  .children-group {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    position: relative;
    width: 100%;
  }

  .child-col {
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
  }

  /* === FOOTER CREDITS === */
  .credits {
    position: relative;
    z-index: 10;
    text-align: center;
    padding: 40px 20px 60px;
    border-top: 1px solid rgba(201,168,76,0.1);
    max-width: 600px;
    margin: 0 auto;
  }

  .credits-title {
    font-family: 'Amiri', serif;
    font-size: 1.4rem;
    color: var(--gold);
    margin-bottom: 24px;
  }

  .credits-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-top: 20px;
  }

  .credit-item {
    background: rgba(201,168,76,0.04);
    border: 1px solid rgba(201,168,76,0.15);
    border-radius: 3px;
    padding: 16px;
    transition: border-color 0.3s;
  }

  .credit-item:hover {
    border-color: rgba(201,168,76,0.4);
  }

  .credit-role {
    font-size: 0.7rem;
    letter-spacing: 2px;
    color: var(--gold);
    text-transform: uppercase;
    margin-bottom: 8px;
  }

  .credit-name {
    font-family: 'Amiri', serif;
    font-size: 1.05rem;
    color: var(--parchment);
    line-height: 1.4;
  }

  /* === LEGEND === */
  .legend {
    display: flex;
    justify-content: center;
    gap: 24px;
    flex-wrap: wrap;
    margin: 0 auto 40px;
    padding: 0 20px;
    position: relative;
    z-index: 10;
  }

  .legend-item {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 0.8rem;
    color: rgba(245,237,216,0.55);
  }

  .legend-dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    border: 2px solid var(--gold);
    background: rgba(201,168,76,0.2);
  }

  /* === RESPONSIVE === */
  @media (max-width: 700px) {
    .credits-grid { grid-template-columns: 1fr; }
    .children-group { gap: 12px; }
    .card { min-width: 140px; padding: 14px 14px; }
    .card-name { font-size: 0.95rem; }
  }

  /* connector lines between children */
  .children-connector {
    position: relative;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    width: 100%;
  }

  .branch-line-h {
    position: absolute;
    top: 0;
    height: 2px;
    background: linear-gradient(to right, transparent, var(--gold-dark) 20%, var(--gold-dark) 80%, transparent);
  }

  .branch-line-v {
    width: 2px;
    height: 30px;
    background: linear-gradient(to bottom, var(--gold-dark), var(--gold));
    margin: 0 auto;
  }

  /* glow pulse on root */
  .card.root-card::after {
    content: '';
    position: absolute;
    inset: -1px;
    border-radius: 3px;
    border: 1px solid var(--gold);
    opacity: 0;
    animation: pulse-glow 3s ease-in-out infinite;
  }

  @keyframes pulse-glow {
    0%, 100% { opacity: 0; box-shadow: 0 0 0px var(--gold); }
    50% { opacity: 0.4; box-shadow: 0 0 20px rgba(201,168,76,0.3); }
  }
</style>
</head>
<body>

<div class="bg-layer"></div>
<div class="bg-pattern"></div>

<!-- HEADER -->
<header>
  <div class="ornament-top">
    <div class="ornament-line"></div>
    <div class="ornament-diamond"></div>
    <div class="ornament-line" style="background: linear-gradient(to right, transparent, var(--gold), transparent);"></div>
  </div>

  <div class="header-badge">سجل النسب</div>
  <h1>آل الفكي صالح</h1>
  <p class="subtitle">شجرة العائلة — حفظ الجذور وتوثيق النسب</p>

  <div class="ornament-top" style="margin-top:24px; margin-bottom:0;">
    <div class="ornament-line"></div>
    <div class="ornament-diamond"></div>
    <div class="ornament-line" style="background: linear-gradient(to right, transparent, var(--gold), transparent);"></div>
  </div>
</header>



<!-- COMING SOON -->
<div style="position:relative; z-index:10; text-align:center; padding: 40px 20px;">
  <div style="display:inline-block; border: 1px solid rgba(74,158,218,0.3); border-radius:4px; padding: 30px 60px; background: rgba(74,158,218,0.05);">
    <div style="font-family:'Amiri',serif; font-size:3.5rem; color:#7ec8f0; text-shadow: 0 0 30px rgba(74,158,218,0.4); letter-spacing:6px;">قريباً</div>
    <div style="margin-top:14px; width:60px; height:2px; background:linear-gradient(to right, transparent, #4a9eda, transparent); margin-inline:auto;"></div>
  </div>
</div>

<!-- CREDITS -->
<div class="credits">
  <div class="section-divider">
    <div class="div-line"></div>
    <span class="div-ornament">✦</span>
    <div class="div-line right"></div>
  </div>

  <div class="credits-title">فريق العمل</div>

  <div class="credits-grid">
    <div class="credit-item">
      <div class="credit-role">الإدارة</div>
      <div class="credit-name">أحمد خالد أحمد</div>
    </div>
    <div class="credit-item">
      <div class="credit-role">بناء وتصميم</div>
      <div class="credit-name">خالد أحمد خالد</div>
    </div>
  </div>


</div>

</body>
</html>
