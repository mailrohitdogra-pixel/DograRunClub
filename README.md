<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Dogra Run Club | Vijaypur</title>
  <meta name="description" content="Dogra Run Club - Vijaypur's community running movement. Run together. Stronger together.">
  <meta name="theme-color" content="#080808">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&family=Oswald:wght@500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --black: #070707;
      --dark: #0d0d0d;
      --card: #121212;
      --card-light: #181818;
      --white: #ffffff;
      --muted: #a4a4a4;
      --orange: #ff6a00;
      --orange-light: #ff8a3d;
      --border: rgba(255,255,255,0.09);
      --max: 1180px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--black);
      color: var(--white);
      font-family: "Inter", sans-serif;
      overflow-x: hidden;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    .container {
      width: min(92%, var(--max));
      margin: auto;
    }

    /* ================= NAVBAR ================= */

    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      padding: 18px 0;
      background: rgba(7,7,7,0.72);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(255,255,255,0.06);
    }

    .nav-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 900;
      letter-spacing: 1px;
    }

    .brand img {
      width: 42px;
      height: 42px;
      object-fit: contain;
    }

    .brand span {
      font-size: 14px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 30px;
      font-size: 13px;
      font-weight: 600;
      color: #ddd;
    }

    .nav-links a {
      transition: 0.25s ease;
    }

    .nav-links a:hover {
      color: var(--orange);
    }

    .nav-cta {
      background: var(--white);
      color: #000;
      padding: 11px 18px;
      border-radius: 100px;
      font-size: 12px;
      font-weight: 800;
    }

    .nav-cta:hover {
      background: var(--orange);
      color: #fff;
    }

    /* ================= HERO ================= */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
      padding: 140px 0 80px;
      background:
        radial-gradient(circle at 75% 35%, rgba(255,106,0,0.16), transparent 28%),
        linear-gradient(120deg, #050505 0%, #0b0b0b 55%, #111 100%);
    }

    .hero::after {
      content: "";
      position: absolute;
      width: 500px;
      height: 500px;
      right: -200px;
      bottom: -250px;
      background: var(--orange);
      opacity: 0.08;
      filter: blur(100px);
      border-radius: 50%;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 850px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--orange);
      font-size: 12px;
      font-weight: 800;
      letter-spacing: 2px;
      text-transform: uppercase;
      margin-bottom: 25px;
    }

    .eyebrow::before {
      content: "";
      width: 30px;
      height: 2px;
      background: var(--orange);
    }

    .hero h1 {
      font-family: "Oswald", sans-serif;
      font-size: clamp(70px, 13vw, 170px);
      line-height: 0.84;
      letter-spacing: -3px;
      text-transform: uppercase;
      max-width: 900px;
    }

    .hero h1 span {
      color: var(--orange);
    }

    .hero-subtitle {
      margin-top: 32px;
      max-width: 600px;
      font-size: clamp(18px, 2vw, 24px);
      line-height: 1.5;
      color: #c7c7c7;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 35px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 15px 24px;
      border-radius: 100px;
      font-size: 13px;
      font-weight: 800;
      transition: 0.25s ease;
    }

    .btn-primary {
      background: var(--orange);
      color: #fff;
      box-shadow: 0 10px 35px rgba(255,106,0,0.18);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      background: var(--orange-light);
    }

    .btn-secondary {
      border: 1px solid var(--border);
      color: #fff;
      background: rgba(255,255,255,0.03);
    }

    .btn-secondary:hover {
      background: #fff;
      color: #000;
    }

    .hero-bottom {
      position: absolute;
      bottom: 35px;
      left: 0;
      width: 100%;
      z-index: 2;
    }

    .scroll-text {
      font-size: 10px;
      letter-spacing: 2px;
      text-transform: uppercase;
      color: #666;
    }

    /* ================= STATS ================= */

    .stats {
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      background: #0a0a0a;
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
    }

    .stat {
      padding: 34px 20px;
      border-right: 1px solid var(--border);
    }

    .stat:last-child {
      border-right: none;
    }

    .stat-number {
      font-family: "Oswald", sans-serif;
      font-size: 42px;
      color: var(--white);
    }

    .stat-label {
      margin-top: 4px;
      font-size: 11px;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    /* ================= SECTIONS ================= */

    section {
      padding: 110px 0;
    }

    .section-kicker {
      color: var(--orange);
      font-size: 11px;
      letter-spacing: 2px;
      font-weight: 800;
      text-transform: uppercase;
      margin-bottom: 14px;
    }

    .section-title {
      font-family: "Oswald", sans-serif;
      font-size: clamp(44px, 7vw, 82px);
      line-height: 0.95;
      text-transform: uppercase;
      max-width: 800px;
    }

    .section-title span {
      color: var(--orange);
    }

    .section-intro {
      color: var(--muted);
      max-width: 650px;
      line-height: 1.7;
      margin-top: 22px;
      font-size: 16px;
    }

    /* ================= FEATURE EVENT ================= */

    .event-section {
      background:
        linear-gradient(135deg, #121212 0%, #090909 100%);
    }

    .event-card {
      margin-top: 50px;
      border: 1px solid var(--border);
      border-radius: 28px;
      overflow: hidden;
      background: #101010;
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      min-height: 500px;
    }

    .event-visual {
      position: relative;
      min-height: 450px;
      background:
        radial-gradient(circle at 70% 30%, rgba(255,106,0,0.45), transparent 25%),
        linear-gradient(135deg, #1c1c1c, #080808);
      display: flex;
      align-items: flex-end;
      padding: 42px;
      overflow: hidden;
    }

    .event-visual::before {
      content: "DRC";
      position: absolute;
      top: -45px;
      right: -20px;
      font-family: "Oswald", sans-serif;
      font-size: 220px;
      font-weight: 700;
      color: rgba(255,255,255,0.025);
    }

    .event-label {
      position: relative;
      z-index: 2;
      background: var(--orange);
      color: #fff;
      padding: 8px 13px;
      border-radius: 100px;
      font-size: 10px;
      font-weight: 900;
      letter-spacing: 1px;
      text-transform: uppercase;
    }

    .event-details {
      padding: 50px;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .event-details h3 {
      font-family: "Oswald", sans-serif;
      font-size: clamp(42px, 5vw, 68px);
      line-height: 0.95;
      text-transform: uppercase;
    }

    .event-details h3 span {
      color: var(--orange);
    }

    .event-date {
      margin-top: 24px;
      font-size: 14px;
      color: #ddd;
      font-weight: 700;
    }

    .event-meta {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 10px;
      margin-top: 28px;
    }

    .meta-box {
      background: #171717;
      border: 1px solid var(--border);
      padding: 17px;
      border-radius: 14px;
    }

    .meta-box small {
      color: #777;
      display: block;
      font-size: 9px;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 5px;
    }

    .meta-box strong {
      font-size: 15px;
    }

    .event-note {
      margin-top: 22px;
      font-size: 12px;
      line-height: 1.6;
      color: var(--muted);
    }

    .event-button {
      margin-top: 28px;
    }

    /* ================= RUNS ================= */

    .runs-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
      margin-top: 50px;
    }

    .run-card {
      padding: 35px;
      border: 1px solid var(--border);
      background: var(--card);
      border-radius: 22px;
      transition: 0.3s ease;
      position: relative;
      overflow: hidden;
    }

    .run-card:hover {
      transform: translateY(-6px);
      border-color: rgba(255,106,0,0.4);
    }

    .run-card::after {
      content: "";
      position: absolute;
      width: 150px;
      height: 150px;
      right: -70px;
      bottom: -70px;
      border-radius: 50%;
      background: var(--orange);
      opacity: 0.06;
    }

    .run-day {
      font-size: 11px;
      color: var(--orange);
      font-weight: 900;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .run-card h3 {
      font-family: "Oswald", sans-serif;
      font-size: 48px;
      text-transform: uppercase;
      margin: 10px 0 20px;
    }

    .run-info {
      color: #bbb;
      line-height: 2;
      font-size: 14px;
    }

    .run-free {
      display: inline-block;
      margin-top: 22px;
      color: #fff;
      background: #202020;
      padding: 8px 13px;
      border-radius: 100px;
      font-size: 10px;
      font-weight: 800;
      text-transform: uppercase;
    }

    /* ================= ABOUT ================= */

    .about {
      background: #f4f4f4;
      color: #080808;
    }

    .about .section-kicker {
      color: var(--orange);
    }

    .about .section-title {
      max-width: 900px;
    }

    .about-text {
      margin-top: 35px;
      max-width: 760px;
      font-size: clamp(22px, 3vw, 34px);
      line-height: 1.35;
      font-weight: 600;
    }

    .about-text strong {
      color: var(--orange);
    }

    .values {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
      margin-top: 55px;
    }

    .value {
      padding: 30px;
      border: 1px solid #ddd;
      border-radius: 18px;
      background: #fff;
    }

    .value-number {
      font-family: "Oswald", sans-serif;
      color: var(--orange);
      font-size: 16px;
    }

    .value h3 {
      font-size: 18px;
      margin: 35px 0 10px;
    }

    .value p {
      font-size: 13px;
      color: #666;
      line-height: 1.6;
    }

    /* ================= GALLERY ================= */

    .gallery-grid {
      margin-top: 50px;
      display: grid;
      grid-template-columns: 1.4fr 1fr 1fr;
      grid-auto-rows: 230px;
      gap: 12px;
    }

    .gallery-item {
      background:
        linear-gradient(135deg, #191919, #0b0b0b);
      border-radius: 16px;
      border: 1px solid var(--border);
      overflow: hidden;
      position: relative;
    }

    .gallery-item.large {
      grid-row: span 2;
    }

    .gallery-item::after {
      content: "DRC";
      position: absolute;
      left: 18px;
      bottom: 15px;
      font-family: "Oswald", sans-serif;
      font-size: 28px;
      color: rgba(255,255,255,0.25);
    }

    /* ================= CTA ================= */

    .final-cta {
      padding: 130px 0;
      background:
        radial-gradient(circle at center, rgba(255,106,0,0.17), transparent 40%),
        #080808;
      text-align: center;
    }

    .final-cta h2 {
      font-family: "Oswald", sans-serif;
      font-size: clamp(60px, 11vw, 130px);
      line-height: 0.85;
      text-transform: uppercase;
    }

    .final-cta h2 span {
      color: var(--orange);
    }

    .final-cta p {
      max-width: 500px;
      margin: 25px auto 0;
      color: #999;
      line-height: 1.6;
    }

    .final-actions {
      margin-top: 32px;
    }

    /* ================= FOOTER ================= */

    footer {
      padding: 50px 0 100px;
      border-top: 1px solid var(--border);
      background: #050505;
    }

    .footer-top {
      display: flex;
      justify-content: space-between;
      gap: 30px;
      align-items: flex-start;
    }

    .footer-brand {
      font-family: "Oswald", sans-serif;
      font-size: 32px;
      text-transform: uppercase;
    }

    .footer-brand span {
      color: var(--orange);
    }

    .footer-links {
      display: flex;
      gap: 25px;
      color: #888;
      font-size: 12px;
    }

    .footer-links a:hover {
      color: #fff;
    }

    .copyright {
      margin-top: 50px;
      color: #555;
      font-size: 11px;
    }

    /* ================= MOBILE CTA ================= */

    .mobile-cta {
      display: none;
    }

    /* ================= RESPONSIVE ================= */

    @media (max-width: 850px) {

      .nav-links {
        display: none;
      }

      .nav-cta {
        display: block;
      }

      .hero {
        min-height: 92vh;
        padding-top: 130px;
      }

      .hero h1 {
        letter-spacing: -1px;
      }

      .stats-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .stat:nth-child(2) {
        border-right: none;
      }

      .stat:nth-child(1),
      .stat:nth-child(2) {
        border-bottom: 1px solid var(--border);
      }

      .event-card {
        grid-template-columns: 1fr;
      }

      .event-visual {
        min-height: 280px;
      }

      .runs-grid {
        grid-template-columns: 1fr;
      }

      .values {
        grid-template-columns: 1fr;
      }

      .gallery-grid {
        grid-template-columns: 1fr 1fr;
        grid-auto-rows: 180px;
      }

      .gallery-item.large {
        grid-row: span 2;
      }
    }

    @media (max-width: 600px) {

      body {
        padding-bottom: 70px;
      }

      nav {
        padding: 12px 0;
      }

      .brand img {
        width: 35px;
        height: 35px;
      }

      .brand span {
        font-size: 12px;
      }

      .nav-cta {
        padding: 9px 14px;
        font-size: 10px;
      }

      .hero {
        min-height: 88vh;
        padding: 120px 0 70px;
      }

      .hero h1 {
        font-size: clamp(62px, 18vw, 100px);
      }

      .hero-subtitle {
        font-size: 16px;
      }

      .hero-actions {
        flex-direction: column;
        align-items: stretch;
      }

      .btn {
        width: 100%;
      }

      section {
        padding: 80px 0;
      }

      .event-details {
        padding: 30px 24px;
      }

      .event-visual {
        padding: 25px;
        min-height: 220px;
      }

      .event-meta {
        grid-template-columns: 1fr;
      }

      .run-card {
        padding: 28px;
      }

      .run-card h3 {
        font-size: 40px;
      }

      .gallery-grid {
        grid-template-columns: 1fr 1fr;
        grid-auto-rows: 150px;
      }

      .footer-top {
        flex-direction: column;
      }

      .footer-links {
        flex-wrap: wrap;
      }

      .mobile-cta {
        display: block;
        position: fixed;
        bottom: 0;
        left: 0;
        width: 100%;
        z-index: 999;
        padding: 10px;
        background: rgba(5,5,5,0.92);
        backdrop-filter: blur(15px);
        border-top: 1px solid var(--border);
      }

      .mobile-cta a {
        display: block;
        background: var(--orange);
        text-align: center;
        padding: 14px;
        border-radius: 12px;
        font-size: 12px;
        font-weight: 900;
        text-transform: uppercase;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <nav>
    <div class="container nav-inner">

      <a href="#" class="brand">
        <img src="logo.jpg.png" alt="Dogra Run Club">
        <span>DOGRA RUN CLUB</span>
      </a>

      <div class="nav-links">
        <a href="#events">Events</a>
        <a href="#runs">Runs</a>
        <a href="#about">About</a>
        <a href="#community">Community</a>
      </div>

      <a
        href="https://chat.whatsapp.com/CBqkjRm5SBoAucOudYO0F7?s=cl&p=i&mlu=2"
        class="nav-cta"
        target="_blank"
      >
        JOIN DRC
      </a>

    </div>
  </nav>


  <!-- HERO -->

  <header class="hero">

    <div class="container">

      <div class="hero-content">

        <div class="eyebrow">
          VIJAYPUR • JAMMU
        </div>

        <h1>
          DOGRA<br>
          RUN <span>CLUB</span>
        </h1>

        <p class="hero-subtitle">
          A community built around running, fitness and showing up.
          No pressure. No competition. Just better mornings together.
        </p>

        <div class="hero-actions">

          <a href="#events" class="btn btn-primary">
            VIEW NEXT EVENT →
          </a>

          <a
            href="https://chat.whatsapp.com/CBqkjRm5SBoAucOudYO0F7?s=cl&p=i&mlu=2"
            class="btn btn-secondary"
            target="_blank"
          >
            JOIN COMMUNITY
          </a>

        </div>

      </div>

    </div>

    <div class="hero-bottom">
      <div class="container">
        <div class="scroll-text">
          RUN TOGETHER. STRONGER TOGETHER.
        </div>
      </div>
    </div>

  </header>


  <!-- STATS -->

  <div class="stats">

    <div class="container stats-grid">

      <div class="stat">
        <div class="stat-number">17+</div>
        <div class="stat-label">Community Runs</div>
      </div>

      <div class="stat">
        <div class="stat-number">5K+</div>
        <div class="stat-label">Miles Together</div>
      </div>

      <div class="stat">
        <div class="stat-number">100+</div>
        <div class="stat-label">People in the Movement</div>
      </div>

      <div class="stat">
        <div class="stat-number">FREE</div>
        <div class="stat-label">Community Runs</div>
      </div>

    </div>

  </div>


  <!-- FEATURE EVENT -->

  <section class="event-section" id="events">

    <div class="container">

      <div class="section-kicker">
        NEXT UP
      </div>

      <h2 class="section-title">
        RUN.<br>
        <span>REFRESH.</span><br>
        REPEAT.
      </h2>

      <div class="event-card">

        <div class="event-visual">

          <div class="event-label">
            DRC SPECIAL EVENT
          </div>

        </div>

        <div class="event-details">

          <div class="section-kicker">
            04 OCTOBER 2026
          </div>

          <h3>
            DRC ×<br>
            <span>DIVE & DINE</span>
          </h3>

          <div class="event-date">
            5K RUN • POOL • DJ • REFRESHMENTS
          </div>

          <div class="event-meta">

            <div class="meta-box">
              <small>Run</small>
              <strong>6:00 AM</strong>
            </div>

            <div class="meta-box">
              <small>Pool</small>
              <strong>₹179</strong>
            </div>

            <div class="meta-box">
              <small>Run Entry</small>
              <strong>FREE</strong>
            </div>

            <div class="meta-box">
              <small>Pool Passes</small>
              <strong>100 ONLY</strong>
            </div>

          </div>

          <p class="event-note">
            The run is free. Pool access is optional and separately
            priced. Refreshments will be provided by DRC.
            Food at the venue is not included.
          </p>

          <div class="event-button">

            <a href="#" class="btn btn-primary">
              REGISTER FOR EVENT →
            </a>

          </div>

        </div>

      </div>

    </div>

  </section>


  <!-- WEEKLY RUNS -->

  <section id="runs">

    <div class="container">

      <div class="section-kicker">
        EVERY WEEK
      </div>

      <h2 class="section-title">
        SHOW UP.<br>
        <span>PUT IN THE MILES.</span>
      </h2>

      <p class="section-intro">
        Two regular opportunities every week to get outside,
        move your body and run with people who actually show up.
      </p>

      <div class="runs-grid">

        <div class="run-card">

          <div class="run-day">
            SUNDAY
          </div>

          <h3>
            Sunday<br>Run
          </h3>

          <div class="run-info">
            06:00 AM<br>
            Vijaypur, Jammu<br>
            Meet at FitZone Gym
          </div>

          <div class="run-free">
            Open for all • Free
          </div>

        </div>


        <div class="run-card">

          <div class="run-day">
            WEDNESDAY
          </div>

          <h3>
            Wednesday<br>Rush
          </h3>

          <div class="run-info">
            06:00 AM<br>
            Ring Road<br>
            Zamindara Dhaba
          </div>

          <div class="run-free">
            10K • Open for all
          </div>

        </div>

      </div>

    </div>

  </section>


  <!-- ABOUT -->

  <section class="about" id="about">

    <div class="container">

      <div class="section-kicker">
        WHO WE ARE
      </div>

      <h2 class="section-title">
        WE CREATE<br>
        <span>RUNNERS.</span>
      </h2>

      <p class="about-text">
        Dogra Run Club is a community for people who want to
        <strong>start running, stay consistent and become better.</strong>
        Beginners, regular runners, walkers and everyone in between.
      </p>

      <div class="values">

        <div class="value">

          <div class="value-number">
            01
          </div>

          <h3>NO PRESSURE</h3>

          <p>
            No race. No competition. Run at your own pace and
            keep moving forward.
          </p>

        </div>


        <div class="value">

          <div class="value-number">
            02
          </div>

          <h3>EVERYONE WELCOME</h3>

          <p>
            You don't have to call yourself a runner before
            joining a running club.
          </p>

        </div>


        <div class="value">

          <div class="value-number">
            03
          </div>

          <h3>COMMUNITY FIRST</h3>

          <p>
            Fitness becomes easier when you're surrounded by
            people who keep showing up.
          </p>

        </div>

      </div>

    </div>

  </section>


  <!-- GALLERY -->

  <section>

    <div class="container">

      <div class="section-kicker">
        THE MOVEMENT
      </div>

      <h2 class="section-title">
        MILES.<br>
        <span>MEMORIES.</span>
      </h2>

      <p class="section-intro">
        From early morning miles to post-run madness,
        this is what the DRC community looks like.
      </p>

      <div class="gallery-grid">

        <!-- Replace these blocks with your actual DRC photos -->

        <div class="gallery-item large"></div>

        <div class="gallery-item"></div>

        <div class="gallery-item"></div>

        <div class="gallery-item"></div>

        <div class="gallery-item"></div>

      </div>

    </div>

  </section>


  <!-- COMMUNITY CTA -->

  <section class="final-cta" id="community">

    <div class="container">

      <div class="section-kicker">
        YOUR NEXT RUN STARTS HERE
      </div>

      <h2>
        DON'T<br>
        <span>RUN ALONE.</span>
      </h2>

      <p>
        Join the Dogra Run Club community and be part of
        the movement growing in Vijaypur.
      </p>

      <div class="final-actions">

        <a
          href="https://chat.whatsapp.com/CBqkjRm5SBoAucOudYO0F7?s=cl&p=i&mlu=2"
          class="btn btn-primary"
          target="_blank"
        >
          JOIN DRC WHATSAPP →
        </a>

      </div>

    </div>

  </section>


  <!-- FOOTER -->

  <footer>

    <div class="container">

      <div class="footer-top">

        <div class="footer-brand">
          DOGRA RUN <span>CLUB</span>
        </div>

        <div class="footer-links">

          <a href="#events">Events</a>
          <a href="#runs">Runs</a>
          <a href="#about">About</a>

          <a
            href="https://instagram.com/dograrunclub"
            target="_blank"
          >
            Instagram
          </a>

        </div>

      </div>

      <div class="copyright">
        © 2026 Dogra Run Club Vijaypur. Run Together. Stronger Together.
      </div>

    </div>

  </footer>


  <!-- MOBILE STICKY CTA -->

  <div class="mobile-cta">

    <a
      href="https://chat.whatsapp.com/CBqkjRm5SBoAucOudYO0F7?s=cl&p=i&mlu=2"
      target="_blank"
    >
      JOIN DRC COMMUNITY →
    </a>

  </div>


</body>
</html>
