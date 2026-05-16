<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>MTS Design – Graphic Design Studio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;1,400;1,500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --primary: #48426D;
      --primary-dark: #2e2a47;
      --primary-light: #6b6496;
      --primary-pale: #f0edf8;
      --secondary: #f1c28e;
      --secondary-dark: #c07a30;
      --slogan: #f3ab9d;
      --white: #ffffff;
      --off-white: #faf9fd;
      --gray-light: #f4f3f8;
      --gray-mid: #b0adc4;
      --gray-text: #6b6884;
      --border: rgba(72, 66, 109, 0.15);
      --font-display: 'Cormorant Garamond', Georgia, serif;
      --font-body: 'DM Sans', sans-serif;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: var(--font-body);
      color: var(--primary-dark);
      background: var(--white);
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }

    /* ── NAV ── */
    nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 1.25rem 2.5rem;
      background: var(--primary);
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .nav-logo {
      font-family: var(--font-display);
      font-size: 22px;
      font-weight: 500;
      letter-spacing: 4px;
      color: var(--white);
      text-decoration: none;
    }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      font-size: 13px;
      font-weight: 400;
      color: rgba(255,255,255,0.65);
      text-decoration: none;
      letter-spacing: 0.5px;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--white); }

    /* ── HERO ── */
    .hero {
      background: var(--primary);
      padding: 6rem 2.5rem 5rem;
      text-align: center;
    }
    .hero-eyebrow {
      font-size: 11px;
      letter-spacing: 4px;
      text-transform: uppercase;
      color: rgba(255,255,255,0.5);
      margin-bottom: 2rem;
    }
    .hero h1 {
      font-family: var(--font-display);
      font-size: clamp(42px, 6vw, 68px);
      font-weight: 400;
      line-height: 1.05;
      color: var(--white);
      letter-spacing: -1px;
      margin-bottom: 1rem;
    }
    .hero h1 em {
      font-style: italic;
      color: var(--secondary);
    }
    .hero-slogan {
      font-family: var(--font-display);
      font-size: 20px;
      font-style: italic;
      color: var(--slogan);
      margin-bottom: 1.25rem;
      font-weight: 400;
    }
    .hero-sub {
      font-size: 15px;
      color: rgba(255,255,255,0.6);
      max-width: 480px;
      margin: 0 auto 2.5rem;
      line-height: 1.8;
    }
    .hero-ctas { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; }
    .btn-primary {
      display: inline-block;
      padding: 12px 28px;
      background: var(--secondary);
      color: var(--primary-dark);
      font-family: var(--font-body);
      font-size: 14px;
      font-weight: 500;
      text-decoration: none;
      border-radius: 6px;
      border: none;
      cursor: pointer;
      transition: opacity 0.2s, transform 0.15s;
    }
    .btn-primary:hover { opacity: 0.9; transform: translateY(-1px); }
    .btn-ghost {
      display: inline-block;
      padding: 12px 28px;
      background: transparent;
      color: var(--white);
      font-family: var(--font-body);
      font-size: 14px;
      font-weight: 400;
      text-decoration: none;
      border-radius: 6px;
      border: 1px solid rgba(255,255,255,0.3);
      cursor: pointer;
      transition: background 0.2s;
    }
    .btn-ghost:hover { background: rgba(255,255,255,0.08); }

    /* ── STATS ── */
    .stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      background: var(--primary-dark);
    }
    .stat {
      padding: 2rem;
      text-align: center;
      border-right: 1px solid rgba(255,255,255,0.08);
    }
    .stat:last-child { border-right: none; }
    .stat-num {
      font-family: var(--font-display);
      font-size: 40px;
      font-weight: 500;
      color: var(--secondary);
      line-height: 1;
    }
    .stat-label {
      font-size: 12px;
      color: rgba(255,255,255,0.45);
      margin-top: 6px;
      letter-spacing: 0.5px;
    }

    /* ── SECTIONS ── */
    section { padding: 5rem 2.5rem; border-bottom: 1px solid var(--border); }
    section:last-of-type { border-bottom: none; }

    .section-label {
      font-size: 10px;
      letter-spacing: 4px;
      text-transform: uppercase;
      color: var(--primary-light);
      font-weight: 500;
      margin-bottom: 2.5rem;
    }

    /* ── ABOUT ── */
    .about { background: var(--white); }
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 4rem;
      align-items: center;
      max-width: 1100px;
      margin: 0 auto;
    }
    .about-grid h2 {
      font-family: var(--font-display);
      font-size: 40px;
      font-weight: 400;
      line-height: 1.2;
      color: var(--primary);
      margin-bottom: 1.25rem;
    }
    .about-grid p {
      font-size: 15px;
      color: var(--gray-text);
      line-height: 1.85;
    }
    .about-grid p + p { margin-top: 1rem; }

    .founder-card {
      background: var(--primary);
      border-radius: 16px;
      padding: 2rem;
      display: flex;
      flex-direction: column;
      gap: 1.25rem;
    }
    .founder-top { display: flex; align-items: center; gap: 16px; }
    .founder-avatar {
      width: 56px;
      height: 56px;
      border-radius: 50%;
      background: var(--secondary);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: var(--font-display);
      font-size: 22px;
      font-weight: 500;
      color: var(--primary-dark);
      flex-shrink: 0;
    }
    .founder-name {
      font-family: var(--font-display);
      font-size: 20px;
      font-weight: 500;
      color: var(--white);
    }
    .founder-role { font-size: 13px; color: var(--slogan); margin-top: 3px; }
    .founder-bio {
      font-size: 14px;
      color: rgba(255,255,255,0.6);
      line-height: 1.75;
      border-top: 1px solid rgba(255,255,255,0.12);
      padding-top: 1.25rem;
    }
    .founder-links { display: flex; gap: 8px; flex-wrap: wrap; }
    .founder-link {
      display: inline-flex;
      align-items: center;
      gap: 5px;
      font-size: 12px;
      color: rgba(255,255,255,0.75);
      text-decoration: none;
      padding: 5px 12px;
      border: 1px solid rgba(255,255,255,0.2);
      border-radius: 6px;
      transition: background 0.2s;
    }
    .founder-link:hover { background: rgba(255,255,255,0.1); }

    /* ── PORTFOLIO ── */
    .portfolio { background: var(--gray-light); }
    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1.25rem;
      max-width: 1100px;
      margin: 0 auto;
    }
    .project {
      background: var(--white);
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid var(--border);
      transition: transform 0.2s, box-shadow 0.2s;
    }
    .project:hover { transform: translateY(-3px); box-shadow: 0 12px 32px rgba(72,66,109,0.12); }
    .project-thumb {
      height: 180px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-bottom: 1px solid var(--border);
    }
    .project-thumb i { font-size: 36px; }
    .t1 { background: #f0edf8; } .t1 i { color: var(--primary); }
    .t2 { background: #fdf3e5; } .t2 i { color: var(--secondary-dark); }
    .t3 { background: #fde8e4; } .t3 i { color: #c45c4e; }
    .t4 { background: #e8e6f2; } .t4 i { color: var(--primary-light); }
    .project-info { padding: 1.25rem 1.5rem; }
    .project-tag {
      font-size: 10px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: var(--primary-light);
      font-weight: 500;
      margin-bottom: 6px;
    }
    .project-title { font-size: 16px; font-weight: 500; color: var(--primary-dark); }
    .project-desc { font-size: 13px; color: var(--gray-text); margin-top: 6px; line-height: 1.65; }

    /* ── SERVICES ── */
    .services { background: var(--white); }
    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.25rem;
      max-width: 1100px;
      margin: 0 auto;
    }
    .service-card {
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 1.75rem;
      background: var(--white);
    }
    .service-card.featured {
      border: 2px solid var(--primary);
      background: var(--primary-pale);
    }
    .service-icon { font-size: 24px; color: var(--primary); margin-bottom: 1rem; display: block; }
    .service-badge {
      display: inline-block;
      font-size: 10px;
      padding: 3px 10px;
      border-radius: 20px;
      background: var(--secondary);
      color: var(--primary-dark);
      font-weight: 500;
      letter-spacing: 0.5px;
      margin-bottom: 0.5rem;
    }
    .service-name { font-size: 16px; font-weight: 500; color: var(--primary); margin-bottom: 4px; }
    .service-price {
      font-family: var(--font-display);
      font-size: 28px;
      font-weight: 500;
      color: var(--primary);
      margin: 0.75rem 0 0.5rem;
      letter-spacing: -0.5px;
    }
    .service-price span { font-size: 14px; font-weight: 400; color: var(--gray-text); font-family: var(--font-body); }
    .service-desc { font-size: 13px; color: var(--gray-text); line-height: 1.65; margin-bottom: 1rem; }
    .service-list { list-style: none; }
    .service-list li {
      font-size: 13px;
      color: var(--gray-text);
      padding: 5px 0;
      border-bottom: 1px solid var(--border);
      display: flex;
      align-items: center;
      gap: 7px;
    }
    .service-list li:last-child { border-bottom: none; }
    .service-list i { font-size: 14px; color: var(--primary); flex-shrink: 0; }

    /* ── REVIEWS ── */
    .reviews { background: var(--gray-light); }
    .reviews-inner { max-width: 1100px; margin: 0 auto; }
    .rating-summary {
      display: flex;
      align-items: center;
      gap: 2rem;
      padding: 1.75rem 2rem;
      background: var(--primary);
      border-radius: 12px;
      margin-bottom: 1.5rem;
    }
    .rating-big {
      font-family: var(--font-display);
      font-size: 56px;
      font-weight: 500;
      color: var(--secondary);
      line-height: 1;
    }
    .rating-stars-static { display: flex; gap: 4px; }
    .rating-stars-static span { font-size: 22px; color: var(--secondary); }
    .rating-count { font-size: 13px; color: rgba(255,255,255,0.5); margin-top: 5px; }
    .reviews-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1.25rem;
    }
    .review-card {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 1.5rem;
    }
    .review-stars { display: flex; gap: 3px; margin-bottom: 1rem; }
    .review-stars span { font-size: 16px; color: var(--secondary-dark); }
    .review-text {
      font-family: var(--font-display);
      font-size: 15px;
      font-style: italic;
      color: var(--primary-dark);
      line-height: 1.7;
      margin-bottom: 1rem;
    }
    .review-author { display: flex; align-items: center; gap: 10px; }
    .review-avatar {
      width: 32px;
      height: 32px;
      border-radius: 50%;
      background: var(--primary);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 11px;
      font-weight: 500;
      color: var(--white);
      flex-shrink: 0;
    }
    .review-name { font-size: 13px; font-weight: 500; color: var(--primary-dark); }
    .review-date { font-size: 11px; color: var(--gray-mid); }

    /* Leave a rating card */
    .leave-review-card {
      background: var(--white);
      border: 1.5px dashed var(--primary-light);
      border-radius: 12px;
      padding: 1.5rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      gap: 0.75rem;
    }
    .leave-review-card p { font-size: 14px; font-weight: 500; color: var(--primary); }
    .leave-stars { display: flex; gap: 6px; }
    .leave-star {
      font-size: 30px;
      cursor: pointer;
      color: #d5d2e5;
      transition: color 0.1s, transform 0.1s;
      line-height: 1;
      user-select: none;
    }
    .leave-star.hover, .leave-star.selected { color: var(--secondary); transform: scale(1.15); }
    .leave-feedback { font-size: 12px; color: var(--gray-text); min-height: 18px; }

    /* ── CONTACT ── */
    .contact { background: var(--white); }
    .contact-inner {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 4rem;
      align-items: start;
      max-width: 1100px;
      margin: 0 auto;
    }
    .contact-inner h2 {
      font-family: var(--font-display);
      font-size: 38px;
      font-weight: 400;
      line-height: 1.2;
      color: var(--primary);
      margin-bottom: 0.75rem;
    }
    .contact-inner > div > p {
      font-size: 15px;
      color: var(--gray-text);
      line-height: 1.8;
      margin-bottom: 1.75rem;
    }
    .contact-channels { display: flex; flex-direction: column; gap: 0.75rem; }
    .channel {
      display: flex;
      align-items: center;
      gap: 14px;
      padding: 1rem 1.25rem;
      border: 1px solid var(--border);
      border-radius: 10px;
      text-decoration: none;
      color: var(--primary-dark);
      transition: border-color 0.2s, background 0.2s;
    }
    .channel:hover { border-color: var(--primary); background: var(--primary-pale); }
    .channel i { font-size: 20px; color: var(--primary); flex-shrink: 0; }
    .channel-info p { font-size: 14px; font-weight: 500; }
    .channel-info span { font-size: 12px; color: var(--gray-text); }
    .contact-form { display: flex; flex-direction: column; gap: 1rem; }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    .form-field { display: flex; flex-direction: column; gap: 5px; }
    .form-label { font-size: 12px; font-weight: 500; color: var(--primary); letter-spacing: 0.3px; }
    input, select, textarea {
      font-family: var(--font-body);
      font-size: 14px;
      padding: 10px 14px;
      border: 1px solid var(--border);
      border-radius: 8px;
      background: var(--white);
      color: var(--primary-dark);
      outline: none;
      transition: border-color 0.2s;
      width: 100%;
    }
    input:focus, select:focus, textarea:focus { border-color: var(--primary); }
    textarea { min-height: 110px; resize: none; }

    /* ── FOOTER ── */
    footer {
      padding: 1.75rem 2.5rem;
      background: var(--primary-dark);
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 1rem;
    }
    footer p { font-size: 13px; color: rgba(255,255,255,0.4); }
    .footer-links { display: flex; gap: 1.5rem; }
    .footer-links a { font-size: 13px; color: rgba(255,255,255,0.5); text-decoration: none; transition: color 0.2s; }
    .footer-links a:hover { color: var(--white); }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      nav { padding: 1rem 1.25rem; }
      .nav-links { display: none; }
      .hero { padding: 4rem 1.25rem 3rem; }
      .hero h1 { font-size: 38px; }
      .stats { grid-template-columns: repeat(3,1fr); }
      .stat { padding: 1.25rem 0.5rem; }
      .stat-num { font-size: 28px; }
      section { padding: 3rem 1.25rem; }
      .about-grid, .contact-inner { grid-template-columns: 1fr; gap: 2rem; }
      .portfolio-grid, .reviews-grid { grid-template-columns: 1fr; }
      .services-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <a class="nav-logo" href="#">MTS</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#portfolio">Portfolio</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#reviews">Reviews</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero">
    <p class="hero-eyebrow">Graphic Design Studio &middot; Addis Ababa</p>
    <h1>Design that makes<br>brands <em>unforgettable</em></h1>
    <p class="hero-slogan">"Where creativity meets identity"</p>
    <p class="hero-sub">MTS Design crafts visual identities, brand systems, and digital experiences that leave a lasting impression.</p>
    <div class="hero-ctas">
      <a class="btn-primary" href="#portfolio">View our work</a>
      <a class="btn-ghost" href="mailto:mts.maren18@gmail.com">Get a quote</a>
    </div>
  </section>

  <!-- STATS -->
  <div class="stats">
    <div class="stat"><div class="stat-num">1</div><div class="stat-label">Creative founder</div></div>
    <div class="stat"><div class="stat-num">50+</div><div class="stat-label">Projects delivered</div></div>
    <div class="stat"><div class="stat-num">5.0</div><div class="stat-label">Average rating</div></div>
  </div>

  <!-- ABOUT -->
  <section class="about" id="about">
    <p class="section-label">About</p>
    <div class="about-grid">
      <div>
        <h2>One founder.<br>One clear vision.</h2>
        <p>MTS Design was built on a belief that great design transforms how people see a brand. Combining strategic thinking with refined aesthetics, MTS creates work that resonates — and endures.</p>
        <p>Working closely with startups, small businesses, and individuals who care deeply about how they present themselves to the world.</p>
      </div>
      <div class="founder-card">
        <div class="founder-top">
          <div class="founder-avatar">M</div>
          <div>
            <div class="founder-name">Mickyas T.</div>
            <div class="founder-role">Founder &amp; Creative Director</div>
          </div>
        </div>
        <div class="founder-bio">Graphic designer based in Addis Ababa, specializing in brand identity, logo design, posters, and digital graphics. Passionate about creating meaningful visuals that help brands stand out.</div>
        <div class="founder-links">
          <a class="founder-link" href="https://t.me/Mickyas_T" target="_blank"><i class="ti ti-brand-telegram"></i> Telegram</a>
          <a class="founder-link" href="mailto:mts.maren18@gmail.com"><i class="ti ti-mail"></i> Email</a>
          <a class="founder-link" href="https://wa.me/251940786019" target="_blank"><i class="ti ti-brand-whatsapp"></i> WhatsApp</a>
        </div>
      </div>
    </div>
  </section>

  <!-- PORTFOLIO -->
  <section class="portfolio" id="portfolio">
    <p class="section-label">Portfolio</p>
    <div class="portfolio-grid">
      <div class="project">
        <div class="project-thumb t1"><i class="ti ti-building-store"></i></div>
        <div class="project-info">
          <p class="project-tag">Brand identity</p>
          <p class="project-title">Habesha Coffee Co.</p>
          <p class="project-desc">Full brand identity system including logo, color palette, packaging, and signage for an Addis-based specialty coffee brand.</p>
        </div>
      </div>
      <div class="project">
        <div class="project-thumb t2"><i class="ti ti-device-mobile"></i></div>
        <div class="project-info">
          <p class="project-tag">Social media</p>
          <p class="project-title">Selam Fashion</p>
          <p class="project-desc">Social media template system and content strategy for a modern Ethiopian fashion label targeting young professionals.</p>
        </div>
      </div>
      <div class="project">
        <div class="project-thumb t3"><i class="ti ti-layout"></i></div>
        <div class="project-info">
          <p class="project-tag">Poster &amp; print</p>
          <p class="project-title">Addis Music Festival</p>
          <p class="project-desc">Event branding, poster series, and promotional materials for a three-day music and arts festival.</p>
        </div>
      </div>
      <div class="project">
        <div class="project-thumb t4"><i class="ti ti-shirt"></i></div>
        <div class="project-info">
          <p class="project-tag">Merchandise</p>
          <p class="project-title">Unity Streetwear</p>
          <p class="project-desc">T-shirt collection design and brand development for an emerging streetwear label rooted in Ethiopian culture.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section class="services" id="services">
    <p class="section-label">Services &amp; pricing</p>
    <div class="services-grid">
      <div class="service-card">
        <i class="ti ti-pencil service-icon"></i>
        <div class="service-name">Starter</div>
        <div class="service-price">$150 <span>/ project</span></div>
        <div class="service-desc">Perfect for individuals and small businesses needing a clean, professional look.</div>
        <ul class="service-list">
          <li><i class="ti ti-check"></i> Logo design (2 concepts)</li>
          <li><i class="ti ti-check"></i> Color palette</li>
          <li><i class="ti ti-check"></i> 2 revision rounds</li>
          <li><i class="ti ti-check"></i> Source files</li>
        </ul>
      </div>
      <div class="service-card featured">
        <i class="ti ti-layers-difference service-icon"></i>
        <div class="service-badge">Most popular</div>
        <div class="service-name">Brand identity</div>
        <div class="service-price">$400 <span>/ project</span></div>
        <div class="service-desc">A complete brand system for businesses ready to make a serious impression.</div>
        <ul class="service-list">
          <li><i class="ti ti-check"></i> Logo + brand mark</li>
          <li><i class="ti ti-check"></i> Full brand guidelines</li>
          <li><i class="ti ti-check"></i> Business card &amp; letterhead</li>
          <li><i class="ti ti-check"></i> Social media kit</li>
          <li><i class="ti ti-check"></i> Unlimited revisions</li>
        </ul>
      </div>
      <div class="service-card">
        <i class="ti ti-sparkles service-icon"></i>
        <div class="service-name">Custom</div>
        <div class="service-price">Let's talk</div>
        <div class="service-desc">For campaigns, events, merchandise, or anything that needs a bespoke approach.</div>
        <ul class="service-list">
          <li><i class="ti ti-check"></i> Posters &amp; flyers</li>
          <li><i class="ti ti-check"></i> T-shirt &amp; merch design</li>
          <li><i class="ti ti-check"></i> Event branding</li>
          <li><i class="ti ti-check"></i> Ongoing retainer option</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- REVIEWS -->
  <section class="reviews" id="reviews">
    <div class="reviews-inner">
      <p class="section-label">Client reviews</p>
      <div class="rating-summary">
        <div class="rating-big">5.0</div>
        <div>
          <div class="rating-stars-static">
            <span>★</span><span>★</span><span>★</span><span>★</span><span>★</span>
          </div>
          <div class="rating-count">Based on 3 reviews</div>
        </div>
      </div>
      <div class="reviews-grid">
        <div class="review-card">
          <div class="review-stars"><span>★</span><span>★</span><span>★</span><span>★</span><span>★</span></div>
          <p class="review-text">"Mickyas delivered exactly what our brand needed. The logo is clean, memorable, and professional. Highly recommend."</p>
          <div class="review-author">
            <div class="review-avatar">AB</div>
            <div><div class="review-name">Abebe B.</div><div class="review-date">April 2026</div></div>
          </div>
        </div>
        <div class="review-card">
          <div class="review-stars"><span>★</span><span>★</span><span>★</span><span>★</span><span>★</span></div>
          <p class="review-text">"Amazing work on our social media kit. Fast, responsive, and the designs exceeded our expectations."</p>
          <div class="review-author">
            <div class="review-avatar">SL</div>
            <div><div class="review-name">Sara L.</div><div class="review-date">March 2026</div></div>
          </div>
        </div>
        <div class="review-card">
          <div class="review-stars"><span>★</span><span>★</span><span>★</span><span>★</span><span>★</span></div>
          <p class="review-text">"Our event posters looked incredible. MTS Design understands the brief and brings real creativity to every project."</p>
          <div class="review-author">
            <div class="review-avatar">DM</div>
            <div><div class="review-name">Daniel M.</div><div class="review-date">February 2026</div></div>
          </div>
        </div>
        <div class="leave-review-card">
          <p>Rate your experience with MTS Design</p>
          <div class="leave-stars" id="leave-stars">
            <span class="leave-star" data-v="1">★</span>
            <span class="leave-star" data-v="2">★</span>
            <span class="leave-star" data-v="3">★</span>
            <span class="leave-star" data-v="4">★</span>
            <span class="leave-star" data-v="5">★</span>
          </div>
          <div class="leave-feedback" id="leave-feedback"></div>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section class="contact" id="contact">
    <p class="section-label">Contact</p>
    <div class="contact-inner">
      <div>
        <h2>Let's build something great together.</h2>
        <p>Whether you have a clear brief or just a rough idea, we'd love to hear from you. We typically respond within 24 hours.</p>
        <div class="contact-channels">
          <a class="channel" href="mailto:mts.maren18@gmail.com">
            <i class="ti ti-mail"></i>
            <div class="channel-info"><p>Email</p><span>mts.maren18@gmail.com</span></div>
          </a>
          <a class="channel" href="tel:+251966008384">
            <i class="ti ti-phone"></i>
            <div class="channel-info"><p>Phone</p><span>+251 966 008 384</span></div>
          </a>
          <a class="channel" href="https://wa.me/251940786019" target="_blank">
            <i class="ti ti-brand-whatsapp"></i>
            <div class="channel-info"><p>WhatsApp</p><span>+251 940 786 019</span></div>
          </a>
          <a class="channel" href="https://t.me/Mickyas_T" target="_blank">
            <i class="ti ti-brand-telegram"></i>
            <div class="channel-info"><p>Telegram (direct)</p><span>@Mickyas_T</span></div>
          </a>
          <a class="channel" href="https://t.me/mts_design_all" target="_blank">
            <i class="ti ti-brand-telegram"></i>
            <div class="channel-info"><p>Telegram channel</p><span>t.me/mts_design_all</span></div>
          </a>
        </div>
      </div>
      <div class="contact-form">
        <div class="form-row">
          <div class="form-field">
            <label class="form-label">Name</label>
            <input type="text" placeholder="Your name" />
          </div>
          <div class="form-field">
            <label class="form-label">Email</label>
            <input type="email" placeholder="your@email.com" />
          </div>
        </div>
        <div class="form-field">
          <label class="form-label">Service interested in</label>
          <select>
            <option>Logo design</option>
            <option>Brand identity</option>
            <option>Posters &amp; flyers</option>
            <option>Social media graphics</option>
            <option>T-shirt design</option>
            <option>Other</option>
          </select>
        </div>
        <div class="form-field">
          <label class="form-label">Tell us about your project</label>
          <textarea placeholder="Describe your project, timeline, and budget..."></textarea>
        </div>
        <button class="btn-primary" style="align-self:flex-start">Send message</button>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>© 2026 MTS Design. All rights reserved.</p>
    <div class="footer-links">
      <a href="https://t.me/mts_design_all" target="_blank">Telegram</a>
      <a href="mailto:mts.maren18@gmail.com">Email</a>
      <a href="https://wa.me/251940786019" target="_blank">WhatsApp</a>
    </div>
  </footer>

  <script>
    const labels = ['Terrible', 'Poor', 'Okay', 'Good', 'Outstanding!'];
    const leaveStars = document.querySelectorAll('.leave-star');
    const feedback = document.getElementById('leave-feedback');
    let selected = 0;
    leaveStars.forEach(s => {
      s.addEventListener('mouseenter', () => {
        const v = parseInt(s.dataset.v);
        leaveStars.forEach(x => x.classList.toggle('hover', parseInt(x.dataset.v) <= v));
        feedback.textContent = labels[v - 1];
      });
      s.addEventListener('mouseleave', () => {
        leaveStars.forEach(x => x.classList.remove('hover'));
        feedback.textContent = selected ? labels[selected - 1] : '';
      });
      s.addEventListener('click', () => {
        selected = parseInt(s.dataset.v);
        leaveStars.forEach(x => x.classList.toggle('selected', parseInt(x.dataset.v) <= selected));
        feedback.textContent = labels[selected - 1] + ' — thank you for your feedback!';
      });
    });
  </script>

</body>
</html>
