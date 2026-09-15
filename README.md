<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0, viewport-fit=cover">
  <title>DealForge NG — Deals Worth Knowing</title>
  <meta name="description" content="Discover interesting gadgets, tech products, smart finds and deals with DealForge NG. We find it. You decide.">

  <meta property="og:type" content="website">
  <meta property="og:title" content="DealForge NG — Deals Worth Knowing">
  <meta property="og:description" content="Discover interesting gadgets, tech products, smart finds and deals with DealForge NG. We find it. You decide.">
  <meta property="og:url" content="https://dealforge.ng">
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="DealForge NG — Deals Worth Knowing">
  <meta name="twitter:description" content="We find it. You decide.">
  <meta name="theme-color" content="#FF6B2B">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">

  <style>
    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

    :root {
      --charcoal: #171717;
      --charcoal-dark: #242424;
      --orange: #FF6B2B;
      --orange-dark: #E85A1C;
      --white: #FFFFFF;
      --bg-light: #F6F6F4;
      --text-secondary: #707070;

      --radius-card: 18px;
      --radius-pill: 50px;
      --shadow-sm: 0 2px 8px rgba(0,0,0,0.04);
      --shadow-md: 0 8px 24px rgba(0,0,0,0.08);
      --shadow-lg: 0 16px 40px rgba(0,0,0,0.12);
      --shadow-orange: 0 6px 20px rgba(255,107,43,0.32);

      --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      --transition: 0.25s cubic-bezier(0.2, 0.9, 0.4, 1);
    }

    html {
      scroll-behavior: smooth;
      -webkit-text-size-adjust: 100%;
      scroll-padding-top: 80px;
    }

    body {
      font-family: var(--font);
      background: var(--white);
      color: var(--charcoal);
      line-height: 1.5;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      overflow-x: hidden;
    }

    img { max-width: 100%; display: block; height: auto; }
    a { text-decoration: none; color: inherit; }
    button { font-family: inherit; cursor: pointer; border: none; background: none; }
    ul { list-style: none; }

    ::-webkit-scrollbar { width: 6px; height: 6px; }
    ::-webkit-scrollbar-track { background: var(--bg-light); }
    ::-webkit-scrollbar-thumb { background: #ccc; border-radius: 10px; }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* ============ HEADER ============ */
    .site-header {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(255,255,255,0.94);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      border-bottom: 1px solid rgba(0,0,0,0.05);
      transition: box-shadow var(--transition);
    }
    .site-header.scrolled { box-shadow: 0 4px 20px rgba(0,0,0,0.06); }

    .header-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 62px;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }

    .logo {
      font-size: 1.2rem;
      font-weight: 800;
      letter-spacing: -0.5px;
      color: var(--charcoal);
      display: flex;
      align-items: baseline;
      gap: 1px;
    }
    .logo span { color: var(--orange); }

    .desktop-nav { display: none; align-items: center; gap: 30px; }
    .desktop-nav a {
      font-size: 0.88rem;
      font-weight: 500;
      color: var(--charcoal-dark);
      transition: color var(--transition);
      position: relative;
      padding: 4px 0;
    }
    .desktop-nav a::after {
      content: '';
      position: absolute;
      bottom: -2px;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--orange);
      transition: width var(--transition);
    }
    .desktop-nav a:hover { color: var(--charcoal); }
    .desktop-nav a:hover::after { width: 100%; }

    .desktop-cta {
      display: none;
      background: var(--orange);
      color: var(--white);
      padding: 10px 22px;
      border-radius: var(--radius-pill);
      font-weight: 600;
      font-size: 0.85rem;
      transition: all var(--transition);
      box-shadow: var(--shadow-orange);
    }
    .desktop-cta:hover {
      background: var(--orange-dark);
      transform: translateY(-1px);
      box-shadow: 0 8px 24px rgba(255,107,43,0.42);
    }

    .mobile-menu-btn {
      display: flex;
      flex-direction: column;
      gap: 5px;
      padding: 10px;
      background: none;
      border: none;
      cursor: pointer;
      z-index: 1100;
      min-width: 44px;
      min-height: 44px;
      align-items: center;
      justify-content: center;
    }
    .mobile-menu-btn span {
      display: block;
      width: 22px;
      height: 2px;
      background: var(--charcoal);
      border-radius: 2px;
      transition: all var(--transition);
    }
    .mobile-menu-btn.active span:nth-child(1) { transform: rotate(45deg) translate(5px, 5px); }
    .mobile-menu-btn.active span:nth-child(2) { opacity: 0; }
    .mobile-menu-btn.active span:nth-child(3) { transform: rotate(-45deg) translate(5px, -5px); }

    .mobile-nav {
      position: fixed;
      top: 62px;
      left: 0;
      right: 0;
      background: var(--white);
      padding: 16px 20px 24px;
      display: flex;
      flex-direction: column;
      gap: 4px;
      transform: translateY(-130%);
      transition: transform 0.35s cubic-bezier(0.2, 0.9, 0.4, 1);
      z-index: 999;
      border-bottom: 1px solid rgba(0,0,0,0.06);
      box-shadow: var(--shadow-lg);
      max-height: calc(100vh - 62px);
      overflow-y: auto;
    }
    .mobile-nav.open { transform: translateY(0); }
    .mobile-nav a {
      padding: 14px 16px;
      font-size: 1rem;
      font-weight: 500;
      color: var(--charcoal);
      border-radius: 12px;
      transition: background var(--transition);
    }
    .mobile-nav a:hover, .mobile-nav a:active { background: var(--bg-light); }
    .mobile-nav .mobile-cta {
      background: var(--orange);
      color: var(--white);
      text-align: center;
      font-weight: 600;
      margin-top: 8px;
      box-shadow: var(--shadow-orange);
    }

    /* ============ HERO ============ */
    .hero {
      padding: 40px 0 56px;
      background: linear-gradient(165deg, #FAFAF8 0%, #FFFFFF 100%);
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute;
      top: -120px;
      right: -120px;
      width: 340px;
      height: 340px;
      background: radial-gradient(circle, rgba(255,107,43,0.09) 0%, transparent 70%);
      border-radius: 50%;
      pointer-events: none;
    }
    .hero .container { display: flex; flex-direction: column; gap: 40px; position: relative; }
    .hero-content { max-width: 620px; }

    .hero-badge {
      display: inline-block;
      background: rgba(255,107,43,0.1);
      color: var(--orange);
      font-size: 0.7rem;
      font-weight: 700;
      letter-spacing: 1px;
      text-transform: uppercase;
      padding: 6px 14px;
      border-radius: var(--radius-pill);
      margin-bottom: 18px;
    }
    .hero h1 {
      font-size: clamp(2rem, 9vw, 3.75rem);
      font-weight: 800;
      line-height: 1.05;
      letter-spacing: -1.8px;
      color: var(--charcoal);
      margin-bottom: 18px;
    }
    .hero h1 .highlight { color: var(--orange); }
    .hero p {
      font-size: 1.05rem;
      color: var(--text-secondary);
      line-height: 1.6;
      margin-bottom: 24px;
      max-width: 500px;
    }
    .hero-tagline {
      display: inline-block;
      font-size: 0.8rem;
      font-weight: 700;
      letter-spacing: 1.8px;
      text-transform: uppercase;
      color: var(--charcoal);
      border-left: 3px solid var(--orange);
      padding-left: 12px;
      margin-bottom: 28px;
    }
    .hero-ctas { display: flex; flex-wrap: wrap; gap: 12px; }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 14px 26px;
      border-radius: var(--radius-pill);
      font-weight: 600;
      font-size: 0.92rem;
      transition: all var(--transition);
      min-height: 48px;
      touch-action: manipulation;
      border: 1.5px solid transparent;
    }
    .btn-primary {
      background: var(--orange);
      color: var(--white);
      box-shadow: var(--shadow-orange);
    }
    .btn-primary:hover, .btn-primary:active {
      background: var(--orange-dark);
      transform: translateY(-2px);
      box-shadow: 0 10px 28px rgba(255,107,43,0.45);
    }
    .btn-secondary {
      background: var(--white);
      color: var(--charcoal);
      border-color: #E2E2E0;
    }
    .btn-secondary:hover, .btn-secondary:active {
      border-color: var(--charcoal);
      background: var(--bg-light);
      transform: translateY(-2px);
    }

    .hero-visual {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      min-height: 220px;
    }
    .floating-cards {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      width: 100%;
      max-width: 380px;
      position: relative;
    }
    .float-card {
      background: var(--white);
      border-radius: var(--radius-card);
      padding: 14px;
      box-shadow: var(--shadow-md);
      border: 1px solid rgba(0,0,0,0.04);
      animation: float 5s ease-in-out infinite;
      display: flex;
      flex-direction: column;
      gap: 6px;
    }
    .float-card:nth-child(2) { animation-delay: 1.2s; margin-top: 22px; }
    .float-card:nth-child(3) { animation-delay: 2.4s; margin-top: -12px; }
    .float-card:nth-child(4) { animation-delay: 0.6s; margin-top: 10px; }

    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-7px); }
    }

    .float-card-icon { font-size: 1.7rem; line-height: 1; }
    .float-card-title { font-size: 0.72rem; font-weight: 700; color: var(--charcoal); line-height: 1.2; }
    .float-card-price { font-size: 0.78rem; font-weight: 800; color: var(--orange); }
    .float-card-tag {
      font-size: 0.55rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      background: rgba(255,107,43,0.1);
      color: var(--orange);
      padding: 3px 8px;
      border-radius: var(--radius-pill);
      align-self: flex-start;
    }

    /* ============ SECTIONS ============ */
    .section-header { margin-bottom: 28px; }
    .section-header h2 {
      font-size: clamp(1.5rem, 5.5vw, 2.1rem);
      font-weight: 800;
      letter-spacing: -1px;
      color: var(--charcoal);
      margin-bottom: 6px;
    }
    .section-header p {
      font-size: 0.95rem;
      color: var(--text-secondary);
      max-width: 560px;
    }

    /* ============ SEARCH & FILTERS ============ */
    .search-section { padding: 0 0 32px; }
    .search-bar { position: relative; margin-bottom: 16px; }
    .search-bar input {
      width: 100%;
      padding: 16px 20px 16px 48px;
      border-radius: var(--radius-pill);
      border: 1.5px solid #E2E2E0;
      font-size: 0.95rem;
      font-family: inherit;
      background: var(--white);
      transition: border-color var(--transition), box-shadow var(--transition);
      -webkit-appearance: none;
    }
    .search-bar input:focus {
      outline: none;
      border-color: var(--orange);
      box-shadow: 0 0 0 4px rgba(255,107,43,0.1);
    }
    .search-bar input::placeholder { color: #9ca3af; }
    .search-icon {
      position: absolute;
      left: 18px;
      top: 50%;
      transform: translateY(-50%);
      color: var(--text-secondary);
      font-size: 1rem;
      pointer-events: none;
    }

    .filter-chips {
      display: flex;
      gap: 8px;
      overflow-x: auto;
      padding-bottom: 8px;
      -webkit-overflow-scrolling: touch;
      scrollbar-width: none;
      -ms-overflow-style: none;
    }
    .filter-chips::-webkit-scrollbar { display: none; }
    .filter-chip {
      flex-shrink: 0;
      padding: 8px 18px;
      border-radius: var(--radius-pill);
      border: 1.5px solid #E2E2E0;
      background: var(--white);
      font-size: 0.8rem;
      font-weight: 600;
      color: var(--charcoal-dark);
      transition: all var(--transition);
      white-space: nowrap;
      min-height: 38px;
      touch-action: manipulation;
    }
    .filter-chip:hover, .filter-chip:active {
      border-color: var(--charcoal);
      background: var(--bg-light);
    }
    .filter-chip.active {
      background: var(--charcoal);
      color: var(--white);
      border-color: var(--charcoal);
    }

    /* ============ PRODUCT GRID ============ */
    .products-section { padding: 0 0 48px; }
    .product-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 20px;
    }
    .empty-state {
      grid-column: 1 / -1;
      text-align: center;
      padding: 48px 20px;
      color: var(--text-secondary);
    }
    .empty-state strong {
      display: block;
      font-size: 1.05rem;
      font-weight: 600;
      color: var(--charcoal);
      margin-bottom: 6px;
    }

    /* ============ PRODUCT CARD ============ */
    .product-card {
      background: var(--white);
      border-radius: var(--radius-card);
      overflow: hidden;
      box-shadow: var(--shadow-sm);
      border: 1px solid rgba(0,0,0,0.04);
      transition: transform var(--transition), box-shadow var(--transition);
      display: flex;
      flex-direction: column;
      position: relative;
      cursor: pointer;
    }
    .product-card:hover { transform: translateY(-4px); box-shadow: var(--shadow-lg); }
    .product-card:active { transform: scale(0.995); }

    .card-image-wrap {
      position: relative;
      background: var(--bg-light);
      aspect-ratio: 1 / 1;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .card-image-wrap img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.4s ease;
    }
    .product-card:hover .card-image-wrap img { transform: scale(1.05); }
    .card-image-placeholder {
      font-size: 3.2rem;
      color: #c9c9c9;
      user-select: none;
    }

    .card-badge {
      position: absolute;
      top: 12px;
      left: 12px;
      background: var(--orange);
      color: var(--white);
      font-size: 0.62rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      padding: 5px 11px;
      border-radius: var(--radius-pill);
      box-shadow: 0 4px 12px rgba(255,107,43,0.3);
      z-index: 2;
    }
    .card-badge.badge-trending { background: #EF4444; box-shadow: 0 4px 12px rgba(239,68,68,0.3); }
    .card-badge.badge-top { background: #F59E0B; box-shadow: 0 4px 12px rgba(245,158,11,0.3); }
    .card-badge.badge-new { background: #10B981; box-shadow: 0 4px 12px rgba(16,185,129,0.3); }
    .card-badge.badge-smart { background: #3B82F6; box-shadow: 0 4px 12px rgba(59,130,246,0.3); }
    .card-badge.badge-alert { background: #8B5CF6; box-shadow: 0 4px 12px rgba(139,92,246,0.3); }

    .card-body {
      padding: 16px;
      display: flex;
      flex-direction: column;
      gap: 8px;
      flex: 1;
    }
    .card-category {
      font-size: 0.68rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.7px;
      color: var(--orange);
    }
    .card-title {
      font-size: 0.95rem;
      font-weight: 700;
      color: var(--charcoal);
      line-height: 1.3;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
      min-height: 2.6em;
    }
    .card-rating {
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: 0.78rem;
      color: var(--text-secondary);
    }
    .card-rating .stars { color: #F59E0B; font-size: 0.82rem; }

    .card-prices {
      display: flex;
      align-items: baseline;
      gap: 8px;
      flex-wrap: wrap;
    }
    .card-price-current {
      font-size: 1.15rem;
      font-weight: 800;
      color: var(--charcoal);
    }
    .card-price-previous {
      font-size: 0.82rem;
      color: var(--text-secondary);
      text-decoration: line-through;
    }
    .card-discount {
      font-size: 0.68rem;
      font-weight: 700;
      color: #10B981;
      background: rgba(16,185,129,0.1);
      padding: 2px 8px;
      border-radius: var(--radius-pill);
    }

    .card-desc {
      font-size: 0.8rem;
      color: var(--text-secondary);
      line-height: 1.45;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
      overflow: hidden;
    }

    .card-cta {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      margin-top: auto;
      padding: 12px 16px;
      background: var(--charcoal);
      color: var(--white);
      border-radius: var(--radius-pill);
      font-weight: 600;
      font-size: 0.85rem;
      transition: all var(--transition);
      min-height: 44px;
      touch-action: manipulation;
      border: none;
      width: 100%;
    }
    .card-cta:hover, .card-cta:active {
      background: var(--orange);
      transform: translateY(-1px);
      box-shadow: var(--shadow-orange);
    }

    /* ============ TRANSPARENCY ============ */
    .transparency-section {
      padding: 0 0 40px;
    }
    .transparency-box {
      background: var(--bg-light);
      border-radius: var(--radius-card);
      padding: 20px 22px;
      display: flex;
      align-items: flex-start;
      gap: 14px;
      border: 1px solid rgba(0,0,0,0.04);
    }
    .transparency-icon {
      font-size: 1.4rem;
      line-height: 1;
      flex-shrink: 0;
    }
    .transparency-text {
      font-size: 0.82rem;
      color: var(--text-secondary);
      line-height: 1.6;
    }
    .transparency-text strong { color: var(--charcoal); font-weight: 700; }

    /* ============ CATEGORIES ============ */
    .categories-section {
      padding: 48px 0;
      background: var(--bg-light);
    }
    .category-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
    }
    .category-card {
      background: var(--white);
      border-radius: var(--radius-card);
      padding: 20px 16px;
      display: flex;
      flex-direction: column;
      gap: 8px;
      transition: transform var(--transition), box-shadow var(--transition);
      cursor: pointer;
      border: 1px solid rgba(0,0,0,0.04);
      touch-action: manipulation;
      min-height: 120px;
      text-align: left;
    }
    .category-card:hover, .category-card:active {
      transform: translateY(-3px);
      box-shadow: var(--shadow-md);
      border-color: rgba(255,107,43,0.2);
    }
    .category-icon { font-size: 1.9rem; line-height: 1; }
    .category-name {
      font-size: 0.9rem;
      font-weight: 700;
      color: var(--charcoal);
      line-height: 1.2;
    }
    .category-desc {
      font-size: 0.75rem;
      color: var(--text-secondary);
      line-height: 1.35;
    }

    /* ============ WHY DEALFORGE ============ */
    .why-section { padding: 48px 0; }
    .why-grid { display: grid; grid-template-columns: 1fr; gap: 16px; }
    .why-card {
      background: var(--white);
      border-radius: var(--radius-card);
      padding: 24px 22px;
      border: 1px solid rgba(0,0,0,0.05);
      box-shadow: var(--shadow-sm);
      transition: transform var(--transition), box-shadow var(--transition);
    }
    .why-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-md); }
    .why-icon { font-size: 2rem; margin-bottom: 12px; display: block; }
    .why-card h3 {
      font-size: 1rem;
      font-weight: 700;
      margin-bottom: 6px;
      color: var(--charcoal);
      letter-spacing: -0.2px;
    }
    .why-card p { font-size: 0.85rem; color: var(--text-secondary); line-height: 1.55; }

    /* ============ HOW IT WORKS ============ */
    .how-section {
      padding: 56px 0;
      background: var(--charcoal);
      color: var(--white);
    }
    .how-section .section-header h2 { color: var(--white); }
    .how-section .section-header p { color: rgba(255,255,255,0.6); }

    .how-steps { display: grid; grid-template-columns: 1fr; gap: 20px; }
    .how-step {
      background: rgba(255,255,255,0.06);
      border-radius: var(--radius-card);
      padding: 28px 24px;
      border: 1px solid rgba(255,255,255,0.08);
      transition: background var(--transition), transform var(--transition);
    }
    .how-step:hover {
      background: rgba(255,255,255,0.1);
      transform: translateY(-3px);
    }
    .step-number {
      font-size: 2.4rem;
      font-weight: 800;
      color: var(--orange);
      line-height: 1;
      margin-bottom: 14px;
      opacity: 0.95;
      letter-spacing: -1px;
    }
    .how-step h3 { font-size: 1.1rem; font-weight: 700; margin-bottom: 8px; }
    .how-step p { font-size: 0.9rem; color: rgba(255,255,255,0.72); line-height: 1.55; }
    .how-headline {
      text-align: center;
      font-size: clamp(1.3rem, 4.5vw, 1.7rem);
      font-weight: 700;
      margin-top: 36px;
      color: var(--white);
      letter-spacing: -0.6px;
    }

    /* ============ COMMUNITY ============ */
    .community-section { padding: 56px 0; }
    .community-card {
      background: linear-gradient(135deg, #FFF6F1 0%, #FFFFFF 100%);
      border-radius: 24px;
      padding: 40px 24px;
      text-align: center;
      border: 1px solid rgba(255,107,43,0.14);
    }
    .community-card h2 {
      font-size: clamp(1.4rem, 5.5vw, 2.1rem);
      font-weight: 800;
      margin-bottom: 12px;
      letter-spacing: -1px;
    }
    .community-card p {
      font-size: 0.95rem;
      color: var(--text-secondary);
      max-width: 520px;
      margin: 0 auto 26px;
      line-height: 1.6;
    }
    .social-buttons {
      display: flex;
      flex-direction: column;
      gap: 10px;
      max-width: 340px;
      margin: 0 auto;
    }
    .social-btn {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 14px 20px;
      border-radius: var(--radius-pill);
      font-weight: 600;
      font-size: 0.9rem;
      transition: all var(--transition);
      min-height: 48px;
      touch-action: manipulation;
      width: 100%;
      color: var(--white);
    }
    .social-btn.tiktok { background: var(--charcoal); }
    .social-btn.instagram {
      background: linear-gradient(45deg, #F09433, #E6683C, #DC2743, #CC2366, #BC1888);
    }
    .social-btn.telegram { background: #0088CC; }
    .social-btn:hover, .social-btn:active {
      transform: translateY(-2px);
      box-shadow: var(--shadow-md);
      filter: brightness(1.05);
    }

    /* ============ EMAIL ============ */
    .email-section { padding: 0 0 56px; }
    .email-card {
      background: var(--bg-light);
      border-radius: 24px;
      padding: 36px 24px;
      text-align: center;
    }
    .email-card h3 {
      font-size: 1.25rem;
      font-weight: 800;
      margin-bottom: 8px;
      letter-spacing: -0.4px;
    }
    .email-card p {
      font-size: 0.9rem;
      color: var(--text-secondary);
      margin-bottom: 20px;
      line-height: 1.5;
    }
    .email-form {
      display: flex;
      flex-direction: column;
      gap: 10px;
      max-width: 420px;
      margin: 0 auto;
    }
    .email-form input {
      padding: 14px 20px;
      border-radius: var(--radius-pill);
      border: 1.5px solid #E2E2E0;
      font-size: 0.9rem;
      font-family: inherit;
      background: var(--white);
      transition: border-color var(--transition), box-shadow var(--transition);
      min-height: 48px;
      -webkit-appearance: none;
    }
    .email-form input:focus {
      outline: none;
      border-color: var(--orange);
      box-shadow: 0 0 0 4px rgba(255,107,43,0.1);
    }
    .email-form button {
      padding: 14px 24px;
      border-radius: var(--radius-pill);
      background: var(--orange);
      color: var(--white);
      font-weight: 600;
      font-size: 0.9rem;
      transition: all var(--transition);
      min-height: 48px;
      touch-action: manipulation;
      box-shadow: var(--shadow-orange);
    }
    .email-form button:hover, .email-form button:active {
      background: var(--orange-dark);
      transform: translateY(-1px);
      box-shadow: 0 8px 24px rgba(255,107,43,0.42);
    }
    .email-note {
      font-size: 0.72rem;
      color: var(--text-secondary);
      margin-top: 14px;
      opacity: 0.85;
      display: block;
    }

    /* ============ FOOTER ============ */
    .site-footer {
      background: var(--charcoal);
      color: rgba(255,255,255,0.72);
      padding: 56px 0 120px;
    }
    .footer-brand { margin-bottom: 32px; }
    .footer-brand .logo {
      color: var(--white);
      margin-bottom: 10px;
      font-size: 1.3rem;
    }
    .footer-tagline {
      font-size: 0.85rem;
      color: rgba(255,255,255,0.55);
      font-weight: 500;
      letter-spacing: 0.3px;
    }
    .footer-links {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 28px;
      margin-bottom: 36px;
    }
    .footer-col h4 {
      font-size: 0.75rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1.2px;
      color: var(--white);
      margin-bottom: 14px;
    }
    .footer-col a {
      display: block;
      font-size: 0.85rem;
      color: rgba(255,255,255,0.6);
      padding: 5px 0;
      transition: color var(--transition);
    }
    .footer-col a:hover { color: var(--orange); }

    .footer-social {
      display: flex;
      gap: 12px;
      margin-bottom: 32px;
    }
    .footer-social a {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 42px;
      height: 42px;
      border-radius: 50%;
      background: rgba(255,255,255,0.08);
      color: var(--white);
      font-size: 1.05rem;
      transition: background var(--transition), transform var(--transition);
    }
    .footer-social a:hover {
      background: var(--orange);
      transform: translateY(-2px);
    }

    .footer-disclaimer {
      font-size: 0.72rem;
      color: rgba(255,255,255,0.45);
      line-height: 1.6;
      padding-top: 28px;
      border-top: 1px solid rgba(255,255,255,0.08);
    }
    .footer-disclaimer p { margin-bottom: 10px; }
    .footer-disclaimer p:last-child { margin-bottom: 0; }

    /* ============ MOBILE BOTTOM NAV ============ */
    .mobile-bottom-nav {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      background: rgba(255,255,255,0.97);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      border-top: 1px solid rgba(0,0,0,0.06);
      display: flex;
      justify-content: space-around;
      align-items: center;
      padding: 6px 0 calc(6px + env(safe-area-inset-bottom, 0px));
      z-index: 1000;
    }
    .mobile-bottom-nav a {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 2px;
      padding: 8px 12px;
      font-size: 0.6rem;
      font-weight: 600;
      color: var(--text-secondary);
      transition: color var(--transition);
      min-width: 60px;
      min-height: 44px;
      touch-action: manipulation;
    }
    .mobile-bottom-nav a .nav-icon { font-size: 1.2rem; line-height: 1; }
    .mobile-bottom-nav a.active,
    .mobile-bottom-nav a:hover { color: var(--orange); }

    /* ============ MODAL ============ */
    .modal-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.55);
      backdrop-filter: blur(4px);
      -webkit-backdrop-filter: blur(4px);
      z-index: 2000;
      display: flex;
      align-items: flex-end;
      justify-content: center;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s ease;
    }
    .modal-overlay.open { opacity: 1; pointer-events: auto; }

    .modal-content {
      background: var(--white);
      border-radius: 24px 24px 0 0;
      width: 100%;
      max-width: 640px;
      max-height: 92vh;
      overflow-y: auto;
      padding: 20px 20px 32px;
      transform: translateY(100%);
      transition: transform 0.4s cubic-bezier(0.2, 0.9, 0.4, 1);
      -webkit-overflow-scrolling: touch;
      position: relative;
    }
    .modal-overlay.open .modal-content { transform: translateY(0); }

    .modal-close {
      position: absolute;
      top: 16px;
      right: 16px;
      width: 38px;
      height: 38px;
      border-radius: 50%;
      background: var(--bg-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      color: var(--charcoal);
      transition: background var(--transition);
      z-index: 10;
      touch-action: manipulation;
    }
    .modal-close:hover { background: #e6e6e6; }

    .modal-image {
      width: 100%;
      aspect-ratio: 16 / 12;
      border-radius: 16px;
      background: var(--bg-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 5rem;
      color: #c9c9c9;
      margin-bottom: 22px;
      overflow: hidden;
    }
    .modal-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .modal-category {
      font-size: 0.72rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.7px;
      color: var(--orange);
      margin-bottom: 8px;
    }
    .modal-title {
      font-size: 1.4rem;
      font-weight: 800;
      line-height: 1.2;
      margin-bottom: 12px;
      letter-spacing: -0.5px;
      padding-right: 40px;
    }
    .modal-rating {
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 0.85rem;
      color: var(--text-secondary);
      margin-bottom: 16px;
    }
    .modal-rating .stars { color: #F59E0B; }

    .modal-prices {
      display: flex;
      align-items: baseline;
      gap: 10px;
      flex-wrap: wrap;
      margin-bottom: 22px;
      padding-bottom: 22px;
      border-bottom: 1px solid #ECECEC;
    }
    .modal-price-current {
      font-size: 1.65rem;
      font-weight: 800;
      color: var(--charcoal);
      letter-spacing: -0.5px;
    }
    .modal-price-previous {
      font-size: 1rem;
      color: var(--text-secondary);
      text-decoration: line-through;
    }
    .modal-discount {
      font-size: 0.78rem;
      font-weight: 700;
      color: #10B981;
      background: rgba(16,185,129,0.1);
      padding: 4px 12px;
      border-radius: var(--radius-pill);
    }

    .modal-section { margin-bottom: 22px; }
    .modal-section h4 {
      font-size: 0.78rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.8px;
      color: var(--charcoal);
      margin-bottom: 10px;
    }
    .modal-section p {
      font-size: 0.9rem;
      color: var(--text-secondary);
      line-height: 1.65;
    }
    .modal-section ul {
      display: flex;
      flex-direction: column;
      gap: 8px;
    }
    .modal-section ul li {
      font-size: 0.88rem;
      color: var(--text-secondary);
      padding-left: 22px;
      position: relative;
      line-height: 1.5;
    }
    .modal-section ul li::before {
      content: '';
      position: absolute;
      left: 4px;
      top: 9px;
      width: 6px;
      height: 6px;
      background: var(--orange);
      border-radius: 50%;
    }

    .modal-cta {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      width: 100%;
      padding: 16px;
      background: var(--orange);
      color: var(--white);
      border-radius: var(--radius-pill);
      font-weight: 700;
      font-size: 0.98rem;
      transition: all var(--transition);
      min-height: 52px;
      touch-action: manipulation;
      margin-top: 8px;
      box-shadow: var(--shadow-orange);
    }
    .modal-cta:hover, .modal-cta:active {
      background: var(--orange-dark);
      transform: translateY(-1px);
      box-shadow: 0 10px 28px rgba(255,107,43,0.42);
    }

    .modal-disclaimer {
      font-size: 0.7rem;
      color: var(--text-secondary);
      text-align: center;
      margin-top: 16px;
      opacity: 0.85;
      line-height: 1.6;
      padding: 12px 8px 0;
      border-top: 1px solid #ECECEC;
    }

    /* ============================================================
       DEALFORGE AGENT
       ============================================================ */
    .agent-section {
      padding: 64px 0;
      background: #FAFAF8;
      border-top: 1px solid rgba(0,0,0,0.05);
    }
    .agent-shell {
      background: var(--charcoal);
      color: var(--white);
      border-radius: 26px;
      padding: 28px 20px;
      box-shadow: var(--shadow-lg);
      position: relative;
      overflow: hidden;
    }
    .agent-shell::before {
      content: '';
      position: absolute;
      width: 300px;
      height: 300px;
      right: -120px;
      top: -130px;
      background: radial-gradient(circle, rgba(255,107,43,0.22) 0%, transparent 70%);
      pointer-events: none;
    }
    .agent-header { position: relative; z-index: 1; margin-bottom: 28px; }
    .agent-label {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      background: rgba(255,107,43,0.15);
      color: #FF8A55;
      padding: 6px 12px;
      border-radius: var(--radius-pill);
      font-size: 0.68rem;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 0.8px;
      margin-bottom: 14px;
    }
    .agent-header h2 {
      color: var(--white);
      font-size: clamp(1.7rem, 6vw, 2.5rem);
      line-height: 1.1;
      letter-spacing: -1px;
      margin-bottom: 10px;
    }
    .agent-header p {
      color: rgba(255,255,255,0.65);
      font-size: 0.92rem;
      max-width: 620px;
      line-height: 1.6;
    }
    .agent-grid {
      position: relative;
      z-index: 1;
      display: grid;
      grid-template-columns: 1fr;
      gap: 18px;
    }
    .agent-panel {
      background: rgba(255,255,255,0.07);
      border: 1px solid rgba(255,255,255,0.09);
      border-radius: 20px;
      padding: 20px;
    }
    .agent-panel h3 {
      color: var(--white);
      font-size: 0.95rem;
      margin-bottom: 16px;
    }
    .agent-input-group { margin-bottom: 14px; }
    .agent-input-group label {
      display: block;
      font-size: 0.7rem;
      font-weight: 700;
      color: rgba(255,255,255,0.6);
      text-transform: uppercase;
      letter-spacing: 0.7px;
      margin-bottom: 7px;
    }
    .agent-input,
    .agent-select {
      width: 100%;
      min-height: 46px;
      padding: 12px 14px;
      border-radius: 12px;
      border: 1px solid rgba(255,255,255,0.12);
      background: rgba(255,255,255,0.08);
      color: var(--white);
      font-family: inherit;
      font-size: 0.88rem;
      outline: none;
    }
    .agent-input::placeholder { color: rgba(255,255,255,0.35); }
    .agent-input:focus,
    .agent-select:focus {
      border-color: var(--orange);
      box-shadow: 0 0 0 3px rgba(255,107,43,0.12);
    }
    .agent-select option { color: var(--charcoal); background: var(--white); }
    .agent-two-column {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
    }
    .agent-run-btn {
      width: 100%;
      min-height: 50px;
      border-radius: var(--radius-pill);
      background: var(--orange);
      color: var(--white);
      font-weight: 800;
      font-size: 0.9rem;
      box-shadow: var(--shadow-orange);
      transition: all var(--transition);
      margin-top: 4px;
    }
    .agent-run-btn:hover {
      background: var(--orange-dark);
      transform: translateY(-2px);
    }
    .agent-run-btn:disabled { opacity: 0.65; cursor: wait; transform: none; }
    .agent-status {
      margin-top: 12px;
      min-height: 20px;
      font-size: 0.72rem;
      color: rgba(255,255,255,0.55);
      text-align: center;
    }
    .agent-results { display: none; }
    .agent-results.visible { display: block; }
    .agent-result-top {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      gap: 12px;
      margin-bottom: 14px;
    }
    .agent-result-name { font-size: 1.05rem; font-weight: 800; line-height: 1.3; }
    .agent-score {
      min-width: 62px;
      height: 62px;
      border-radius: 50%;
      background: rgba(255,107,43,0.15);
      border: 2px solid var(--orange);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }
    .agent-score strong { font-size: 1.1rem; line-height: 1; color: var(--orange); }
    .agent-score span { font-size: 0.52rem; color: rgba(255,255,255,0.55); margin-top: 3px; }
    .agent-verdict {
      padding: 11px 13px;
      border-radius: 12px;
      background: rgba(255,255,255,0.06);
      color: rgba(255,255,255,0.78);
      font-size: 0.78rem;
      line-height: 1.5;
      margin-bottom: 16px;
    }
    .agent-verdict strong { color: var(--white); }
    .agent-metrics {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 8px;
      margin-bottom: 18px;
    }
    .agent-metric {
      background: rgba(255,255,255,0.05);
      border-radius: 12px;
      padding: 11px;
    }
    .agent-metric span {
      display: block;
      font-size: 0.6rem;
      color: rgba(255,255,255,0.48);
      margin-bottom: 3px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }
    .agent-metric strong { font-size: 0.82rem; color: var(--white); }
    .agent-output { margin-top: 16px; }
    .agent-output h4 {
      font-size: 0.68rem;
      text-transform: uppercase;
      letter-spacing: 0.8px;
      color: var(--orange);
      margin-bottom: 8px;
    }
    .agent-copy-box {
      background: rgba(0,0,0,0.2);
      border: 1px solid rgba(255,255,255,0.07);
      border-radius: 12px;
      padding: 13px;
      font-size: 0.78rem;
      line-height: 1.55;
      color: rgba(255,255,255,0.78);
      white-space: pre-wrap;
    }
    .agent-actions {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      margin-top: 10px;
    }
    .agent-action-btn {
      min-height: 42px;
      border-radius: 10px;
      background: rgba(255,255,255,0.08);
      color: var(--white);
      border: 1px solid rgba(255,255,255,0.08);
      font-size: 0.72rem;
      font-weight: 700;
      transition: all var(--transition);
    }
    .agent-action-btn:hover { background: rgba(255,255,255,0.14); }
    .agent-action-btn.approve {
      background: rgba(16,185,129,0.14);
      color: #6EE7B7;
    }
    .agent-action-btn.approve:hover { background: rgba(16,185,129,0.22); }
    .agent-approved {
      margin-top: 12px;
      display: none;
      padding: 10px 12px;
      border-radius: 10px;
      background: rgba(16,185,129,0.12);
      color: #6EE7B7;
      font-size: 0.72rem;
      font-weight: 700;
    }
    .agent-approved.show { display: block; }
    .agent-disclaimer {
      position: relative;
      z-index: 1;
      margin-top: 18px;
      font-size: 0.65rem;
      color: rgba(255,255,255,0.4);
      line-height: 1.5;
    }

    /* ============ RESPONSIVE ============ */
    @media (min-width: 375px) {
      .product-grid { grid-template-columns: repeat(2, 1fr); gap: 14px; }
      .category-grid { gap: 14px; }
    }
    @media (min-width: 480px) {
      .social-buttons {
        flex-direction: row;
        max-width: 100%;
        justify-content: center;
        flex-wrap: wrap;
      }
      .social-btn { width: auto; flex: 1; min-width: 150px; }
    }
    @media (min-width: 640px) {
      .why-grid { grid-template-columns: repeat(2, 1fr); }
      .how-steps { grid-template-columns: repeat(3, 1fr); }
      .footer-links { grid-template-columns: repeat(3, 1fr); }
      .category-grid { grid-template-columns: repeat(3, 1fr); }
      .modal-image { aspect-ratio: 16 / 10; }
    }
    @media (min-width: 768px) {
      .header-inner { height: 70px; }
      .desktop-nav { display: flex; }
      .desktop-cta { display: inline-flex; }
      .mobile-menu-btn { display: none; }
      .mobile-nav { display: none; }
      .mobile-bottom-nav { display: none; }
      .site-footer { padding-bottom: 56px; }
      .hero { padding: 70px 0 90px; }
      .hero .container { flex-direction: row; align-items: center; gap: 60px; }
      .hero-content { flex: 1; }
      .hero-visual { flex: 1; min-height: 340px; }
      .floating-cards { max-width: 420px; }
      .float-card { padding: 18px; }
      .product-grid { grid-template-columns: repeat(3, 1fr); gap: 22px; }
      .category-grid { grid-template-columns: repeat(6, 1fr); }
      .why-grid { grid-template-columns: repeat(4, 1fr); }
      .modal-overlay { align-items: center; padding: 20px; }
      .modal-content {
        border-radius: 24px;
        max-height: 88vh;
        padding: 28px 28px 36px;
      }
      .email-form { flex-direction: row; }
      .email-form input { flex: 1; }
      .email-form button { flex-shrink: 0; width: auto; padding: 14px 28px; }
      .agent-shell { padding: 38px; }
      .agent-grid {
        grid-template-columns: minmax(280px, 0.8fr) minmax(320px, 1.2fr);
      }
    }
    @media (min-width: 1024px) {
      .product-grid { grid-template-columns: repeat(3, 1fr); gap: 24px; }
      .hero h1 { font-size: 3.75rem; }
      .hero p { font-size: 1.12rem; }
      .agent-shell { padding: 44px; }
    }
    @media (min-width: 1440px) {
      .container { max-width: 1280px; }
      .product-grid { grid-template-columns: repeat(3, 1fr); gap: 28px; }
      .hero h1 { font-size: 4.2rem; }
    }

    /* ============ ANIMATIONS ============ */
    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .fade-in-up { animation: fadeInUp 0.7s ease forwards; opacity: 0; }
    .fade-in-up-delay-2 { animation-delay: 0.2s; }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
        scroll-behavior: auto !important;
      }
      .float-card { animation: none; }
    }

    a:focus-visible, button:focus-visible, input:focus-visible, select:focus-visible {
      outline: 2px solid var(--orange);
      outline-offset: 2px;
    }
  </style>
</head>
<body>

  <!-- ============ HEADER ============ -->
  <header class="site-header" id="siteHeader">
    <div class="header-inner">
      <a href="#" class="logo" aria-label="DealForge NG home">DealForge<span>NG</span></a>

      <nav class="desktop-nav" aria-label="Main navigation">
        <a href="#deals">Deals</a>
        <a href="#categories">Categories</a>
        <a href="#how-it-works">How It Works</a>
        <a href="#community">Community</a>
      </nav>

      <a href="#deals" class="desktop-cta">Explore Deals</a>

      <button class="mobile-menu-btn" id="mobileMenuBtn" aria-label="Toggle menu" aria-expanded="false">
        <span></span><span></span><span></span>
      </button>
    </div>

    <nav class="mobile-nav" id="mobileNav" aria-label="Mobile navigation">
      <a href="#deals">Deals</a>
      <a href="#categories">Categories</a>
      <a href="#how-it-works">How It Works</a>
      <a href="#community">Community</a>
      <a href="#deals" class="mobile-cta">Explore Deals</a>
    </nav>
  </header>

  <main>
    <!-- ============ HERO ============ -->
    <section class="hero" aria-labelledby="hero-heading">
      <div class="container">
        <div class="hero-content fade-in-up">
          <div class="hero-badge">Product Discovery</div>
          <h1 id="hero-heading">Deals worth <span class="highlight">knowing.</span></h1>
          <p>Discover interesting products, useful gadgets and deals worth checking out — without endlessly searching.</p>
          <div class="hero-tagline">We find it. You decide.</div>
          <div class="hero-ctas">
            <a href="#deals" class="btn btn-primary">Explore Today's Deals</a>
            <a href="#community" class="btn btn-secondary">Join Our Community</a>
          </div>
        </div>

        <div class="hero-visual fade-in-up fade-in-up-delay-2" aria-hidden="true">
          <div class="floating-cards">
            <div class="float-card">
              <div class="float-card-icon">🔋</div>
              <div class="float-card-title">Power Bank</div>
              <div class="float-card-price">₦15,720</div>
              <div class="float-card-tag">🔥 Trending</div>
            </div>
            <div class="float-card">
              <div class="float-card-icon">🎧</div>
              <div class="float-card-title">Earhook Earbuds</div>
              <div class="float-card-price">Check price</div>
              <div class="float-card-tag">⭐ Top Pick</div>
            </div>
            <div class="float-card">
              <div class="float-card-icon">📸</div>
              <div class="float-card-title">Selfie Tripod</div>
              <div class="float-card-price">Check price</div>
              <div class="float-card-tag">💡 Smart Find</div>
            </div>
            <div class="float-card">
              <div class="float-card-icon">⚡</div>
              <div class="float-card-title">Deal Alert</div>
              <div class="float-card-price">New finds daily</div>
              <div class="float-card-tag">🆕 New</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ============ SEARCH & FILTERS ============ -->
    <section class="search-section" aria-label="Search and filter products">
      <div class="container">
        <div class="search-bar">
          <span class="search-icon" aria-hidden="true">🔍</span>
          <input type="search" id="searchInput" placeholder="Search products, gadgets and deals…" aria-label="Search products">
        </div>
        <div class="filter-chips" role="group" aria-label="Filter products by category">
          <button class="filter-chip active" data-filter="all">All</button>
          <button class="filter-chip" data-filter="Tech &amp; Gadgets">Tech &amp; Gadgets</button>
          <button class="filter-chip" data-filter="Audio">Audio</button>
          <button class="filter-chip" data-filter="Home">Home</button>
          <button class="filter-chip" data-filter="Work &amp; Study">Work &amp; Study</button>
          <button class="filter-chip" data-filter="Trending">Trending</button>
          <button class="filter-chip" data-filter="Smart Finds">Smart Finds</button>
        </div>
      </div>
    </section>

    <!-- ============ DEALFORGE AGENT ============ -->
    <section class="agent-section" id="agent" aria-labelledby="agent-heading">
      <div class="container">
        <div class="agent-shell">

          <div class="agent-header">
            <div class="agent-label">🤖 DealForge Agent · V1</div>
            <h2 id="agent-heading">Find the next deal worth knowing.</h2>
            <p>Give the Agent a product idea and a budget. It will analyze the opportunity, score the find and generate content ready for TikTok or WhatsApp.</p>
          </div>

          <div class="agent-grid">

            <!-- INPUT PANEL -->
            <div class="agent-panel">
              <h3>🔎 Deal Hunter</h3>

              <div class="agent-input-group">
                <label for="agentProduct">Product / Deal</label>
                <input class="agent-input" id="agentProduct" type="text" placeholder="e.g. wireless earbuds">
              </div>

              <div class="agent-two-column">
                <div class="agent-input-group">
                  <label for="agentBudget">Budget</label>
                  <input class="agent-input" id="agentBudget" type="number" min="0" placeholder="15000">
                </div>
                <div class="agent-input-group">
                  <label for="agentRating">Min Rating</label>
                  <select class="agent-select" id="agentRating">
                    <option value="0">Any</option>
                    <option value="3">3.0+</option>
                    <option value="3.5">3.5+</option>
                    <option value="4">4.0+</option>
                    <option value="4.5">4.5+</option>
                  </select>
                </div>
              </div>

              <div class="agent-input-group">
                <label for="agentCategory">Category</label>
                <select class="agent-select" id="agentCategory">
                  <option value="Tech &amp; Gadgets">Tech &amp; Gadgets</option>
                  <option value="Audio">Audio</option>
                  <option value="Home">Home</option>
                  <option value="Work &amp; Study">Work &amp; Study</option>
                  <option value="Trending">Trending</option>
                  <option value="Smart Finds">Smart Finds</option>
                </select>
              </div>

              <div class="agent-input-group">
                <label for="agentAffiliate">Affiliate Link</label>
                <input class="agent-input" id="agentAffiliate" type="url" placeholder="Paste affiliate link (optional)">
              </div>

              <button class="agent-run-btn" id="runAgentBtn">⚡ Analyze Find</button>
              <div class="agent-status" id="agentStatus">Ready.</div>
            </div>

            <!-- RESULTS PANEL -->
            <div class="agent-panel">
              <h3>🧠 Agent Analysis</h3>

              <div class="agent-results" id="agentResults">
                <div class="agent-result-top">
                  <div>
                    <div class="agent-result-name" id="agentResultName">—</div>
                  </div>
                  <div class="agent-score">
                    <strong id="agentScore">—</strong>
                    <span>/ 100</span>
                  </div>
                </div>

                <div class="agent-verdict" id="agentVerdict">—</div>

                <div class="agent-metrics">
                  <div class="agent-metric"><span>Usefulness</span><strong id="metricUsefulness">—</strong></div>
                  <div class="agent-metric"><span>Value</span><strong id="metricValue">—</strong></div>
                  <div class="agent-metric"><span>Content Potential</span><strong id="metricContent">—</strong></div>
                  <div class="agent-metric"><span>Risk</span><strong id="metricRisk">—</strong></div>
                </div>

                <div class="agent-output">
                  <h4>TikTok Hook</h4>
                  <div class="agent-copy-box" id="agentTikTok">—</div>
                  <div class="agent-actions">
                    <button class="agent-action-btn" id="copyTikTok">Copy TikTok</button>
                    <button class="agent-action-btn approve" id="approveDeal">✓ Approve Find</button>
                  </div>
                </div>

                <div class="agent-output">
                  <h4>WhatsApp Copy</h4>
                  <div class="agent-copy-box" id="agentWhatsApp">—</div>
                  <div class="agent-actions">
                    <button class="agent-action-btn" id="copyWhatsApp">Copy WhatsApp</button>
                  </div>
                </div>

                <div class="agent-approved" id="agentApproved">✓ Find approved and saved in this browser.</div>
              </div>

              <div id="agentEmptyState" style="text-align:center;padding:42px 15px;color:rgba(255,255,255,0.38);font-size:0.78rem;line-height:1.6;">
                Enter a product above and let<br>DealForge analyze the opportunity.
              </div>
            </div>

          </div>

          <div class="agent-disclaimer">
            DealForge Agent V1 uses the information you provide to produce an analysis and content draft. It does not automatically purchase, publish, message customers or make financial decisions for you. Verify product information and retailer details before publishing.
          </div>

        </div>
      </div>
    </section>

    <!-- ============ PRODUCTS ============ -->
    <section class="products-section" id="deals" aria-labelledby="deals-heading">
      <div class="container">
        <div class="section-header">
          <h2 id="deals-heading">Today's Picks 🔥</h2>
          <p>Interesting finds we've spotted for you.</p>
        </div>
        <div class="product-grid" id="productGrid"></div>
      </div>
    </section>

    <!-- ============ TRANSPARENCY ============ -->
    <section class="transparency-section" aria-label="Affiliate disclosure">
      <div class="container">
        <div class="transparency-box">
          <span class="transparency-icon" aria-hidden="true">🔗</span>
          <p class="transparency-text">
            <strong>Transparency:</strong> DealForge may earn a commission when you purchase through certain links. This does not affect the price you pay. We discover and highlight products — the actual purchase happens on the retailer's platform.
          </p>
        </div>
      </div>
    </section>

    <!-- ============ CATEGORIES ============ -->
    <section class="categories-section" id="categories" aria-labelledby="categories-heading">
      <div class="container">
        <div class="section-header">
          <h2 id="categories-heading">Browse Categories</h2>
          <p>Find products by what you're looking for.</p>
        </div>
        <div class="category-grid">
          <button class="category-card" data-category="Tech &amp; Gadgets">
            <span class="category-icon">📱</span>
            <span class="category-name">Tech &amp; Gadgets</span>
            <span class="category-desc">Phones, accessories and useful technology.</span>
          </button>
          <button class="category-card" data-category="Audio">
            <span class="category-icon">🎧</span>
            <span class="category-name">Audio</span>
            <span class="category-desc">Earbuds, headphones and speakers.</span>
          </button>
          <button class="category-card" data-category="Home">
            <span class="category-icon">🏠</span>
            <span class="category-name">Home</span>
            <span class="category-desc">Useful products for everyday living.</span>
          </button>
          <button class="category-card" data-category="Work &amp; Study">
            <span class="category-icon">💻</span>
            <span class="category-name">Work &amp; Study</span>
            <span class="category-desc">Products useful for students and productivity.</span>
          </button>
          <button class="category-card" data-category="Trending">
            <span class="category-icon">🔥</span>
            <span class="category-name">Trending</span>
            <span class="category-desc">Products currently getting attention.</span>
          </button>
          <button class="category-card" data-category="Smart Finds">
            <span class="category-icon">💰</span>
            <span class="category-name">Smart Finds</span>
            <span class="category-desc">Interesting products at attractive prices.</span>
          </button>
        </div>
      </div>
    </section>

    <!-- ============ WHY DEALFORGE ============ -->
    <section class="why-section" aria-labelledby="why-heading">
      <div class="container">
        <div class="section-header">
          <h2 id="why-heading">Why DealForge?</h2>
          <p>We do the searching. You make the call.</p>
        </div>
        <div class="why-grid">
          <div class="why-card">
            <span class="why-icon" aria-hidden="true">🔎</span>
            <h3>We Search</h3>
            <p>We look through products and interesting finds so you don't have to search endlessly.</p>
          </div>
          <div class="why-card">
            <span class="why-icon" aria-hidden="true">📊</span>
            <h3>We Check</h3>
            <p>We look at useful information such as ratings, features and available details.</p>
          </div>
          <div class="why-card">
            <span class="why-icon" aria-hidden="true">💡</span>
            <h3>We Highlight</h3>
            <p>We bring attention to products that appear worth checking out.</p>
          </div>
          <div class="why-card">
            <span class="why-icon" aria-hidden="true">🤝</span>
            <h3>You Decide</h3>
            <p>We provide the information. You make the final decision.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ============ HOW IT WORKS ============ -->
    <section class="how-section" id="how-it-works" aria-labelledby="how-heading">
      <div class="container">
        <div class="section-header">
          <h2 id="how-heading">Simple. Transparent. Useful.</h2>
          <p>Three steps to a smarter decision.</p>
        </div>
        <div class="how-steps">
          <div class="how-step">
            <div class="step-number">01</div>
            <h3>Discover</h3>
            <p>Find interesting products and deals.</p>
          </div>
          <div class="how-step">
            <div class="step-number">02</div>
            <h3>Check</h3>
            <p>Review the product information and important considerations.</p>
          </div>
          <div class="how-step">
            <div class="step-number">03</div>
            <h3>Decide</h3>
            <p>Choose whether the product is worth checking out.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ============ COMMUNITY ============ -->
    <section class="community-section" id="community" aria-labelledby="community-heading">
      <div class="container">
        <div class="community-card">
          <h2 id="community-heading">Don't miss the next find.</h2>
          <p>Follow DealForge for new product discoveries, useful finds and deals worth knowing.</p>
          <div class="social-buttons">
            <a href="https://www.tiktok.com/@dealforge.ng" class="social-btn tiktok" target="_blank" rel="noopener noreferrer">
              <span aria-hidden="true">🎵</span> Follow on TikTok
            </a>
            <a href="https://www.instagram.com/dealforge.ng" class="social-btn instagram" target="_blank" rel="noopener noreferrer">
              <span aria-hidden="true">📸</span> Follow on Instagram
            </a>
            <a href="https://t.me/dealforgeng1" class="social-btn telegram" target="_blank" rel="noopener noreferrer">
              <span aria-hidden="true">✈️</span> Join on Telegram
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- ============ EMAIL ============ -->
    <section class="email-section" aria-labelledby="email-heading">
      <div class="container">
        <div class="email-card">
          <h3 id="email-heading">Get the next interesting find.</h3>
          <p>Stay updated when we discover something worth checking out.</p>
          <form class="email-form" id="emailForm" novalidate>
            <input type="email" id="emailInput" placeholder="Enter your email" aria-label="Email address">
            <button type="submit" id="notifyBtn">Notify Me</button>
          </form>
          <span class="email-note">Demo only — email collection is not connected yet.</span>
        </div>
      </div>
    </section>
  </main>

  <!-- ============ FOOTER ============ -->
  <footer class="site-footer" id="about">
    <div class="container">
      <div class="footer-brand">
        <div class="logo">DealForge<span>NG</span></div>
        <div class="footer-tagline">We find it. You decide.</div>
      </div>

      <div class="footer-links">
        <div class="footer-col">
          <h4>Explore</h4>
          <a href="#deals">Deals</a>
          <a href="#categories">Categories</a>
          <a href="#how-it-works">How It Works</a>
        </div>
        <div class="footer-col">
          <h4>Company</h4>
          <a href="#about">About</a>
          <a href="#transparency">Affiliate Disclosure</a>
          <a href="mailto:hello@dealforge.ng">Contact</a>
        </div>
        <div class="footer-col">
          <h4>Follow</h4>
          <a href="https://www.tiktok.com/@dealforge.ng" target="_blank" rel="noopener noreferrer">TikTok</a>
          <a href="https://www.instagram.com/dealforge.ng" target="_blank" rel="noopener noreferrer">Instagram</a>
          <a href="https://t.me/dealforgeng1" target="_blank" rel="noopener noreferrer">Telegram</a>
        </div>
      </div>

      <div class="footer-social">
        <a href="https://www.tiktok.com/@dealforge.ng" aria-label="TikTok" target="_blank" rel="noopener noreferrer">🎵</a>
        <a href="https://www.instagram.com/dealforge.ng" aria-label="Instagram" target="_blank" rel="noopener noreferrer">📸</a>
        <a href="https://t.me/dealforgeng1" aria-label="Telegram" target="_blank" rel="noopener noreferrer">✈️</a>
      </div>

      <div class="footer-disclaimer">
        <p>DealForge NG may earn a commission when you purchase through certain links. This does not necessarily affect the price you pay. DealForge does not sell or fulfil any products.</p>
        <p>Prices and availability may change. Always confirm the current information on the retailer's website before purchasing.</p>
      </div>
    </div>
  </footer>

  <!-- ============ MOBILE BOTTOM NAV ============ -->
  <nav class="mobile-bottom-nav" aria-label="Mobile bottom navigation">
    <a href="#" class="active" aria-label="Home"><span class="nav-icon" aria-hidden="true">🏠</span><span>Home</span></a>
    <a href="#deals" aria-label="Deals"><span class="nav-icon" aria-hidden="true">🔥</span><span>Deals</span></a>
    <a href="#categories" aria-label="Categories"><span class="nav-icon" aria-hidden="true">📂</span><span>Categories</span></a>
    <a href="#community" aria-label="Community"><span class="nav-icon" aria-hidden="true">💬</span><span>Community</span></a>
  </nav>

  <!-- ============ MODAL ============ -->
  <div class="modal-overlay" id="modalOverlay" role="dialog" aria-modal="true" aria-labelledby="modalTitle">
    <div class="modal-content" role="document">
      <button class="modal-close" id="modalClose" aria-label="Close product details">✕</button>
      <div id="modalBody"></div>
    </div>
  </div>

  <script>
    /* ============================================================
       PRODUCT DATA
       ============================================================ */
    const products = [
      {
        id: 'itel-powerbank',
        name: 'itel 20,000mAh Dual Output Fast Charging Power Bank',
        category: 'Tech & Gadgets',
        image: '',
        imageEmoji: '🔋',
        price: '₦15,720',
        previousPrice: '',
        discount: '',
        rating: '3.9',
        ratingCount: '16,000+',
        description: '20,000mAh capacity with dual output and fast charging. 12-month warranty.',
        features: [
          '20,000mAh capacity',
          'Dual output',
          'Fast charging',
          '12-month warranty'
        ],
        whyNoticed: 'High capacity power bank with strong verified ratings and a 12-month warranty — useful for daily commuting, travel or power outages.',
        considerations: 'Check the retailer listing for current price, availability and warranty details.',
        badge: '🔥 TRENDING',
        badgeClass: 'badge-trending',
        affiliateUrl: 'https://www.jumia.com.ng/itel-20000mah-dual-output-fast-charging-power-bank-98332547.html?utm_source=social&utm_medium=pdpshare'
      },
      {
        id: 'oipetluck-earbuds',
        name: 'OIPETLUCK Earhook Earbuds',
        category: 'Audio',
        image: '',
        imageEmoji: '🎧',
        price: 'Check price',
        previousPrice: '',
        discount: '',
        rating: '4.0',
        ratingCount: '168',
        description: 'Bluetooth earbuds with earhook design, designed for sports and running.',
        features: [
          'Bluetooth earbuds',
          'Earhook design',
          'Designed for sports/running'
        ],
        whyNoticed: 'The earhook design is useful for active use — running, workouts and gym sessions — with a solid 4.0 rating.',
        considerations: 'Check the retailer listing for current price and availability.',
        badge: '⭐ TOP PICK',
        badgeClass: 'badge-top',
        affiliateUrl: 'https://www.jumia.com.ng/oipetluck-earhook-earbuds-earphones-headset-for-runnersfitterssport-400103561.html?utm_source=social&utm_medium=pdpshare'
      },
      {
        id: 'bluetooth-selfie-tripod',
        name: 'Bluetooth Selfie Stick Tripod with Fill Light',
        category: 'Tech & Gadgets',
        image: '',
        imageEmoji: '📸',
        price: 'Check price',
        previousPrice: '',
        discount: '',
        rating: '',
        ratingCount: '',
        description: 'Selfie stick with tripod functionality, fill light and Bluetooth remote.',
        features: [
          'Selfie stick',
          'Tripod functionality',
          'Fill light',
          'Bluetooth remote'
        ],
        whyNoticed: 'Combines a selfie stick, tripod and fill light into one portable tool — handy for content creators, vloggers and casual photographers.',
        considerations: 'Check the retailer listing for current details and specifications.',
        badge: '💡 SMART FIND',
        badgeClass: 'badge-smart',
        affiliateUrl: 'https://www.jumia.com.ng/generic-bluetooth-selfie-stick-tripod-fill-light-shutter-remote-106334121.html?utm_source=social&utm_medium=pdpshare'
      }
    ];

    /* ============================================================
       STATE
       ============================================================ */
    let activeFilter = 'all';
    let searchQuery = '';

    /* ============================================================
       UTILITIES
       ============================================================ */
    function isPlaceholder(url) {
      if (!url) return true;
      const trimmed = String(url).trim();
      if (trimmed === '' || trimmed === '#') return true;
      if (trimmed.indexOf('PASTE_') === 0) return true;
      if (trimmed.indexOf('[') === 0) return true;
      return false;
    }

    function isSafeUrl(url) {
      if (!url) return false;
      const trimmed = String(url).trim().toLowerCase();
      return (
        trimmed.indexOf('http://') === 0 ||
        trimmed.indexOf('https://') === 0 ||
        trimmed.indexOf('mailto:') === 0
      );
    }

    function escapeHtml(str) {
      if (str == null) return '';
      return String(str)
        .replace(/&/g, '&amp;')
        .replace(/</g, '&lt;')
        .replace(/>/g, '&gt;')
        .replace(/"/g, '&quot;')
        .replace(/'/g, '&#39;');
    }

    /* ============================================================
       RENDER PRODUCTS
       ============================================================ */
    function renderProducts() {
      const grid = document.getElementById('productGrid');
      if (!grid) return;

      const q = searchQuery.toLowerCase().trim();

      const filtered = products.filter(function (p) {
        const matchesFilter = activeFilter === 'all' || p.category === activeFilter;
        if (!matchesFilter) return false;
        if (q === '') return true;

        const haystack = [
          p.name,
          p.category,
          p.description,
          p.whyNoticed,
          (p.features || []).join(' ')
        ].join(' ').toLowerCase();

        return haystack.indexOf(q) !== -1;
      });

      if (filtered.length === 0) {
        grid.innerHTML =
          '<div class="empty-state">' +
            '<strong>No products found</strong>' +
            '<span>Try a different search or filter.</span>' +
          '</div>';
        return;
      }

      grid.innerHTML = filtered.map(function (product) {
        const hasImage = product.image && !isPlaceholder(product.image);
        const imgHtml = hasImage
          ? '<img src="' + escapeHtml(product.image) + '" alt="' + escapeHtml(product.name) + '" loading="lazy" width="400" height="400">'
          : '<span class="card-image-placeholder" aria-hidden="true">' + (product.imageEmoji || '📦') + '</span>';

        const hasBadge = product.badge && String(product.badge).trim() !== '';
        const badgeHtml = hasBadge
          ? '<span class="card-badge ' + (product.badgeClass || '') + '">' + escapeHtml(product.badge) + '</span>'
          : '';

        const ratingHtml = product.rating
          ? '<div class="card-rating">' +
              '<span class="stars" aria-hidden="true">★</span>' +
              '<span>' + escapeHtml(product.rating) + '/5</span>' +
              (product.ratingCount ? '<span>· ' + escapeHtml(product.ratingCount) + ' ratings</span>' : '') +
            '</div>'
          : '';

        const priceHtml =
          '<div class="card-prices">' +
            '<span class="card-price-current">' + escapeHtml(product.price) + '</span>' +
            (product.previousPrice ? '<span class="card-price-previous">' + escapeHtml(product.previousPrice) + '</span>' : '') +
            (product.discount ? '<span class="card-discount">-' + escapeHtml(product.discount) + '</span>' : '') +
          '</div>';

        return (
          '<article class="product-card" data-id="' + escapeHtml(product.id) + '" tabindex="0" role="button" aria-label="View details for ' + escapeHtml(product.name) + '">' +
            '<div class="card-image-wrap">' +
              badgeHtml +
              imgHtml +
            '</div>' +
            '<div class="card-body">' +
              '<span class="card-category">' + escapeHtml(product.category) + '</span>' +
              '<h3 class="card-title">' + escapeHtml(product.name) + '</h3>' +
              ratingHtml +
              priceHtml +
              '<p class="card-desc">' + escapeHtml(product.description) + '</p>' +
              '<button class="card-cta" data-id="' + escapeHtml(product.id) + '" aria-label="Check deal for ' + escapeHtml(product.name) + '">Check Deal →</button>' +
            '</div>' +
          '</article>'
        );
      }).join('');

      grid.querySelectorAll('.product-card').forEach(function (card) {
        card.addEventListener('click', function (e) {
          if (e.target.closest('.card-cta')) return;
          openProductModal(card.dataset.id);
        });
        card.addEventListener('keydown', function (e) {
          if (e.key === 'Enter' || e.key === ' ') {
            e.preventDefault();
            openProductModal(card.dataset.id);
          }
        });
      });

      grid.querySelectorAll('.card-cta').forEach(function (btn) {
        btn.addEventListener('click', function (e) {
          e.stopPropagation();
          const product = products.find(function (p) { return p.id === btn.dataset.id; });
          if (product && !isPlaceholder(product.affiliateUrl) && isSafeUrl(product.affiliateUrl)) {
            window.open(product.affiliateUrl, '_blank', 'noopener,noreferrer');
          } else {
            openProductModal(btn.dataset.id);
          }
        });
      });
    }

    /* ============================================================
       PRODUCT MODAL
       ============================================================ */
    function openProductModal(id) {
      const product = products.find(function (p) { return p.id === id; });
      if (!product) return;

      const modalBody = document.getElementById('modalBody');
      const hasImage = product.image && !isPlaceholder(product.image);
      const placeholder = isPlaceholder(product.affiliateUrl) || !isSafeUrl(product.affiliateUrl);

      const imgHtml = hasImage
        ? '<img src="' + escapeHtml(product.image) + '" alt="' + escapeHtml(product.name) + '" loading="lazy">'
        : '<span aria-hidden="true">' + (product.imageEmoji || '📦') + '</span>';

      const ratingHtml = product.rating
        ? '<div class="modal-rating">' +
            '<span class="stars" aria-hidden="true">★</span>' +
            '<span>' + escapeHtml(product.rating) + '/5</span>' +
            (product.ratingCount ? '<span>· ' + escapeHtml(product.ratingCount) + ' ratings</span>' : '') +
          '</div>'
        : '';

      const pricesHtml =
        '<div class="modal-prices">' +
          '<span class="modal-price-current">' + escapeHtml(product.price) + '</span>' +
          (product.previousPrice ? '<span class="modal-price-previous">' + escapeHtml(product.previousPrice) + '</span>' : '') +
          (product.discount ? '<span class="modal-discount">-' + escapeHtml(product.discount) + '</span>' : '') +
        '</div>';

      const featuresHtml = (product.features && product.features.length)
        ? '<div class="modal-section">' +
            '<h4>Key Specifications</h4>' +
            '<ul>' + product.features.map(function (f) { return '<li>' + escapeHtml(f) + '</li>'; }).join('') + '</ul>' +
          '</div>'
        : '';

      const whyHtml = product.whyNoticed
        ? '<div class="modal-section">' +
            '<h4>Why we noticed it</h4>' +
            '<p>' + escapeHtml(product.whyNoticed) + '</p>' +
          '</div>'
        : '';

      const considerHtml = product.considerations
        ? '<div class="modal-section">' +
            '<h4>Things to consider</h4>' +
            '<p>' + escapeHtml(product.considerations) + '</p>' +
          '</div>'
        : '';

      const ctaHref = placeholder ? '#' : product.affiliateUrl;
      const ctaTarget = placeholder ? '' : 'target="_blank" rel="noopener noreferrer"';

      modalBody.innerHTML =
        '<div class="modal-image">' + imgHtml + '</div>' +
        '<div class="modal-category">' + escapeHtml(product.category) + '</div>' +
        '<h2 class="modal-title" id="modalTitle">' + escapeHtml(product.name) + '</h2>' +
        ratingHtml +
        pricesHtml +
        '<div class="modal-section">' +
          '<h4>Description</h4>' +
          '<p>' + escapeHtml(product.description) + '</p>' +
        '</div>' +
        featuresHtml +
        whyHtml +
        considerHtml +
        '<a href="' + escapeHtml(ctaHref) + '" class="modal-cta" id="modalCta" ' + ctaTarget + '>View Deal →</a>' +
        '<p class="modal-disclaimer">' +
          'Prices, availability and product information can change. Check the retailer\'s page for the latest details. ' +
          'DealForge NG does not sell or fulfil this product. DealForge may earn a commission from qualifying purchases at no extra cost to you.' +
        '</p>';

      const modalCta = document.getElementById('modalCta');
      if (modalCta && placeholder) {
        modalCta.addEventListener('click', function (e) {
          e.preventDefault();
          alert('Retailer link coming soon.');
        });
      }

      document.getElementById('modalOverlay').classList.add('open');
      document.body.style.overflow = 'hidden';
    }

    function closeModal() {
      document.getElementById('modalOverlay').classList.remove('open');
      document.body.style.overflow = '';
    }

    /* ============================================================
       SEARCH, FILTERS, CATEGORIES
       ============================================================ */
    function initSearch() {
      const input = document.getElementById('searchInput');
      if (!input) return;
      let debounce;
      input.addEventListener('input', function (e) {
        clearTimeout(debounce);
        const val = e.target.value;
        debounce = setTimeout(function () {
          searchQuery = val.trim();
          renderProducts();
        }, 180);
      });
    }

    function setActiveFilter(filterValue) {
      activeFilter = filterValue;
      document.querySelectorAll('.filter-chip').forEach(function (chip) {
        chip.classList.toggle('active', chip.dataset.filter === filterValue);
      });
      renderProducts();
    }

    function initFilters() {
      document.querySelectorAll('.filter-chip').forEach(function (chip) {
        chip.addEventListener('click', function () {
          setActiveFilter(chip.dataset.filter);
        });
      });
    }

    function initCategoryCards() {
      document.querySelectorAll('.category-card').forEach(function (card) {
        card.addEventListener('click', function () {
          const cat = card.dataset.category;
          const chip = document.querySelector('.filter-chip[data-filter="' + cat + '"]');
          if (chip) {
            setActiveFilter(cat);
            const deals = document.getElementById('deals');
            if (deals) deals.scrollIntoView({ behavior: 'smooth', block: 'start' });
          }
        });
      });
    }

    /* ============================================================
       MOBILE MENU
       ============================================================ */
    function initMobileMenu() {
      const btn = document.getElementById('mobileMenuBtn');
      const nav = document.getElementById('mobileNav');
      if (!btn || !nav) return;

      btn.addEventListener('click', function () {
        const isOpen = nav.classList.toggle('open');
        btn.classList.toggle('active');
        btn.setAttribute('aria-expanded', isOpen ? 'true' : 'false');
      });

      nav.querySelectorAll('a').forEach(function (link) {
        link.addEventListener('click', function () {
          nav.classList.remove('open');
          btn.classList.remove('active');
          btn.setAttribute('aria-expanded', 'false');
        });
      });
    }

    /* ============================================================
       HEADER SHADOW
       ============================================================ */
    function initHeaderScroll() {
      const header = document.getElementById('siteHeader');
      if (!header) return;
      const onScroll = function () {
        header.classList.toggle('scrolled', window.scrollY > 10);
      };
      window.addEventListener('scroll', onScroll, { passive: true });
      onScroll();
    }

    /* ============================================================
       MODAL EVENTS
       ============================================================ */
    function initModal() {
      const overlay = document.getElementById('modalOverlay');
      const closeBtn = document.getElementById('modalClose');
      if (!overlay || !closeBtn) return;

      closeBtn.addEventListener('click', closeModal);
      overlay.addEventListener('click', function (e) {
        if (e.target === overlay) closeModal();
      });
      document.addEventListener('keydown', function (e) {
        if (e.key === 'Escape' && overlay.classList.contains('open')) closeModal();
      });
    }

    /* ============================================================
       EMAIL FORM (visual demo only)
       ============================================================ */
    function initEmailForm() {
      const form = document.getElementById('emailForm');
      const btn = document.getElementById('notifyBtn');
      const input = document.getElementById('emailInput');
      if (!form || !btn || !input) return;

      form.addEventListener('submit', function (e) {
        e.preventDefault();
        if (!input.value.trim()) {
          input.focus();
          return;
        }
        const original = btn.textContent;
        btn.textContent = '✓ Noted!';
        btn.style.background = '#10B981';
        btn.disabled = true;
        setTimeout(function () {
          btn.textContent = original;
          btn.style.background = '';
          btn.disabled = false;
          input.value = '';
        }, 2000);
      });
    }

    /* ============================================================
       MOBILE BOTTOM NAV
       ============================================================ */
    function initMobileBottomNav() {
      const links = document.querySelectorAll('.mobile-bottom-nav a');
      if (!links.length) return;
      links.forEach(function (link) {
        link.addEventListener('click', function () {
          links.forEach(function (l) { l.classList.remove('active'); });
          link.classList.add('active');
        });
      });
    }

    /* ============================================================
       DEALFORGE AGENT V1
       ============================================================ */

    /* Safe localStorage access — works even in private mode */
    function safeGetApproved() {
      try {
        const raw = localStorage.getItem('dealforgeApprovedFinds');
        if (!raw) return [];
        const parsed = JSON.parse(raw);
        return Array.isArray(parsed) ? parsed : [];
      } catch (err) {
        return [];
      }
    }

    function safeSetApproved(list) {
      try {
        localStorage.setItem('dealforgeApprovedFinds', JSON.stringify(list));
        return true;
      } catch (err) {
        return false;
      }
    }

    const agentState = {
      currentFind: null,
      approvedFinds: safeGetApproved()
    };

    function calculateDealScore(data) {
      let score = 50;

      /* Budget */
      if (data.budget && data.price) {
        if (data.price <= data.budget) {
          score += 15;
        } else if (data.price <= data.budget * 1.1) {
          score += 7;
        } else {
          score -= 10;
        }
      }

      /* Rating */
      if (data.rating >= 4.5) {
        score += 15;
      } else if (data.rating >= 4) {
        score += 10;
      } else if (data.rating >= 3.5) {
        score += 5;
      } else if (data.rating > 0 && data.rating < 3) {
        score -= 10;
      }

      /* Product/content potential */
      const product = String(data.product || '').toLowerCase();

      const highInterestWords = [
        'earbuds',
        'headphones',
        'power bank',
        'charger',
        'tripod',
        'phone',
        'keyboard',
        'mouse',
        'speaker',
        'watch',
        'projector',
        'gaming',
        'led',
        'smart'
      ];

      highInterestWords.forEach(function (word) {
        if (product.indexOf(word) !== -1) {
          score += 3;
        }
      });

      return Math.max(0, Math.min(100, Math.round(score)));
    }

    function getVerdict(score) {
      if (score >= 85) {
        return '<strong>🔥 Strong find.</strong> This has several signals that make it worth investigating further before publishing.';
      }
      if (score >= 70) {
        return '<strong>💡 Promising find.</strong> There is enough potential here for DealForge to consider creating content around it.';
      }
      if (score >= 55) {
        return '<strong>👀 Worth checking.</strong> The product has some potential, but more verification is recommended.';
      }
      return '<strong>⚠️ Weak opportunity.</strong> The available information does not currently provide a strong enough reason to highlight it.';
    }

    function generateTikTok(product, category, score) {
      const hooks = [
        'Would you actually buy this?',
        'I found something you might want to see.',
        'This might be one of those surprisingly useful finds.',
        'Before you spend money on this, check this out.',
        'This product caught my attention for one reason.',
        'Is this actually worth the money?'
      ];

      const hook = hooks[Math.floor(Math.random() * hooks.length)];

      return (
        hook +
        '\n\n' +
        'Product: ' + product +
        '\n' +
        'Category: ' + category +
        '\n\n' +
        'DealForge score: ' + score + '/100.' +
        '\n\n' +
        'We found it. We checked the available information. ' +
        'Now you decide if it is worth checking out.' +
        '\n\n' +
        '#DealForgeNG #DealsNigeria #TechFinds #SmartFinds'
      );
    }

    function generateWhatsApp(product, category, score) {
      return (
        '🔥 DEALFORGE FIND\n\n' +
        product +
        '\n\n' +
        'Category: ' + category +
        '\n' +
        'DealForge score: ' + score + '/100\n\n' +
        'Why we noticed it:\n' +
        'A potentially interesting ' + category.toLowerCase() +
        ' find worth checking out.\n\n' +
        '💡 We find it. You decide.\n\n' +
        'Always confirm the current price, availability and product details before buying.'
      );
    }

    function runDealForgeAgent() {
      const productInput = document.getElementById('agentProduct');
      const budgetInput = document.getElementById('agentBudget');
      const ratingInput = document.getElementById('agentRating');
      const categoryInput = document.getElementById('agentCategory');
      const affiliateInput = document.getElementById('agentAffiliate');

      const status = document.getElementById('agentStatus');
      const button = document.getElementById('runAgentBtn');

      const product = productInput.value.trim();
      const budget = Number(budgetInput.value) || 0;
      const minimumRating = Number(ratingInput.value) || 0;
      const category = categoryInput.value;
      const affiliateUrl = affiliateInput.value.trim();

      if (!product) {
        productInput.focus();
        status.textContent = 'Enter a product first.';
        return;
      }

      button.disabled = true;
      button.textContent = '⏳ Analyzing...';
      status.textContent = 'DealForge Agent is analyzing the find...';

      setTimeout(function () {
        /* Try to find a matching existing product */
        const lowerProduct = product.toLowerCase();
        const matchingProduct = products.find(function (p) {
          const name = p.name.toLowerCase();
          return name.indexOf(lowerProduct) !== -1 || lowerProduct.indexOf(name) !== -1;
        });

        let price = 0;
        let rating = minimumRating;

        if (matchingProduct) {
          /* Extract numeric price if available */
          const numericPrice = String(matchingProduct.price).replace(/[^\d.]/g, '');
          const parsed = Number(numericPrice);
          if (!isNaN(parsed) && parsed > 0) {
            price = parsed;
          }
          /* Use matching product rating if higher than min */
          if (matchingProduct.rating) {
            const r = Number(matchingProduct.rating);
            if (!isNaN(r) && r > rating) {
              rating = r;
            }
          }
        }

        const score = calculateDealScore({
          product: product,
          budget: budget,
          price: price,
          rating: rating
        });

        const verdict = getVerdict(score);
        const tiktok = generateTikTok(product, category, score);
        const whatsapp = generateWhatsApp(product, category, score);

        /* Save current find */
        agentState.currentFind = {
          id: 'agent-' + Date.now(),
          product: product,
          category: category,
          budget: budget,
          price: price,
          rating: rating,
          score: score,
          affiliateUrl: affiliateUrl,
          tiktok: tiktok,
          whatsapp: whatsapp,
          createdAt: new Date().toISOString()
        };

        /* Update UI */
        document.getElementById('agentResultName').textContent = product;
        document.getElementById('agentScore').textContent = score;
        document.getElementById('agentVerdict').innerHTML = verdict;

        document.getElementById('metricUsefulness').textContent =
          score >= 75 ? 'High' :
          score >= 55 ? 'Medium' : 'Low';

        /* Value metric — properly reflects when we DO know price */
        let valueLabel;
        if (price > 0 && budget > 0) {
          if (price <= budget) {
            valueLabel = 'Within budget';
          } else if (price <= budget * 1.1) {
            valueLabel = 'Slightly over';
          } else {
            valueLabel = 'Over budget';
          }
        } else if (price > 0) {
          valueLabel = 'No budget set';
        } else {
          valueLabel = 'Needs price check';
        }
        document.getElementById('metricValue').textContent = valueLabel;

        document.getElementById('metricContent').textContent =
          score >= 70 ? 'High' :
          score >= 55 ? 'Medium' : 'Low';

        document.getElementById('metricRisk').textContent =
          score >= 75 ? 'Low–Med' :
          score >= 55 ? 'Medium' : 'Higher';

        document.getElementById('agentTikTok').textContent = tiktok;
        document.getElementById('agentWhatsApp').textContent = whatsapp;

        document.getElementById('agentResults').classList.add('visible');
        document.getElementById('agentEmptyState').style.display = 'none';
        document.getElementById('agentApproved').classList.remove('show');

        button.disabled = false;
        button.textContent = '⚡ Analyze Again';
        status.textContent = 'Analysis complete. Review the result before publishing.';
      }, 700);
    }

    function copyAgentText(elementId, buttonId) {
      const element = document.getElementById(elementId);
      const button = document.getElementById(buttonId);
      if (!element || !button) return;

      const text = element.textContent;

      /* Preferred: clipboard API */
      if (navigator.clipboard && navigator.clipboard.writeText) {
        navigator.clipboard.writeText(text).then(function () {
          const original = button.textContent;
          button.textContent = '✓ Copied!';
          setTimeout(function () { button.textContent = original; }, 1500);
        }).catch(function () {
          fallbackCopy(text, button);
        });
        return;
      }

      fallbackCopy(text, button);
    }

    /* Fallback for old browsers / insecure contexts */
    function fallbackCopy(text, button) {
      try {
        const ta = document.createElement('textarea');
        ta.value = text;
        ta.setAttribute('readonly', '');
        ta.style.position = 'absolute';
        ta.style.left = '-9999px';
        document.body.appendChild(ta);
        ta.select();
        document.execCommand('copy');
        document.body.removeChild(ta);

        const original = button.textContent;
        button.textContent = '✓ Copied!';
        setTimeout(function () { button.textContent = original; }, 1500);
      } catch (err) {
        alert('Copy failed. Please select the text manually.');
      }
    }

    function approveAgentFind() {
      if (!agentState.currentFind) {
        document.getElementById('agentStatus').textContent =
          'Run an analysis first.';
        return;
      }

      const existingIndex = agentState.approvedFinds.findIndex(function (item) {
        return item.id === agentState.currentFind.id;
      });

      if (existingIndex === -1) {
        agentState.approvedFinds.push(agentState.currentFind);
      }

      const ok = safeSetApproved(agentState.approvedFinds);

      const approvedEl = document.getElementById('agentApproved');
      approvedEl.classList.add('show');

      if (ok) {
        document.getElementById('agentStatus').textContent =
          'Find approved and saved locally.';
      } else {
        approvedEl.textContent = '✓ Find approved (session only — storage unavailable).';
        document.getElementById('agentStatus').textContent =
          'Saved in this session only (browser storage unavailable).';
      }
    }

    function initDealForgeAgent() {
      const runButton = document.getElementById('runAgentBtn');
      if (!runButton) return;

      runButton.addEventListener('click', runDealForgeAgent);

      const copyTikTokBtn = document.getElementById('copyTikTok');
      if (copyTikTokBtn) {
        copyTikTokBtn.addEventListener('click', function () {
          copyAgentText('agentTikTok', 'copyTikTok');
        });
      }

      const copyWhatsAppBtn = document.getElementById('copyWhatsApp');
      if (copyWhatsAppBtn) {
        copyWhatsAppBtn.addEventListener('click', function () {
          copyAgentText('agentWhatsApp', 'copyWhatsApp');
        });
      }

      const approveBtn = document.getElementById('approveDeal');
      if (approveBtn) {
        approveBtn.addEventListener('click', approveAgentFind);
      }

      const productInput = document.getElementById('agentProduct');
      if (productInput) {
        productInput.addEventListener('keydown', function (e) {
          if (e.key === 'Enter') {
            e.preventDefault();
            runDealForgeAgent();
          }
        });
      }
    }

    /* ============================================================
       INIT
       ============================================================ */
    document.addEventListener('DOMContentLoaded', function () {
      renderProducts();
      initSearch();
      initFilters();
      initCategoryCards();
      initMobileMenu();
      initHeaderScroll();
      initModal();
      initEmailForm();
      initMobileBottomNav();
      initDealForgeAgent();
    });
  </script>
</body>
</html>