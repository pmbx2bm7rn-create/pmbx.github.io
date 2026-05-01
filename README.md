# pmbx.github.io
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>1Games – Your #1 Free Gaming Hub | Play Now</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    :root {
      --bg: #050816;
      --bg-alt: #0b1020;
      --accent: #ff4b4b;
      --accent-soft: #ff9b4b;
      --text: #f5f5f5;
      --muted: #a0a4b8;
      --card: #111827;
      --border: #1f2937;
      --radius-lg: 18px;
      --radius-md: 12px;
      --radius-sm: 8px;
      --shadow-soft: 0 18px 40px rgba(0, 0, 0, 0.45);
      --shadow-chip: 0 10px 25px rgba(0, 0, 0, 0.35);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #111827 0, #020617 45%, #000 100%);
      color: var(--text);
      min-height: 100vh;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .page {
      max-width: 1200px;
      margin: 0 auto;
      padding: 24px 16px 48px;
    }

    /* Top bar */
    .topbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 24px;
      gap: 16px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .logo-icon {
      width: 40px;
      height: 40px;
      border-radius: 14px;
      background: conic-gradient(from 210deg, #ff4b4b, #ff9b4b, #4f46e5, #22c55e, #ff4b4b);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #fff;
      font-weight: 800;
      font-size: 20px;
      box-shadow: var(--shadow-chip);
    }

    .logo-text-main {
      font-weight: 800;
      font-size: 20px;
      letter-spacing: 0.04em;
    }

    .logo-text-sub {
      font-size: 11px;
      color: var(--muted);
      text-transform: uppercase;
      letter-spacing: 0.16em;
    }

    .top-actions {
      display: flex;
      align-items: center;
      gap: 10px;
      flex-wrap: wrap;
      justify-content: flex-end;
    }

    .pill {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 6px 10px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.3);
      color: var(--muted);
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.12em;
    }

    .pill-dot {
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: #22c55e;
      box-shadow: 0 0 0 4px rgba(34, 197, 94, 0.25);
    }

    .btn-ghost {
      padding: 7px 12px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      background: rgba(15, 23, 42, 0.9);
      color: var(--muted);
      font-size: 12px;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      cursor: pointer;
    }

    .btn-primary {
      padding: 8px 16px;
      border-radius: 999px;
      border: none;
      background: linear-gradient(135deg, #ff4b4b, #ff9b4b);
      color: #111827;
      font-size: 13px;
      font-weight: 600;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      cursor: pointer;
      box-shadow: 0 14px 30px rgba(248, 113, 113, 0.45);
    }

    .btn-primary span.icon {
      font-size: 16px;
    }

    /* Layout main */
    .layout {
      display: grid;
      grid-template-columns: minmax(0, 2.1fr) minmax(0, 1.4fr);
      gap: 22px;
    }

    @media (max-width: 900px) {
      .layout {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    /* Left column */
    .hero-card {
      background: radial-gradient(circle at top left, #1f2937 0, #020617 55%);
      border-radius: 26px;
      padding: 22px 20px 18px;
      border: 1px solid rgba(148, 163, 184, 0.35);
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    .hero-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 16px;
      margin-bottom: 18px;
    }

    .hero-title-block {
      max-width: 70%;
    }

    .hero-kicker {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--accent-soft);
      margin-bottom: 6px;
    }

    .hero-title {
      font-size: 26px;
      line-height: 1.15;
      font-weight: 800;
      margin-bottom: 6px;
    }

    .hero-subtitle {
      font-size: 13px;
      color: var(--muted);
      max-width: 360px;
    }

    .hero-badge {
      padding: 7px 10px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.4);
      font-size: 11px;
      color: var(--muted);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      white-space: nowrap;
    }

    .hero-badge-dot {
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: #22c55e;
    }

    .hero-main {
      display: grid;
      grid-template-columns: minmax(0, 1.6fr) minmax(0, 1.2fr);
      gap: 18px;
      align-items: stretch;
    }

    @media (max-width: 700px) {
      .hero-main {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .hero-games {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .section-label {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--muted);
    }

    .game-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 10px;
      margin-top: 6px;
    }

    @media (max-width: 600px) {
      .game-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    .game-card {
      background: radial-gradient(circle at top, #1f2937 0, #020617 70%);
      border-radius: 16px;
      padding: 10px 9px;
      border: 1px solid rgba(148, 163, 184, 0.35);
      box-shadow: 0 12px 26px rgba(0, 0, 0, 0.45);
      display: flex;
      flex-direction: column;
      gap: 6px;
      cursor: pointer;
      transition: transform 0.16s ease, box-shadow 0.16s ease, border-color 0.16s ease;
      position: relative;
      overflow: hidden;
    }

    .game-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 18px 40px rgba(0, 0, 0, 0.6);
      border-color: rgba(248, 250, 252, 0.6);
    }

    .game-thumb {
      height: 70px;
      border-radius: 12px;
      background: linear-gradient(135deg, #4f46e5, #22c55e);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 11px;
      font-weight: 600;
      color: #e5e7eb;
    }

    .game-title {
      font-size: 12px;
      font-weight: 600;
    }

    .game-meta {
      font-size: 10px;
      color: var(--muted);
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .tag {
      padding: 2px 6px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.4);
      font-size: 9px;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--muted);
    }

    .hero-cta {
      background: radial-gradient(circle at top right, #4f46e5 0, #020617 55%);
      border-radius: 18px;
      padding: 14px 14px 12px;
      border: 1px solid rgba(129, 140, 248, 0.6);
      box-shadow: 0 16px 40px rgba(79, 70, 229, 0.45);
      position: relative;
      overflow: hidden;
    }

    .hero-cta-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
      gap: 10px;
    }

    .hero-cta-title {
      font-size: 15px;
      font-weight: 700;
    }

    .hero-cta-sub {
      font-size: 11px;
      color: var(--muted);
      margin-bottom: 10px;
    }

    .hero-cta-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
      flex-wrap: wrap;
    }

    .hero-cta-stat {
      font-size: 11px;
      color: var(--muted);
    }

    .hero-cta-stat strong {
      color: #e5e7eb;
    }

    /* Categories + About */
    .bottom-row {
      margin-top: 18px;
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1.6fr);
      gap: 18px;
    }

    @media (max-width: 900px) {
      .bottom-row {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .categories-card,
    .about-card {
      background: var(--bg-alt);
      border-radius: 20px;
      padding: 16px 16px 14px;
      border: 1px solid var(--border);
      box-shadow: 0 14px 32px rgba(0, 0, 0, 0.5);
    }

    .section-title {
      font-size: 14px;
      font-weight: 700;
      margin-bottom: 8px;
    }

    .section-sub {
      font-size: 11px;
      color: var(--muted);
      margin-bottom: 12px;
    }

    .chip-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .chip {
      padding: 6px 10px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.4);
      font-size: 11px;
      color: #e5e7eb;
      cursor: pointer;
      transition: background 0.15s ease, border-color 0.15s ease, transform 0.15s ease;
    }

    .chip:hover {
      background: rgba(30, 64, 175, 0.9);
      border-color: rgba(191, 219, 254, 0.8);
      transform: translateY(-1px);
    }

    .chip.chip-primary {
      background: linear-gradient(135deg, #ff4b4b, #ff9b4b);
      color: #111827;
      border-color: transparent;
    }

    .about-body {
      font-size: 12px;
      color: var(--muted);
      line-height: 1.5;
      margin-bottom: 10px;
    }

    .about-body p + p {
      margin-top: 6px;
    }

    .about-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 10px;
      flex-wrap: wrap;
      font-size: 11px;
      color: var(--muted);
    }

    .about-footer strong {
      color: #e5e7eb;
    }

    /* Right column */
    .sidebar {
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .sidebar-card {
      background: var(--bg-alt);
      border-radius: 20px;
      padding: 14px 14px 12px;
      border: 1px solid var(--border);
      box-shadow: 0 14px 32px rgba(0, 0, 0, 0.5);
    }

    .sidebar-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 8px;
      gap: 10px;
    }

    .sidebar-title {
      font-size: 13px;
      font-weight: 700;
    }

    .sidebar-sub {
      font-size: 11px;
      color: var(--muted);
    }

    .sidebar-list {
      display: grid;
      grid-template-columns: minmax(0, 1fr);
      gap: 8px;
      margin-top: 8px;
    }

    .sidebar-item {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      padding: 8px 9px;
      border-radius: 12px;
      background: radial-gradient(circle at left, #1f2937 0, #020617 70%);
      border: 1px solid rgba(148, 163, 184, 0.35);
      cursor: pointer;
      transition: transform 0.15s ease, box-shadow 0.15s ease, border-color 0.15s ease;
    }

    .sidebar-item:hover {
      transform: translateY(-2px);
      box-shadow: 0 14px 30px rgba(0, 0, 0, 0.6);
      border-color: rgba(248, 250, 252, 0.6);
    }

    .sidebar-item-main {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .sidebar-thumb {
      width: 32px;
      height: 32px;
      border-radius: 10px;
      background: linear-gradient(135deg, #22c55e, #4f46e5);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 11px;
      color: #e5e7eb;
      font-weight: 600;
    }

    .sidebar-text {
      display: flex;
      flex-direction: column;
      gap: 2px;
    }

    .sidebar-game-title {
      font-size: 12px;
      font-weight: 600;
    }

    .sidebar-game-meta {
      font-size: 10px;
      color: var(--muted);
    }

    .sidebar-pill {
      font-size: 10px;
      color: var(--muted);
      padding: 3px 7px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      background: rgba(15, 23, 42, 0.9);
    }

    /* Footer mini */
    .mini-footer {
      margin-top: 22px;
      font-size: 11px;
      color: var(--muted);
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      justify-content: space-between;
      border-top: 1px solid rgba(31, 41, 55, 0.9);
      padding-top: 12px;
    }

    .mini-footer-links {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .mini-footer a {
      color: var(--muted);
    }

    .mini-footer a:hover {
      color: #e5e7eb;
    }
  </style>
</head>
<body>
  <div class="page">
    <!-- Top bar -->
    <header class="topbar">
      <div class="logo">
        <div class="logo-icon">1G</div>
        <div>
          <div class="logo-text-main">1Games</div>
          <div class="logo-text-sub">Your #1 free gaming hub</div>
        </div>
      </div>
      <div class="top-actions">
        <div class="pill">
          <span class="pill-dot"></span>
          <span>Instant play · No downloads</span>
        </div>
        <button class="btn-ghost" type="button">
          <span>My Games</span>
        </button>
        <button class="btn-primary" type="button">
          <span class="icon">▶</span>
          <span>Play random game</span>
        </button>
      </div>
    </header>

    <main class="layout">
      <!-- Left column -->
      <section>
        <div class="hero-card">
          <div class="hero-header">
            <div class="hero-title-block">
              <div class="hero-kicker">Free browser games</div>
              <h1 class="hero-title">Welcome to your new online playground.</h1>
              <p class="hero-subtitle">
                Play action, arcade, .io, puzzle, sports, horror, and more—instantly on any device, with zero downloads or paywalls.
              </p>
            </div>
            <div class="hero-badge">
              <span class="hero-badge-dot"></span>
              <span>New games added weekly</span>
            </div>
          </div>

          <div class="hero-main">
            <!-- Featured games -->
            <div class="hero-games">
              <div class="section-label">New games</div>
              <div class="game-grid">
                <article class="game-card">
                  <div class="game-thumb">Dash through the beat</div>
                  <div class="game-title">Dashmetry</div>
                  <div class="game-meta">
                    <span>Rhythm · Platformer</span>
                    <span class="tag">New</span>
                  </div>
                </article>

                <article class="game-card">
                  <div class="game-thumb">Smarter chases</div>
                  <div class="game-title">Escape Road 3</div>
                  <div class="game-meta">
                    <span>Driving · Action</span>
                    <span class="tag">Hot</span>
                  </div>
                </article>

                <article class="game-card">
                  <div class="game-thumb">Chaos unleashed</div>
                  <div class="game-title">Car Chaos</div>
                  <div class="game-meta">
                    <span>Arcade · Physics</span>
                    <span class="tag">Top</span>
                  </div>
                </article>

                <article class="game-card">
                  <div class="game-thumb">Perfect timing</div>
                  <div class="game-title">Wacky Steps</div>
                  <div class="game-meta">
                    <span>Casual · Skill</span>
                    <span class="tag">Fun</span>
                  </div>
                </article>

                <article class="game-card">
                  <div class="game-thumb">Endless slope</div>
                  <div class="game-title">Slope 2</div>
                  <div class="game-meta">
                    <span>Arcade · Reflex</span>
                    <span class="tag">Classic</span>
                  </div>
                </article>

                <article class="game-card">
                  <div class="game-thumb">Pixel-perfect</div>
                  <div class="game-title">Pixel Path</div>
                  <div class="game-meta">
                    <span>Puzzle · Retro</span>
                    <span class="tag">Chill</span>
                  </div>
                </article>
              </div>
            </div>

            <!-- CTA / highlight -->
            <aside class="hero-cta">
              <div class="hero-cta-header">
                <div>
                  <div class="section-label">Why 1Games?</div>
                  <div class="hero-cta-title">Free, fast, and interruption‑free.</div>
                </div>
                <div class="pill">
                  <span>Family‑friendly</span>
                </div>
              </div>
              <p class="hero-cta-sub">
                No downloads, no logins, no in‑game purchases. Just click, play, and discover your next favorite game in seconds.
              </p>
              <div class="hero-cta-footer">
                <div class="hero-cta-stat">
                  <strong>All genres:</strong> Action, arcade, .io, puzzle, sports, horror, and more.
                </div>
                <button class="btn-primary" type="button">
                  <span class="icon">🎮</span>
                  <span>Start playing now</span>
                </button>
              </div>
            </aside>
          </div>

          <!-- Categories + About -->
          <div class="bottom-row">
            <section class="categories-card">
              <h2 class="section-title">Browse by category</h2>
              <p class="section-sub">
                Jump straight into the genre you’re in the mood for.
              </p>
              <div class="chip-row">
                <button class="chip chip-primary" type="button">Action</button>
                <button class="chip" type="button">Adventure</button>
                <button class="chip" type="button">Arcade</button>
                <button class="chip" type="button">Clicker</button>
                <button class="chip" type="button">Driving</button>
                <button class="chip" type="button">Horror</button>
                <button class="chip" type="button">.IO</button>
                <button class="chip" type="button">Puzzle</button>
                <button class="chip" type="button">Shooting</button>
                <button class="chip" type="button">Sports</button>
                <button class="chip" type="button">Survival</button>
                <button class="chip" type="button">Casual</button>
                <button class="chip" type="button">Simulation</button>
                <button class="chip" type="button">Platform</button>
                <button class="chip" type="button">Music</button>
                <button class="chip" type="button">Strategy</button>
              </div>
            </section>

            <section class="about-card">
              <h2 class="section-title">About 1Games</h2>
              <p class="about-body">
                1Games is a multi‑genre platform built to be the most comprehensive online playground—free and accessible to everyone.
                Every game is available for instant play with no downloads, logins, pop‑ups, or interruptions.
              </p>
              <p class="about-body">
                There are no in‑game purchases in any of our games. You get the full experience up front, without hidden costs or
                pay‑to‑win mechanics.
              </p>
              <p class="about-body">
                All games adapt to your screen and work on desktop, tablet, and mobile. Start on your PC, continue on your phone—same
                game, same progress, same fun.
              </p>
              <div class="about-footer">
                <span><strong>Motto:</strong> Create the best playground for all players.</span>
                <span>We update regularly—your feedback shapes what comes next.</span>
              </div>
            </section>
          </div>
        </div>

        <!-- Mini footer -->
        <footer class="mini-footer">
          <div class="mini-footer-links">
            <a href="#">About Us</a>
            <a href="#">Contact Us</a>
            <a href="#">DMCA</a>
            <a href="#">Privacy Policy</a>
            <a href="#">Terms of Service</a>
          </div>
          <div>© 1Games · Play free browser games—no downloads, no paywalls.</div>
        </footer>
      </section>

      <!-- Right column: lists -->
      <aside class="sidebar">
        <section class="sidebar-card">
          <div class="sidebar-header">
            <div>
              <div class="sidebar-title">Trending now</div>
              <div class="sidebar-sub">What players are clicking on today.</div>
            </div>
            <div class="sidebar-pill">Live</div>
          </div>
          <div class="sidebar-list">
            <article class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-thumb">SH</div>
                <div class="sidebar-text">
                  <div class="sidebar-game-title">Stick Hero RPG: Undead Invasion</div>
                  <div class="sidebar-game-meta">Action · RPG</div>
                </div>
              </div>
              <div class="sidebar-pill">Hot</div>
            </article>

            <article class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-thumb">SR</div>
                <div class="sidebar-text">
                  <div class="sidebar-game-title">Slope Rider</div>
                  <div class="sidebar-game-meta">Arcade · Reflex</div>
                </div>
              </div>
              <div class="sidebar-pill">Arcade</div>
            </article>

            <article class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-thumb">RP</div>
                <div class="sidebar-text">
                  <div class="sidebar-game-title">Rob Brainrot 2</div>
                  <div class="sidebar-game-meta">Casual · Meme</div>
                </div>
              </div>
              <div class="sidebar-pill">New</div>
            </article>

            <article class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-thumb">TS</div>
                <div class="sidebar-text">
                  <div class="sidebar-game-title">Tsunamis.io</div>
                  <div class="sidebar-game-meta">.IO · Survival</div>
                </div>
              </div>
              <div class="sidebar-pill">.IO</div>
            </article>
          </div>
        </section>

        <section class="sidebar-card">
          <div class="sidebar-header">
            <div>
              <div class="sidebar-title">Top played</div>
              <div class="sidebar-sub">All‑time favorites on 1Games.</div>
            </div>
            <div class="sidebar-pill">All time</div>
          </div>
          <div class="sidebar-list">
            <article class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-thumb">DM</div>
                <div class="sidebar-text">
                  <div class="sidebar-game-title">Dashmetry</div>
                  <div class="sidebar-game-meta">Rhythm · Platformer</div>
                </div>
              </div>
              <div class="sidebar-pill">#1</div>
            </article>

            <article class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-thumb">SL</div>
                <div class="sidebar-text">
                  <div class="sidebar-game-title">Slope 2</div>
                  <div class="sidebar-game-meta">Arcade · Reflex</div>
                </div>
              </div>
              <div class="sidebar-pill">Arcade</div>
            </article>

            <article class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-thumb">WB</div>
                <div class="sidebar-text">
                  <div class="sidebar-game-title">Wacky Steps</div>
                  <div class="sidebar-game-meta">Casual · Skill</div>
                </div>
              </div>
              <div class="sidebar-pill">Skill</div>
            </article>

            <article class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-thumb">CC</div>
                <div class="sidebar-text">
                  <div class="sidebar-game-title">Car Chaos</div>
                  <div class="sidebar-game-meta">Driving · Action</div>
                </div>
              </div>
              <div class="sidebar-pill">Driving</div>
            </article>
          </div>
        </section>

        <section class="sidebar-card">
          <div class="sidebar-header">
            <div>
              <div class="sidebar-title">My games</div>
              <div class="sidebar-sub">Favorites and last played.</div>
            </div>
            <div class="sidebar-pill">Signed‑out</div>
          </div>
          <p class="sidebar-sub">
            No favorite games yet. Keep playing, and when you find one you love, hit the ♥ to save it here.
          </p>
        </section>
      </aside>
    </main>
  </div>

  <script>
    // Example: simple “Play random game” behavior stub
    const randomBtn = document.querySelector('.btn-primary');
    const gameCards = Array.from(document.querySelectorAll('.game-card'));

    randomBtn?.addEventListener('click', () => {
      if (!gameCards.length) return;
      const random = gameCards[Math.floor(Math.random() * gameCards.length)];
      random.scrollIntoView({ behavior: 'smooth', block: 'center' });
      random.style.outline = '2px solid #f97316';
      random.style.outlineOffset = '3px';
      setTimeout(() => {
        random.style.outline = 'none';
        random.style.outlineOffset = '0';
      }, 1200);
    });
  </script>
</body>
</html>
