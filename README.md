<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Geeta Mehra — README.md Preview</title>
  <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700;800;900&family=Space+Grotesk:wght@300;400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg: #0d1117;
      --surface: #161b22;
      --surface2: #1c2230;
      --border: #30363d;
      --text: #e6edf3;
      --muted: #8b949e;
      --accent: #58a6ff;
      --green: #3fb950;
      --purple: #bc8cff;
      --pink: #ff7b72;
      --orange: #ffa657;
      --teal: #39d353;
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Inter', sans-serif;
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* ─── SCROLLBAR ─── */
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: var(--bg); }
    ::-webkit-scrollbar-thumb { background: linear-gradient(180deg,#58a6ff,#bc8cff); border-radius: 3px; }

    /* ─── BACKGROUND PARTICLES ─── */
    #particles-bg {
      position: fixed; inset: 0; pointer-events: none; z-index: 0; overflow: hidden;
    }
    .star {
      position: absolute;
      border-radius: 50%;
      background: #fff;
      animation: twinkle var(--dur, 3s) ease-in-out infinite var(--delay, 0s);
    }
    @keyframes twinkle {
      0%,100% { opacity: 0.1; transform: scale(1); }
      50% { opacity: 0.8; transform: scale(1.4); }
    }

    /* ─── WRAPPER ─── */
    .readme-wrapper {
      position: relative; z-index: 1;
      max-width: 980px;
      margin: 0 auto;
      padding: 0 16px 60px;
    }

    /* ─── HERO BANNER ─── */
    .hero-banner {
      position: relative;
      width: 100%;
      border-radius: 0 0 32px 32px;
      overflow: hidden;
      margin-bottom: 0;
    }
    .hero-bg {
      background: linear-gradient(135deg,#0f0c29,#1a1a4e,#0f0c29,#1b0a2e,#0d1b47);
      background-size: 400% 400%;
      animation: gradShift 8s ease infinite;
      padding: 64px 32px 80px;
      text-align: center;
      position: relative;
    }
    @keyframes gradShift {
      0%{background-position:0% 50%} 50%{background-position:100% 50%} 100%{background-position:0% 50%}
    }
    .hero-orb {
      position: absolute; border-radius: 50%; filter: blur(80px); pointer-events: none;
    }
    .orb1 { width:340px;height:340px;background:rgba(88,166,255,.18);top:-80px;left:-80px; animation:orbFloat 7s ease-in-out infinite; }
    .orb2 { width:280px;height:280px;background:rgba(188,140,255,.18);bottom:-60px;right:-60px; animation:orbFloat 9s ease-in-out infinite reverse; }
    .orb3 { width:200px;height:200px;background:rgba(255,123,114,.12);top:50%;left:50%;transform:translate(-50%,-50%); animation:orbFloat 6s ease-in-out infinite 2s; }
    @keyframes orbFloat {
      0%,100%{transform:translate(0,0)} 33%{transform:translate(20px,-20px)} 66%{transform:translate(-15px,15px)}
    }
    .hero-badge {
      display: inline-flex; align-items: center; gap: 8px;
      background: rgba(255,255,255,.07); border: 1px solid rgba(255,255,255,.15);
      border-radius: 99px; padding: 6px 18px; font-size: 13px; color: #c9d1d9;
      margin-bottom: 28px; backdrop-filter: blur(8px);
      animation: fadeDown .8s ease both;
    }
    .badge-dot {
      width: 8px; height: 8px; border-radius: 50%;
      background: #3fb950;
      box-shadow: 0 0 8px #3fb950, 0 0 16px #3fb950;
      animation: pulse 2s infinite;
    }
    @keyframes pulse { 0%,100%{transform:scale(1);opacity:1} 50%{transform:scale(1.4);opacity:.7} }
    .hero-name {
      font-family: 'Space Grotesk', sans-serif;
      font-size: clamp(2.8rem, 8vw, 5.5rem);
      font-weight: 800;
      line-height: 1.05;
      background: linear-gradient(135deg,#58a6ff 0%,#bc8cff 35%,#ff7b72 65%,#ffa657 100%);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      background-clip: text;
      background-size: 200% 200%;
      animation: nameShimmer 4s ease-in-out infinite, fadeDown .9s ease .2s both;
      letter-spacing: -1px;
      text-shadow: none;
      filter: drop-shadow(0 0 40px rgba(88,166,255,.4));
    }
    @keyframes nameShimmer {
      0%{background-position:0% 50%} 50%{background-position:100% 50%} 100%{background-position:0% 50%}
    }
    .hero-role {
      font-size: clamp(.95rem,2.5vw,1.2rem);
      color: #8b949e;
      margin-top: 14px;
      animation: fadeDown 1s ease .4s both;
      letter-spacing: .3px;
    }
    .hero-role span { color: #58a6ff; font-weight: 600; }
    .hero-tagline {
      margin-top: 18px;
      font-size: clamp(1rem,2.5vw,1.15rem);
      color: #c9d1d9;
      font-style: italic;
      animation: fadeDown 1s ease .55s both;
    }
    .hero-tagline strong { color: #ffa657; font-style: normal; }

    /* Typing container */
    .typing-wrap {
      margin-top: 28px;
      font-family: 'Fira Code', monospace;
      font-size: clamp(.85rem,2vw,1.05rem);
      color: #3fb950;
      animation: fadeDown 1s ease .7s both;
      display: flex; align-items: center; justify-content: center; gap: 4px;
    }
    .typing-prefix { color: #bc8cff; }
    #typed-text { color: #58a6ff; }
    .cursor {
      display: inline-block; width: 2px; height: 1.1em;
      background: #58a6ff; margin-left: 2px;
      animation: blink .7s step-end infinite;
      vertical-align: middle;
    }
    @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

    .hero-buttons {
      margin-top: 36px;
      display: flex; flex-wrap: wrap; gap: 14px;
      justify-content: center;
      animation: fadeDown 1s ease .85s both;
    }
    .btn {
      display: inline-flex; align-items: center; gap: 8px;
      padding: 11px 26px; border-radius: 10px;
      font-size: .9rem; font-weight: 600;
      text-decoration: none; cursor: pointer;
      transition: all .3s ease;
      border: 1px solid transparent;
      position: relative; overflow: hidden;
    }
    .btn::after {
      content: ''; position: absolute; inset: 0;
      background: rgba(255,255,255,.06);
      opacity: 0; transition: opacity .3s;
    }
    .btn:hover::after { opacity: 1; }
    .btn:hover { transform: translateY(-3px); box-shadow: 0 12px 30px rgba(0,0,0,.4); }
    .btn-primary { background: linear-gradient(135deg,#1f6feb,#388bfd); color: #fff; }
    .btn-secondary { background: rgba(255,255,255,.07); border-color: rgba(255,255,255,.2); color: #e6edf3; }
    .btn-purple { background: linear-gradient(135deg,#6e40c9,#bc8cff); color: #fff; }
    .btn-green  { background: linear-gradient(135deg,#238636,#3fb950); color: #fff; }
    .btn-pink   { background: linear-gradient(135deg,#b91c1c,#ff7b72); color: #fff; }

    /* WAVE SVG */
    .wave-svg { display: block; margin-top: -1px; width: 100%; }

    @keyframes fadeDown { from{opacity:0;transform:translateY(-20px)} to{opacity:1;transform:translateY(0)} }
    @keyframes fadeUp   { from{opacity:0;transform:translateY(20px)}  to{opacity:1;transform:translateY(0)} }
    @keyframes fadeIn   { from{opacity:0} to{opacity:1} }

    /* ─── SECTION ─── */
    .section { margin-top: 56px; }
    .section-header {
      display: flex; align-items: center; gap: 14px;
      margin-bottom: 28px;
    }
    .section-icon {
      font-size: 1.6rem; line-height: 1;
      filter: drop-shadow(0 0 8px currentColor);
    }
    .section-title {
      font-family: 'Space Grotesk', sans-serif;
      font-size: clamp(1.3rem, 3vw, 1.7rem);
      font-weight: 700;
      background: linear-gradient(90deg, #e6edf3, #8b949e);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    .section-line {
      flex: 1; height: 1px;
      background: linear-gradient(90deg, var(--border), transparent);
    }

    /* GLOW DIVIDER */
    .glow-divider {
      height: 1px;
      background: linear-gradient(90deg,transparent,#58a6ff,#bc8cff,#ff7b72,transparent);
      margin: 56px 0;
      position: relative;
    }
    .glow-divider::after {
      content: '';
      position: absolute;
      inset: -3px 20%;
      background: inherit;
      filter: blur(8px);
      opacity: .5;
    }

    /* ─── GLASS CARD ─── */
    .glass-card {
      background: rgba(22,27,34,.75);
      border: 1px solid rgba(48,54,61,.9);
      border-radius: 18px;
      backdrop-filter: blur(12px);
      padding: 28px 32px;
      position: relative;
      overflow: hidden;
      transition: transform .3s ease, box-shadow .3s ease, border-color .3s;
    }
    .glass-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0; height: 2px;
      background: linear-gradient(90deg,#58a6ff,#bc8cff,#ff7b72);
      opacity: .7;
    }
    .glass-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 24px 48px rgba(0,0,0,.5);
      border-color: rgba(88,166,255,.3);
    }

    /* ─── ABOUT ─── */
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 24px;
    }
    @media(max-width:640px){ .about-grid{grid-template-columns:1fr;} }
    .about-item {
      display: flex; align-items: flex-start; gap: 14px;
      padding: 18px 20px;
      background: rgba(255,255,255,.03);
      border: 1px solid rgba(48,54,61,.8);
      border-radius: 14px;
      transition: all .3s;
    }
    .about-item:hover {
      border-color: rgba(88,166,255,.35);
      background: rgba(88,166,255,.05);
      transform: translateX(4px);
    }
    .about-icon { font-size: 1.5rem; flex-shrink: 0; margin-top: 2px; }
    .about-title { font-size: .9rem; font-weight: 700; color: #e6edf3; margin-bottom: 4px; }
    .about-desc  { font-size: .83rem; color: #8b949e; line-height: 1.55; }

    /* ─── WHAT I DO ─── */
    .do-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px,1fr));
      gap: 20px;
    }
    .do-card {
      background: rgba(22,27,34,.9);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 28px 20px;
      text-align: center;
      transition: all .35s ease;
      position: relative; overflow: hidden;
    }
    .do-card::before {
      content: '';
      position: absolute; inset: 0;
      background: var(--grad);
      opacity: 0;
      transition: opacity .35s;
      border-radius: inherit;
    }
    .do-card:hover::before { opacity: .08; }
    .do-card:hover {
      transform: translateY(-6px);
      border-color: var(--color);
      box-shadow: 0 0 30px -8px var(--color);
    }
    .do-card-emoji { font-size: 2.6rem; margin-bottom: 14px; display: block; filter: drop-shadow(0 0 12px var(--color)); }
    .do-card-title { font-weight: 700; font-size: 1rem; color: var(--color); margin-bottom: 8px; }
    .do-card-desc  { font-size: .82rem; color: #8b949e; line-height: 1.5; }

    /* ─── TECH BADGES ─── */
    .badge-section-title {
      font-size: .75rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      color: var(--muted);
      margin-bottom: 10px;
      display: flex; align-items: center; gap: 8px;
    }
    .badge-section-title::after { content:''; flex:1; height:1px; background: var(--border); }
    .badges-wrap { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 20px; }
    .tech-badge {
      display: inline-flex; align-items: center; gap: 6px;
      background: rgba(255,255,255,.05);
      border: 1px solid rgba(255,255,255,.1);
      border-radius: 8px;
      padding: 6px 14px;
      font-size: .8rem; font-weight: 600;
      color: var(--badge-color, #e6edf3);
      cursor: default;
      transition: all .25s;
      position: relative; overflow: hidden;
    }
    .tech-badge::before {
      content: '';
      position: absolute; left: 0; top: 0; bottom: 0;
      width: 3px;
      background: var(--badge-color, #58a6ff);
      border-radius: 0 0 0 0;
    }
    .tech-badge:hover {
      background: rgba(88,166,255,.1);
      border-color: var(--badge-color, #58a6ff);
      transform: scale(1.05);
      box-shadow: 0 4px 16px rgba(0,0,0,.3);
    }

    /* ─── PROJECT CARD ─── */
    .project-card {
      background: rgba(22,27,34,.95);
      border: 1px solid var(--border);
      border-radius: 20px;
      overflow: hidden;
      transition: all .35s ease;
      position: relative;
    }
    .project-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 30px 60px rgba(0,0,0,.5), 0 0 0 1px rgba(88,166,255,.2);
    }
    .project-banner {
      height: 200px;
      background: linear-gradient(135deg,#0f2027,#203a43,#2c5364);
      position: relative; overflow: hidden;
      display: flex; align-items: center; justify-content: center;
    }
    .project-banner-svg { position: absolute; inset: 0; width: 100%; height: 100%; }
    .project-banner-content { position: relative; z-index: 1; text-align: center; }
    .project-banner-icon { font-size: 4rem; filter: drop-shadow(0 0 20px rgba(88,166,255,.6)); }
    .project-banner-label {
      display: inline-block; margin-top: 10px;
      background: rgba(88,166,255,.2); border: 1px solid rgba(88,166,255,.4);
      border-radius: 99px; padding: 4px 16px;
      font-size: .75rem; font-weight: 700;
      color: #58a6ff; letter-spacing: 1px; text-transform: uppercase;
    }
    .project-body { padding: 28px 28px 24px; }
    .project-title { font-family: 'Space Grotesk',sans-serif; font-size: 1.4rem; font-weight: 700; color: #e6edf3; margin-bottom: 8px; }
    .project-desc  { font-size: .88rem; color: #8b949e; line-height: 1.65; margin-bottom: 18px; }
    .project-tags  { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 22px; }
    .project-tag {
      background: rgba(255,255,255,.05);
      border: 1px solid rgba(255,255,255,.1);
      border-radius: 6px; padding: 3px 10px;
      font-size: .75rem; font-family: 'Fira Code',monospace; color: #bc8cff;
    }
    .project-features { margin-bottom: 24px; }
    .project-feature {
      display: flex; align-items: center; gap: 10px;
      font-size: .85rem; color: #c9d1d9; padding: 6px 0;
      border-bottom: 1px solid rgba(48,54,61,.5);
    }
    .project-feature:last-child { border-bottom: none; }
    .feature-dot { width: 6px; height: 6px; border-radius: 50%; background: #3fb950; flex-shrink: 0; box-shadow: 0 0 6px #3fb950; }
    .project-btns { display: flex; flex-wrap: wrap; gap: 10px; }

    /* ─── STATS GRID ─── */
    .stats-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }
    @media(max-width:640px){ .stats-grid{grid-template-columns:1fr;} }
    .stat-card {
      background: rgba(22,27,34,.9);
      border: 1px solid var(--border);
      border-radius: 16px;
      overflow: hidden;
      transition: all .3s;
    }
    .stat-card:hover { border-color: rgba(88,166,255,.3); box-shadow: 0 16px 40px rgba(0,0,0,.4); }
    .stat-card img { width: 100%; height: auto; display: block; }
    .stat-card-full {
      grid-column: 1/-1;
    }

    /* ─── SNAKE ─── */
    .snake-section {
      text-align: center;
      padding: 32px 0;
    }
    .snake-section img { max-width: 100%; border-radius: 12px; }

    /* ─── ACHIEVEMENTS ─── */
    .ach-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(240px,1fr));
      gap: 18px;
    }
    .ach-card {
      background: rgba(22,27,34,.9);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 22px 20px;
      display: flex; gap: 16px; align-items: flex-start;
      transition: all .3s;
      position: relative; overflow: hidden;
    }
    .ach-card::before {
      content: '';
      position: absolute; top: 0; left: 0; right: 0; height: 2px;
      background: linear-gradient(90deg,var(--ach-c1,#58a6ff),var(--ach-c2,#bc8cff));
    }
    .ach-card:hover {
      transform: translateY(-4px);
      border-color: rgba(88,166,255,.3);
      box-shadow: 0 16px 36px rgba(0,0,0,.4);
    }
    .ach-icon { font-size: 2rem; flex-shrink: 0; }
    .ach-title { font-weight: 700; color: #e6edf3; font-size: .92rem; margin-bottom: 4px; }
    .ach-desc  { font-size: .8rem; color: #8b949e; line-height: 1.5; }
    .ach-badge {
      display: inline-block; margin-top: 8px;
      background: rgba(88,166,255,.15);
      border: 1px solid rgba(88,166,255,.3);
      border-radius: 99px; padding: 2px 10px;
      font-size: .7rem; font-weight: 700; color: #58a6ff; letter-spacing: .5px;
    }

    /* ─── GOALS ─── */
    .goals-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(210px,1fr));
      gap: 16px;
    }
    .goal-card {
      background: rgba(22,27,34,.9);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 20px 18px;
      transition: all .3s;
      position: relative;
    }
    .goal-card:hover {
      border-color: var(--g-color);
      box-shadow: 0 0 20px -5px var(--g-color);
      transform: translateY(-3px);
    }
    .goal-num {
      font-family: 'Fira Code',monospace;
      font-size: .7rem; color: var(--g-color);
      margin-bottom: 8px; font-weight: 700;
    }
    .goal-icon { font-size: 1.6rem; margin-bottom: 8px; }
    .goal-title { font-weight: 700; color: #e6edf3; font-size: .9rem; margin-bottom: 4px; }
    .goal-desc  { font-size: .8rem; color: #8b949e; line-height: 1.5; }
    .goal-progress {
      margin-top: 12px;
      height: 4px;
      background: rgba(255,255,255,.07);
      border-radius: 2px;
      overflow: hidden;
    }
    .goal-progress-fill {
      height: 100%;
      border-radius: 2px;
      background: linear-gradient(90deg, var(--g-color), var(--g-color2, var(--g-color)));
      animation: progressIn 1.5s ease both;
    }
    @keyframes progressIn { from{width:0} }

    /* ─── CONNECT ─── */
    .connect-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(180px,1fr));
      gap: 16px;
    }
    .connect-card {
      display: flex; flex-direction: column; align-items: center;
      gap: 12px; padding: 28px 20px;
      background: rgba(22,27,34,.9);
      border: 1px solid var(--border);
      border-radius: 16px;
      text-decoration: none;
      transition: all .35s ease;
      position: relative; overflow: hidden;
    }
    .connect-card::before {
      content: '';
      position: absolute; inset: 0;
      background: var(--c-grad);
      opacity: 0; transition: opacity .35s;
    }
    .connect-card:hover::before { opacity: .08; }
    .connect-card:hover {
      transform: translateY(-6px);
      border-color: var(--c-color);
      box-shadow: 0 0 30px -8px var(--c-color);
    }
    .connect-icon { font-size: 2.2rem; position: relative; z-index: 1; }
    .connect-platform { font-weight: 700; font-size: .9rem; color: var(--c-color); position: relative; z-index: 1; }
    .connect-handle { font-size: .78rem; color: #8b949e; position: relative; z-index: 1; font-family: 'Fira Code',monospace; }

    /* ─── FUN SECTION ─── */
    .fun-section {
      text-align: center;
      padding: 40px 32px;
      background: rgba(22,27,34,.8);
      border: 1px solid var(--border);
      border-radius: 20px;
      position: relative; overflow: hidden;
    }
    .fun-section::before {
      content: '';
      position: absolute; inset: 0;
      background: radial-gradient(ellipse at center, rgba(88,166,255,.06) 0%, transparent 70%);
    }
    .fun-emoji-row {
      font-size: 2rem; margin-bottom: 16px;
      animation: bounce 2s ease-in-out infinite;
    }
    @keyframes bounce { 0%,100%{transform:translateY(0)} 50%{transform:translateY(-8px)} }
    .fun-text {
      font-family: 'Space Grotesk',sans-serif;
      font-size: clamp(1.1rem,3vw,1.5rem);
      font-weight: 700;
      background: linear-gradient(135deg,#58a6ff,#bc8cff,#ff7b72);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      background-clip: text;
    }
    .fun-sub { margin-top: 10px; font-size: .88rem; color: #8b949e; }

    /* ─── QUOTE ─── */
    .quote-card {
      text-align: center;
      padding: 40px 32px;
      border-radius: 20px;
      background: linear-gradient(135deg,rgba(15,12,41,.9),rgba(26,26,78,.9));
      border: 1px solid rgba(88,166,255,.2);
      position: relative; overflow: hidden;
    }
    .quote-card::before {
      content: '"';
      position: absolute; top: -20px; left: 20px;
      font-size: 10rem; color: rgba(88,166,255,.06);
      font-family: Georgia,serif; line-height: 1;
      pointer-events: none;
    }
    .quote-text {
      font-family: 'Space Grotesk',sans-serif;
      font-size: clamp(1.3rem,4vw,2rem);
      font-weight: 800;
      letter-spacing: -0.5px;
      color: #e6edf3;
      position: relative; z-index: 1;
    }
    .quote-text span { color: #58a6ff; }
    .quote-author { margin-top: 14px; color: #8b949e; font-size: .85rem; font-style: italic; }

    /* ─── VISITOR ─── */
    .visitor-wrap {
      text-align: center;
      padding: 24px;
      border-radius: 16px;
      background: rgba(22,27,34,.9);
      border: 1px solid var(--border);
    }
    .visitor-label { font-size: .82rem; color: #8b949e; margin-bottom: 12px; letter-spacing: 1px; text-transform: uppercase; }
    .visitor-counter {
      display: inline-flex; gap: 6px; align-items: center; justify-content: center;
    }
    .v-digit {
      width: 44px; height: 56px;
      background: rgba(88,166,255,.1);
      border: 1px solid rgba(88,166,255,.3);
      border-radius: 8px;
      display: flex; align-items: center; justify-content: center;
      font-family: 'Fira Code',monospace;
      font-size: 1.6rem; font-weight: 700;
      color: #58a6ff;
      animation: flipIn .6s ease both;
    }
    @keyframes flipIn { from{transform:rotateX(90deg);opacity:0} to{transform:rotateX(0);opacity:1} }
    .v-sep { color: #30363d; font-size: 1.2rem; padding: 0 2px; }

    /* ─── FOOTER ─── */
    .footer-wave-top { display: block; width: 100%; margin-bottom: -2px; }
    .footer-body {
      background: linear-gradient(135deg,#0f0c29,#1a1a4e,#1b0a2e);
      background-size: 400% 400%;
      animation: gradShift 8s ease infinite;
      padding: 48px 32px 40px;
      text-align: center;
      border-radius: 24px;
      position: relative; overflow: hidden;
    }
    .footer-orb1 { position:absolute; width:200px;height:200px;background:rgba(88,166,255,.1);border-radius:50%;filter:blur(60px);top:-40px;left:-40px; }
    .footer-orb2 { position:absolute; width:180px;height:180px;background:rgba(188,140,255,.1);border-radius:50%;filter:blur(60px);bottom:-40px;right:-40px; }
    .footer-name {
      font-family: 'Space Grotesk',sans-serif;
      font-size: clamp(1.5rem,4vw,2.2rem);
      font-weight: 800;
      background: linear-gradient(135deg,#58a6ff,#bc8cff,#ff7b72);
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 8px; position: relative; z-index: 1;
    }
    .footer-sub { color: #8b949e; font-size: .88rem; margin-bottom: 20px; position: relative; z-index: 1; }
    .footer-links {
      display: flex; flex-wrap: wrap; gap: 12px;
      justify-content: center; margin-bottom: 28px;
      position: relative; z-index: 1;
    }
    .footer-link {
      color: #8b949e; font-size: .82rem;
      text-decoration: none;
      transition: color .2s;
    }
    .footer-link:hover { color: #58a6ff; }
    .footer-sep { color: #30363d; }
    .footer-bottom { color: #8b949e; font-size: .78rem; position: relative; z-index: 1; line-height: 1.7; }
    .footer-heart { color: #ff7b72; animation: heartbeat 1.2s ease-in-out infinite; display: inline-block; }
    @keyframes heartbeat { 0%,100%{transform:scale(1)} 50%{transform:scale(1.3)} }
    .footer-glow-line {
      height: 1px;
      background: linear-gradient(90deg,transparent,#58a6ff,#bc8cff,#ff7b72,transparent);
      margin: 20px 0;
      position: relative; z-index: 1;
    }

    /* ─── CODE BLOCK ─── */
    .code-block {
      background: #0d1117;
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 24px 28px;
      font-family: 'Fira Code',monospace;
      font-size: .85rem;
      line-height: 1.8;
      position: relative;
    }
    .code-block::before {
      content: '● ● ●';
      position: absolute; top: 14px; left: 20px;
      color: #30363d; font-size: .7rem; letter-spacing: 4px;
    }
    .code-block .cb-content { margin-top: 18px; }
    .cb-k  { color: #ff7b72; }
    .cb-s  { color: #a5d6ff; }
    .cb-v  { color: #3fb950; }
    .cb-c  { color: #8b949e; font-style: italic; }
    .cb-m  { color: #bc8cff; }
    .cb-p  { color: #e6edf3; }

    /* ─── SCROLL REVEAL ─── */
    .reveal { opacity: 0; transform: translateY(30px); transition: opacity .7s ease, transform .7s ease; }
    .revealed { opacity: 1; transform: translateY(0); }

    /* ─── TOOLTIP ─── */
    .tooltip-wrap { position: relative; display: inline-block; }
    .tooltip {
      position: absolute; bottom: calc(100% + 8px); left: 50%; transform: translateX(-50%);
      background: rgba(22,27,34,.95); border: 1px solid var(--border);
      border-radius: 8px; padding: 6px 12px;
      font-size: .75rem; color: #e6edf3; white-space: nowrap;
      pointer-events: none; opacity: 0;
      transition: opacity .2s; z-index: 100;
    }
    .tooltip-wrap:hover .tooltip { opacity: 1; }

    /* animated dots in hero */
    .floating-icons {
      position: absolute; inset: 0; pointer-events: none; overflow: hidden;
    }
    .float-icon {
      position: absolute;
      font-size: 1.2rem;
      opacity: .12;
      animation: floatUp var(--dur, 8s) linear infinite var(--delay, 0s);
    }
    @keyframes floatUp {
      0%   { transform: translateY(100%) rotate(0deg); opacity: .12; }
      100% { transform: translateY(-120%) rotate(360deg); opacity: 0; }
    }

    /* ─── RESPONSIVE ─── */
    @media(max-width:480px){
      .hero-bg { padding: 48px 20px 64px; }
      .glass-card { padding: 20px 18px; }
      .project-body { padding: 20px; }
      .about-item { padding: 14px; }
    }
  </style>
</head>
<body>

<!-- ░░░ STARS BACKGROUND ░░░ -->
<div id="particles-bg"></div>

<div class="readme-wrapper">

  <!-- ═══════════════════════════════════════════════
       1. HERO SECTION
  ═══════════════════════════════════════════════ -->
  <div class="hero-banner">
    <div class="hero-bg">
      <!-- orbs -->
      <div class="hero-orb orb1"></div>
      <div class="hero-orb orb2"></div>
      <div class="hero-orb orb3"></div>

      <!-- floating code icons -->
      <div class="floating-icons" id="floatingIcons"></div>

      <!-- badge -->
      <div class="hero-badge">
        <div class="badge-dot"></div>
        <span>Available for Internships & Collaborations</span>
      </div>

      <!-- name -->
      <h1 class="hero-name">GEETA MEHRA</h1>

      <!-- role -->
      <p class="hero-role">
        <span>☁️ Cloud &amp; DevOps Enthusiast</span> &nbsp;|&nbsp;
        <span>🎓 MCA @ Graphic Era Hill University</span> &nbsp;|&nbsp;
        <span>📍 Haldwani, Uttarakhand</span>
      </p>

      <!-- tagline -->
      <p class="hero-tagline">
        <strong>"Designing scalable cloud systems &amp; automating the future ☁️⚙️"</strong>
      </p>

      <!-- typing -->
      <div class="typing-wrap">
        <span class="typing-prefix">$ </span>
        <span id="typed-text"></span>
        <span class="cursor"></span>
      </div>

      <!-- buttons -->
      <div class="hero-buttons">
        <a href="https://github.com/techgeeta" target="_blank" class="btn btn-primary">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
          GitHub
        </a>
        <a href="https://www.linkedin.com/in/geeta-mehra-b9261a2b7/" target="_blank" class="btn btn-purple">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          LinkedIn
        </a>
        <a href="mailto:techgeeta@example.com" class="btn btn-green">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,12 2,6"/></svg>
          Email Me
        </a>
        <a href="#projects" class="btn btn-secondary">
          🚀 View Projects
        </a>
      </div>
    </div>

    <!-- WAVE BOTTOM -->
    <svg class="wave-svg" viewBox="0 0 1440 80" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
      <defs>
        <linearGradient id="waveGrad" x1="0" y1="0" x2="1" y2="0">
          <stop offset="0%"   stop-color="#58a6ff" stop-opacity=".6"/>
          <stop offset="50%"  stop-color="#bc8cff" stop-opacity=".6"/>
          <stop offset="100%" stop-color="#ff7b72" stop-opacity=".6"/>
        </linearGradient>
      </defs>
      <path fill="url(#waveGrad)" opacity=".3"
        d="M0,40 C200,0 400,80 600,40 C800,0 1000,80 1200,40 C1300,20 1370,50 1440,40 L1440,80 L0,80 Z"/>
      <path fill="#0d1117"
        d="M0,60 C240,20 480,80 720,55 C960,30 1200,75 1440,55 L1440,80 L0,80 Z"/>
    </svg>
  </div>

  <!-- ─── Profile image pill ─── -->
  <div style="display:flex;justify-content:center;margin-top:32px;" class="reveal">
    <div style="display:flex;align-items:center;gap:16px;background:rgba(22,27,34,.9);border:1px solid #30363d;border-radius:99px;padding:10px 24px 10px 10px;">
      <div style="width:52px;height:52px;border-radius:50%;background:linear-gradient(135deg,#58a6ff,#bc8cff);display:flex;align-items:center;justify-content:center;font-size:1.6rem;flex-shrink:0;">👩‍💻</div>
      <div>
        <div style="font-weight:700;font-size:.95rem;color:#e6edf3;">Geeta Mehra</div>
        <div style="font-size:.78rem;color:#8b949e;font-family:'Fira Code',monospace;">@techgeeta</div>
      </div>
      <div style="width:1px;height:36px;background:#30363d;margin:0 6px;"></div>
      <div style="font-size:.78rem;color:#8b949e;">📍 Haldwani, India</div>
    </div>
  </div>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       2. ABOUT ME
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="about">
    <div class="section-header">
      <span class="section-icon">👩‍💻</span>
      <h2 class="section-title">About Me</h2>
      <div class="section-line"></div>
    </div>

    <div class="glass-card" style="margin-bottom:24px;">
      <div style="display:flex;gap:20px;align-items:flex-start;flex-wrap:wrap;">
        <div style="flex:1;min-width:240px;">
          <div style="font-family:'Fira Code',monospace;color:#bc8cff;font-size:.78rem;margin-bottom:10px;">// about_me.json</div>
          <div class="code-block">
            <div class="cb-content">
              <div><span class="cb-k">const</span> <span class="cb-m">geeta</span> <span class="cb-p">= {</span></div>
              <div>&nbsp;&nbsp;<span class="cb-s">"name"</span><span class="cb-p">:</span> <span class="cb-v">"Geeta Mehra"</span><span class="cb-p">,</span></div>
              <div>&nbsp;&nbsp;<span class="cb-s">"role"</span><span class="cb-p">:</span> <span class="cb-v">"Cloud & DevOps Enthusiast"</span><span class="cb-p">,</span></div>
              <div>&nbsp;&nbsp;<span class="cb-s">"education"</span><span class="cb-p">:</span> <span class="cb-v">"MCA @ GEHU"</span><span class="cb-p">,</span></div>
              <div>&nbsp;&nbsp;<span class="cb-s">"location"</span><span class="cb-p">:</span> <span class="cb-v">"Haldwani, India 🇮🇳"</span><span class="cb-p">,</span></div>
              <div>&nbsp;&nbsp;<span class="cb-s">"passion"</span><span class="cb-p">: [</span></div>
              <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="cb-v">"Cloud Computing"</span><span class="cb-p">,</span></div>
              <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="cb-v">"DevOps & CI/CD"</span><span class="cb-p">,</span></div>
              <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="cb-v">"AI Integration"</span><span class="cb-p">,</span></div>
              <div>&nbsp;&nbsp;&nbsp;&nbsp;<span class="cb-v">"Open Source"</span></div>
              <div>&nbsp;&nbsp;<span class="cb-p">],</span></div>
              <div>&nbsp;&nbsp;<span class="cb-s">"status"</span><span class="cb-p">:</span> <span class="cb-v">"Always Learning 🚀"</span></div>
              <div><span class="cb-p">};</span></div>
            </div>
          </div>
        </div>
        <div style="flex:1;min-width:240px;display:flex;flex-direction:column;gap:12px;justify-content:center;">
          <div style="background:rgba(88,166,255,.07);border:1px solid rgba(88,166,255,.2);border-radius:12px;padding:14px 16px;">
            <div style="font-size:.82rem;color:#8b949e;margin-bottom:4px;">🎓 Education</div>
            <div style="font-weight:600;color:#e6edf3;font-size:.9rem;">Master of Computer Applications</div>
            <div style="font-size:.78rem;color:#58a6ff;">Graphic Era Hill University, Haldwani</div>
          </div>
          <div style="background:rgba(63,185,80,.07);border:1px solid rgba(63,185,80,.2);border-radius:12px;padding:14px 16px;">
            <div style="font-size:.82rem;color:#8b949e;margin-bottom:4px;">💡 Focus Areas</div>
            <div style="display:flex;flex-wrap:wrap;gap:6px;margin-top:6px;">
              <span style="background:rgba(63,185,80,.1);border:1px solid rgba(63,185,80,.25);border-radius:6px;padding:2px 8px;font-size:.72rem;color:#3fb950;">AWS</span>
              <span style="background:rgba(63,185,80,.1);border:1px solid rgba(63,185,80,.25);border-radius:6px;padding:2px 8px;font-size:.72rem;color:#3fb950;">CI/CD</span>
              <span style="background:rgba(63,185,80,.1);border:1px solid rgba(63,185,80,.25);border-radius:6px;padding:2px 8px;font-size:.72rem;color:#3fb950;">DevOps</span>
              <span style="background:rgba(63,185,80,.1);border:1px solid rgba(63,185,80,.25);border-radius:6px;padding:2px 8px;font-size:.72rem;color:#3fb950;">AI/ML</span>
              <span style="background:rgba(63,185,80,.1);border:1px solid rgba(63,185,80,.25);border-radius:6px;padding:2px 8px;font-size:.72rem;color:#3fb950;">Automation</span>
            </div>
          </div>
          <div style="background:rgba(188,140,255,.07);border:1px solid rgba(188,140,255,.2);border-radius:12px;padding:14px 16px;">
            <div style="font-size:.82rem;color:#8b949e;margin-bottom:4px;">⚡ Superpower</div>
            <div style="font-size:.85rem;color:#bc8cff;font-weight:600;">Fast Learner · Problem Solver · Team Player</div>
          </div>
        </div>
      </div>
    </div>

    <div class="about-grid">
      <div class="about-item">
        <span class="about-icon">🎯</span>
        <div>
          <div class="about-title">Passionate About Cloud</div>
          <div class="about-desc">Exploring AWS, Azure and cloud-native architectures to build scalable, resilient systems.</div>
        </div>
      </div>
      <div class="about-item">
        <span class="about-icon">⚙️</span>
        <div>
          <div class="about-title">DevOps & CI/CD</div>
          <div class="about-desc">Building automated pipelines with Jenkins, GitHub Actions & containerized deployments.</div>
        </div>
      </div>
      <div class="about-item">
        <span class="about-icon">🤖</span>
        <div>
          <div class="about-title">AI Integration</div>
          <div class="about-desc">Integrating AI/ML into real-world apps using Python, scikit-learn, Pandas & NumPy.</div>
        </div>
      </div>
      <div class="about-item">
        <span class="about-icon">🌱</span>
        <div>
          <div class="about-title">Always Learning</div>
          <div class="about-desc">Constantly upgrading skills through certifications, projects & open-source contributions.</div>
        </div>
      </div>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       3. WHAT I DO
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="what-i-do">
    <div class="section-header">
      <span class="section-icon">🚀</span>
      <h2 class="section-title">What I Do</h2>
      <div class="section-line"></div>
    </div>

    <div class="do-grid">
      <div class="do-card" style="--color:#58a6ff;--grad:linear-gradient(135deg,#58a6ff,#1f6feb);">
        <span class="do-card-emoji">☁️</span>
        <div class="do-card-title">Cloud Computing</div>
        <div class="do-card-desc">Designing and deploying cloud-native solutions on AWS & Azure with scalability in mind.</div>
        <div style="margin-top:16px;display:flex;flex-wrap:wrap;gap:4px;justify-content:center;">
          <span style="background:rgba(88,166,255,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#58a6ff;">EC2</span>
          <span style="background:rgba(88,166,255,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#58a6ff;">S3</span>
          <span style="background:rgba(88,166,255,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#58a6ff;">Lambda</span>
          <span style="background:rgba(88,166,255,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#58a6ff;">VPC</span>
        </div>
      </div>
      <div class="do-card" style="--color:#ff7b72;--grad:linear-gradient(135deg,#ff7b72,#b91c1c);">
        <span class="do-card-emoji">⚙️</span>
        <div class="do-card-title">DevOps</div>
        <div class="do-card-desc">Building CI/CD pipelines, automating deployments and managing infrastructure as code.</div>
        <div style="margin-top:16px;display:flex;flex-wrap:wrap;gap:4px;justify-content:center;">
          <span style="background:rgba(255,123,114,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#ff7b72;">Jenkins</span>
          <span style="background:rgba(255,123,114,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#ff7b72;">Docker</span>
          <span style="background:rgba(255,123,114,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#ff7b72;">GitHub Actions</span>
        </div>
      </div>
      <div class="do-card" style="--color:#ffa657;--grad:linear-gradient(135deg,#ffa657,#b45309);">
        <span class="do-card-emoji">🤖</span>
        <div class="do-card-title">Automation</div>
        <div class="do-card-desc">Scripting and automating repetitive tasks, testing workflows and deployment processes.</div>
        <div style="margin-top:16px;display:flex;flex-wrap:wrap;gap:4px;justify-content:center;">
          <span style="background:rgba(255,166,87,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#ffa657;">Python</span>
          <span style="background:rgba(255,166,87,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#ffa657;">Bash</span>
          <span style="background:rgba(255,166,87,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#ffa657;">YAML</span>
        </div>
      </div>
      <div class="do-card" style="--color:#bc8cff;--grad:linear-gradient(135deg,#bc8cff,#6e40c9);">
        <span class="do-card-emoji">🧠</span>
        <div class="do-card-title">AI Integration</div>
        <div class="do-card-desc">Embedding machine learning models into full-stack apps for intelligent, data-driven features.</div>
        <div style="margin-top:16px;display:flex;flex-wrap:wrap;gap:4px;justify-content:center;">
          <span style="background:rgba(188,140,255,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#bc8cff;">scikit-learn</span>
          <span style="background:rgba(188,140,255,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#bc8cff;">Pandas</span>
          <span style="background:rgba(188,140,255,.12);border-radius:4px;padding:2px 7px;font-size:.68rem;color:#bc8cff;">NumPy</span>
        </div>
      </div>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       4. TECH STACK
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="tech">
    <div class="section-header">
      <span class="section-icon">🛠</span>
      <h2 class="section-title">Tech Stack</h2>
      <div class="section-line"></div>
    </div>

    <div class="glass-card">
      <!-- Languages -->
      <div class="badge-section-title">💻 Languages</div>
      <div class="badges-wrap">
        <span class="tech-badge" style="--badge-color:#00599C;">🔵 C</span>
        <span class="tech-badge" style="--badge-color:#004482;">🔷 C++</span>
        <span class="tech-badge" style="--badge-color:#ED8B00;">☕ Java</span>
        <span class="tech-badge" style="--badge-color:#E34F26;">🌐 HTML5</span>
        <span class="tech-badge" style="--badge-color:#F7DF1E;">✨ JavaScript</span>
      </div>

      <!-- Cloud -->
      <div class="badge-section-title">☁️ Cloud Platforms</div>
      <div class="badges-wrap">
        <span class="tech-badge" style="--badge-color:#FF9900;">🟠 AWS</span>
        <span class="tech-badge" style="--badge-color:#0078D4;">🔵 Microsoft Azure</span>
        <span class="tech-badge" style="--badge-color:#F38020;">🟡 Cloudflare</span>
      </div>

      <!-- DevOps -->
      <div class="badge-section-title">⚙️ DevOps & CI/CD</div>
      <div class="badges-wrap">
        <span class="tech-badge" style="--badge-color:#D24939;">🔴 Jenkins</span>
        <span class="tech-badge" style="--badge-color:#D22128;">🪶 Apache</span>
        <span class="tech-badge" style="--badge-color:#f0f0f0;">🐙 GitHub</span>
        <span class="tech-badge" style="--badge-color:#FC6D26;">🦊 GitLab</span>
        <span class="tech-badge" style="--badge-color:#2496ED;">🐳 Docker</span>
      </div>

      <!-- Tools -->
      <div class="badge-section-title">🔧 Tools & Design</div>
      <div class="badges-wrap">
        <span class="tech-badge" style="--badge-color:#00C4CC;">🎨 Canva</span>
        <span class="tech-badge" style="--badge-color:#FF6B35;">📐 Proto.io</span>
        <span class="tech-badge" style="--badge-color:#1BA0D7;">🌐 Cisco</span>
        <span class="tech-badge" style="--badge-color:#0A66C2;">🔗 Linux</span>
      </div>

      <!-- AI/Data -->
      <div class="badge-section-title">🧠 Data / AI / ML</div>
      <div class="badges-wrap">
        <span class="tech-badge" style="--badge-color:#3776AB;">🐍 Python</span>
        <span class="tech-badge" style="--badge-color:#150458;">🐼 Pandas</span>
        <span class="tech-badge" style="--badge-color:#013243;">🔢 NumPy</span>
        <span class="tech-badge" style="--badge-color:#F7931E;">⚙️ Scikit-learn</span>
      </div>
    </div>

    <!-- Skill bars -->
    <div style="margin-top:24px;display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:16px;">
      <div class="glass-card" style="padding:20px;">
        <div style="font-size:.82rem;color:#8b949e;margin-bottom:12px;">Skill Proficiency</div>
        <div id="skillBars"></div>
      </div>
      <div class="glass-card" style="padding:20px;">
        <div style="font-size:.82rem;color:#8b949e;margin-bottom:16px;">Tech Radar</div>
        <canvas id="radarChart" width="220" height="220" style="display:block;margin:0 auto;"></canvas>
      </div>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       5. FEATURED PROJECT
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="projects">
    <div class="section-header">
      <span class="section-icon">💼</span>
      <h2 class="section-title">Featured Project</h2>
      <div class="section-line"></div>
    </div>

    <div class="project-card">
      <!-- Banner -->
      <div class="project-banner">
        <svg class="project-banner-svg" viewBox="0 0 900 200" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="pbg" x1="0" y1="0" x2="1" y2="1">
              <stop offset="0%" stop-color="#0f2027"/>
              <stop offset="50%" stop-color="#203a43"/>
              <stop offset="100%" stop-color="#2c5364"/>
            </linearGradient>
          </defs>
          <rect width="900" height="200" fill="url(#pbg)"/>
          <!-- grid lines -->
          <g stroke="rgba(88,166,255,.08)" stroke-width="1">
            <line x1="0" y1="40" x2="900" y2="40"/>
            <line x1="0" y1="80" x2="900" y2="80"/>
            <line x1="0" y1="120" x2="900" y2="120"/>
            <line x1="0" y1="160" x2="900" y2="160"/>
            <line x1="150" y1="0" x2="150" y2="200"/>
            <line x1="300" y1="0" x2="300" y2="200"/>
            <line x1="450" y1="0" x2="450" y2="200"/>
            <line x1="600" y1="0" x2="600" y2="200"/>
            <line x1="750" y1="0" x2="750" y2="200"/>
          </g>
          <!-- floating circles -->
          <circle cx="80"  cy="40"  r="50" fill="rgba(88,166,255,.05)"/>
          <circle cx="820" cy="160" r="70" fill="rgba(188,140,255,.05)"/>
          <circle cx="450" cy="100" r="90" fill="rgba(63,185,80,.04)"/>
          <!-- stars -->
          <circle cx="100" cy="80"  r="1.5" fill="rgba(255,255,255,.5)"/>
          <circle cx="250" cy="30"  r="1"   fill="rgba(255,255,255,.4)"/>
          <circle cx="600" cy="150" r="1.5" fill="rgba(255,255,255,.5)"/>
          <circle cx="780" cy="60"  r="1"   fill="rgba(255,255,255,.4)"/>
          <circle cx="350" cy="170" r="1.5" fill="rgba(255,255,255,.5)"/>
        </svg>
        <div class="project-banner-content">
          <div class="project-banner-icon">🏡</div>
          <div class="project-banner-label">⭐ Featured Project</div>
        </div>
      </div>

      <div class="project-body">
        <div style="display:flex;align-items:flex-start;justify-content:space-between;flex-wrap:wrap;gap:12px;margin-bottom:14px;">
          <div>
            <h3 class="project-title">🌟 GramStay AI Booking Platform</h3>
            <div style="font-size:.78rem;color:#8b949e;font-family:'Fira Code',monospace;">Full-Stack · AI-Powered · Rural Tourism</div>
          </div>
          <div style="display:flex;gap:8px;">
            <span style="background:rgba(63,185,80,.1);border:1px solid rgba(63,185,80,.25);border-radius:99px;padding:4px 12px;font-size:.72rem;color:#3fb950;font-weight:700;">🟢 Active</span>
          </div>
        </div>

        <p class="project-desc">
          A full-stack AI-powered booking platform for village homestays in the Jim Corbett region of Uttarakhand.
          Connects urban travelers with authentic rural experiences using intelligent recommendations, real-time availability,
          and seamless booking workflows. Built with modern tech to support sustainable rural tourism.
        </p>

        <div class="project-tags">
          <span class="project-tag">React.js</span>
          <span class="project-tag">Node.js</span>
          <span class="project-tag">MongoDB</span>
          <span class="project-tag">Express</span>
          <span class="project-tag">AI/ML</span>
          <span class="project-tag">AWS S3</span>
          <span class="project-tag">Python</span>
          <span class="project-tag">REST API</span>
        </div>

        <div class="project-features">
          <div class="project-feature"><span class="feature-dot"></span>🤖 AI-powered personalized homestay recommendations</div>
          <div class="project-feature"><span class="feature-dot"></span>🏠 Curated village homestay listings in Jim Corbett region</div>
          <div class="project-feature"><span class="feature-dot"></span>📅 Real-time availability calendar & instant booking</div>
          <div class="project-feature"><span class="feature-dot"></span>💳 Secure payment integration & booking management</div>
          <div class="project-feature"><span class="feature-dot"></span>📱 Fully responsive across all devices</div>
          <div class="project-feature"><span class="feature-dot"></span>🌿 Supports sustainable rural tourism in Uttarakhand</div>
        </div>

        <div class="project-btns">
          <a href="https://github.com/techgeeta" target="_blank" class="btn btn-secondary" style="font-size:.82rem;padding:9px 18px;">
            <svg width="14" height="14" viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
            💻 GitHub Repo
          </a>
          <a href="https://github.com/techgeeta" target="_blank" class="btn btn-primary" style="font-size:.82rem;padding:9px 18px;">
            🔗 View Project
          </a>
          <a href="#" class="btn btn-green" style="font-size:.82rem;padding:9px 18px;">
            🌐 Live Demo
          </a>
        </div>
      </div>
    </div>

    <!-- More projects hint -->
    <div style="margin-top:18px;text-align:center;">
      <a href="https://github.com/techgeeta?tab=repositories" target="_blank" style="display:inline-flex;align-items:center;gap:8px;color:#8b949e;font-size:.85rem;text-decoration:none;padding:10px 20px;border:1px solid #30363d;border-radius:10px;transition:all .3s;" onmouseover="this.style.color='#58a6ff';this.style.borderColor='rgba(88,166,255,.4)'" onmouseout="this.style.color='#8b949e';this.style.borderColor='#30363d'">
        🔍 Explore All Repositories on GitHub →
      </a>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       6. GITHUB ANALYTICS
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="analytics">
    <div class="section-header">
      <span class="section-icon">📊</span>
      <h2 class="section-title">GitHub Analytics</h2>
      <div class="section-line"></div>
    </div>

    <div class="stats-grid">
      <div class="stat-card">
        <img
          src="https://github-readme-stats.vercel.app/api?username=techgeeta&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=bc8cff&text_color=c9d1d9&border_radius=16"
          alt="GitHub Stats"
          loading="lazy"
        />
      </div>
      <div class="stat-card">
        <img
          src="https://github-readme-stats.vercel.app/api/top-langs/?username=techgeeta&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9&border_radius=16&langs_count=8"
          alt="Top Languages"
          loading="lazy"
        />
      </div>
      <div class="stat-card stat-card-full">
        <img
          src="https://github-readme-streak-stats.herokuapp.com/?user=techgeeta&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=30363d&ring=58a6ff&fire=ff7b72&currStreakNum=e6edf3&sideNums=e6edf3&currStreakLabel=bc8cff&sideLabels=8b949e&dates=8b949e&border_radius=16"
          alt="Streak Stats"
          loading="lazy"
          style="width:100%;"
        />
      </div>
      <div class="stat-card stat-card-full">
        <img
          src="https://github-readme-activity-graph.vercel.app/graph?username=techgeeta&bg_color=0d1117&color=58a6ff&line=bc8cff&point=ff7b72&area=true&hide_border=true&area_color=58a6ff"
          alt="Contribution Graph"
          loading="lazy"
          style="width:100%;"
        />
      </div>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       7. SNAKE ANIMATION
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="snake">
    <div class="section-header">
      <span class="section-icon">🐍</span>
      <h2 class="section-title">Contribution Snake</h2>
      <div class="section-line"></div>
    </div>

    <div class="glass-card" style="padding:24px;text-align:center;">
      <p style="font-size:.82rem;color:#8b949e;margin-bottom:20px;font-family:'Fira Code',monospace;">// Watch the snake eat my contributions! 🐍</p>
      <img
        src="https://raw.githubusercontent.com/techgeeta/techgeeta/output/github-contribution-grid-snake-dark.svg"
        alt="Snake Animation"
        style="max-width:100%;border-radius:12px;"
        onerror="this.src='https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg'"
      />
      <p style="margin-top:16px;font-size:.78rem;color:#8b949e;">🟢 Each square = a day of coding · 🐍 Snake eats contributions</p>
    </div>

    <!-- Animated snake alternative -->
    <div style="margin-top:20px;overflow:hidden;border-radius:16px;border:1px solid #30363d;background:#0d1117;padding:20px;">
      <canvas id="snakeCanvas" width="100%" height="120" style="width:100%;display:block;"></canvas>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       8. ACHIEVEMENTS
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="achievements">
    <div class="section-header">
      <span class="section-icon">🏆</span>
      <h2 class="section-title">Achievements & Certifications</h2>
      <div class="section-line"></div>
    </div>

    <div class="ach-grid">
      <div class="ach-card" style="--ach-c1:#58a6ff;--ach-c2:#bc8cff;">
        <span class="ach-icon">🏅</span>
        <div>
          <div class="ach-title">Deloitte Technology Job Simulation</div>
          <div class="ach-desc">Completed a real-world tech simulation covering software engineering & data analysis workflows used at Deloitte.</div>
          <span class="ach-badge">✅ Completed</span>
        </div>
      </div>
      <div class="ach-card" style="--ach-c1:#ff9900;--ach-c2:#ffa657;">
        <span class="ach-icon">☁️</span>
        <div>
          <div class="ach-title">AWS Cloud Foundations</div>
          <div class="ach-desc">Learning core AWS services including EC2, S3, Lambda, IAM and cloud architecture principles.</div>
          <span class="ach-badge" style="color:#ffa657;border-color:rgba(255,166,87,.3);background:rgba(255,166,87,.1);">🔄 In Progress</span>
        </div>
      </div>
      <div class="ach-card" style="--ach-c1:#d24939;--ach-c2:#ff7b72;">
        <span class="ach-icon">⚙️</span>
        <div>
          <div class="ach-title">DevOps Tools Mastery</div>
          <div class="ach-desc">Hands-on experience with Jenkins, Docker, Apache and Git-based CI/CD workflows and automation.</div>
          <span class="ach-badge" style="color:#ff7b72;border-color:rgba(255,123,114,.3);background:rgba(255,123,114,.1);">🔄 In Progress</span>
        </div>
      </div>
      <div class="ach-card" style="--ach-c1:#3fb950;--ach-c2:#39d353;">
        <span class="ach-icon">🎓</span>
        <div>
          <div class="ach-title">MCA — Graphic Era Hill University</div>
          <div class="ach-desc">Pursuing Master of Computer Applications with focus on cloud computing, software engineering & AI.</div>
          <span class="ach-badge" style="color:#3fb950;border-color:rgba(63,185,80,.3);background:rgba(63,185,80,.1);">📚 Ongoing</span>
        </div>
      </div>
      <div class="ach-card" style="--ach-c1:#bc8cff;--ach-c2:#8957e5;">
        <span class="ach-icon">🐍</span>
        <div>
          <div class="ach-title">Python for Data Science</div>
          <div class="ach-desc">Working with Pandas, NumPy and scikit-learn for data analysis, ML models and AI integrations.</div>
          <span class="ach-badge" style="color:#bc8cff;border-color:rgba(188,140,255,.3);background:rgba(188,140,255,.1);">✅ Completed</span>
        </div>
      </div>
      <div class="ach-card" style="--ach-c1:#ffa657;--ach-c2:#f0883e;">
        <span class="ach-icon">🌐</span>
        <div>
          <div class="ach-title">Open Source Contributor</div>
          <div class="ach-desc">Actively contributing to open-source projects and building personal projects on GitHub to grow as a developer.</div>
          <span class="ach-badge" style="color:#ffa657;border-color:rgba(255,166,87,.3);background:rgba(255,166,87,.1);">🌱 Growing</span>
        </div>
      </div>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       9. CURRENT GOALS
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="goals">
    <div class="section-header">
      <span class="section-icon">🎯</span>
      <h2 class="section-title">Current Goals</h2>
      <div class="section-line"></div>
    </div>

    <div class="goals-grid">
      <div class="goal-card" style="--g-color:#58a6ff;--g-color2:#bc8cff;">
        <div class="goal-num">01 /</div>
        <div class="goal-icon">⚙️</div>
        <div class="goal-title">Master DevOps Tools</div>
        <div class="goal-desc">Deep-dive into Kubernetes, Terraform, Ansible and advanced CI/CD patterns.</div>
        <div class="goal-progress"><div class="goal-progress-fill" style="width:65%;"></div></div>
      </div>
      <div class="goal-card" style="--g-color:#3fb950;--g-color2:#39d353;">
        <div class="goal-num">02 /</div>
        <div class="goal-icon">🏗️</div>
        <div class="goal-title">Production-Ready Systems</div>
        <div class="goal-desc">Build and deploy scalable, highly-available cloud systems with real users.</div>
        <div class="goal-progress"><div class="goal-progress-fill" style="width:50%;"></div></div>
      </div>
      <div class="goal-card" style="--g-color:#bc8cff;--g-color2:#8957e5;">
        <div class="goal-num">03 /</div>
        <div class="goal-icon">🌍</div>
        <div class="goal-title">Open Source Contributions</div>
        <div class="goal-desc">Contribute meaningfully to popular open-source DevOps and cloud tools.</div>
        <div class="goal-progress"><div class="goal-progress-fill" style="width:30%;"></div></div>
      </div>
      <div class="goal-card" style="--g-color:#ffa657;--g-color2:#f0883e;">
        <div class="goal-num">04 /</div>
        <div class="goal-icon">💼</div>
        <div class="goal-title">Secure Top Tech Job</div>
        <div class="goal-desc">Land a cloud/DevOps role at a leading technology company post-graduation.</div>
        <div class="goal-progress"><div class="goal-progress-fill" style="width:40%;"></div></div>
      </div>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       10. CONNECT
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="connect">
    <div class="section-header">
      <span class="section-icon">🌐</span>
      <h2 class="section-title">Connect With Me</h2>
      <div class="section-line"></div>
    </div>

    <div class="connect-grid">
      <a href="https://www.linkedin.com/in/geeta-mehra-b9261a2b7/" target="_blank" class="connect-card"
         style="--c-color:#0A66C2;--c-grad:linear-gradient(135deg,#0A66C2,#0077b5);">
        <span class="connect-icon">💼</span>
        <div class="connect-platform">LinkedIn</div>
        <div class="connect-handle">@geeta-mehra-b9261a2b7</div>
        <span style="font-size:.72rem;color:#8b949e;margin-top:4px;">Let's network!</span>
      </a>
      <a href="https://github.com/techgeeta" target="_blank" class="connect-card"
         style="--c-color:#e6edf3;--c-grad:linear-gradient(135deg,#24292f,#161b22);">
        <span class="connect-icon">🐙</span>
        <div class="connect-platform" style="color:#e6edf3;">GitHub</div>
        <div class="connect-handle">@techgeeta</div>
        <span style="font-size:.72rem;color:#8b949e;margin-top:4px;">Star my repos!</span>
      </a>
      <a href="mailto:techgeeta@example.com" class="connect-card"
         style="--c-color:#ff7b72;--c-grad:linear-gradient(135deg,#ff7b72,#b91c1c);">
        <span class="connect-icon">📧</span>
        <div class="connect-platform" style="color:#ff7b72;">Email</div>
        <div class="connect-handle">techgeeta@mail.com</div>
        <span style="font-size:.72rem;color:#8b949e;margin-top:4px;">Say hello!</span>
      </a>
      <a href="https://github.com/techgeeta" target="_blank" class="connect-card"
         style="--c-color:#3fb950;--c-grad:linear-gradient(135deg,#238636,#3fb950);">
        <span class="connect-icon">📍</span>
        <div class="connect-platform" style="color:#3fb950;">Location</div>
        <div class="connect-handle">Haldwani, Uttarakhand</div>
        <span style="font-size:.72rem;color:#8b949e;margin-top:4px;">🇮🇳 India</span>
      </a>
    </div>

    <!-- Availability banner -->
    <div style="margin-top:20px;display:flex;align-items:center;gap:16px;background:rgba(63,185,80,.07);border:1px solid rgba(63,185,80,.2);border-radius:14px;padding:18px 24px;flex-wrap:wrap;">
      <div style="display:flex;align-items:center;gap:10px;flex:1;min-width:200px;">
        <div style="width:12px;height:12px;border-radius:50%;background:#3fb950;box-shadow:0 0 10px #3fb950;animation:pulse 2s infinite;flex-shrink:0;"></div>
        <div>
          <div style="font-weight:700;color:#e6edf3;font-size:.9rem;">Open to Opportunities</div>
          <div style="font-size:.78rem;color:#8b949e;">Internships · Part-time · Freelance · Collaborations</div>
        </div>
      </div>
      <a href="mailto:techgeeta@example.com" class="btn btn-green" style="font-size:.82rem;padding:9px 20px;flex-shrink:0;">
        ✉️ Get In Touch
      </a>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       11. FUN SECTION
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="fun">
    <div class="fun-section">
      <div class="fun-emoji-row">☁️ ⚙️ 🚀 🤖 ✨ 🐍 💡</div>
      <div class="fun-text">I turn ideas into cloud-powered solutions ☁️✨</div>
      <div class="fun-sub">Bridging the gap between imagination and infrastructure, one deploy at a time.</div>

      <div style="margin-top:28px;display:flex;flex-wrap:wrap;gap:16px;justify-content:center;">
        <div style="background:rgba(88,166,255,.08);border:1px solid rgba(88,166,255,.2);border-radius:12px;padding:14px 20px;text-align:center;min-width:120px;">
          <div style="font-size:1.5rem;font-weight:800;color:#58a6ff;" id="linesCount">0</div>
          <div style="font-size:.72rem;color:#8b949e;">Lines of Code</div>
        </div>
        <div style="background:rgba(63,185,80,.08);border:1px solid rgba(63,185,80,.2);border-radius:12px;padding:14px 20px;text-align:center;min-width:120px;">
          <div style="font-size:1.5rem;font-weight:800;color:#3fb950;" id="projectsCount">0</div>
          <div style="font-size:.72rem;color:#8b949e;">Projects Built</div>
        </div>
        <div style="background:rgba(188,140,255,.08);border:1px solid rgba(188,140,255,.2);border-radius:12px;padding:14px 20px;text-align:center;min-width:120px;">
          <div style="font-size:1.5rem;font-weight:800;color:#bc8cff;" id="techCount">0</div>
          <div style="font-size:.72rem;color:#8b949e;">Technologies</div>
        </div>
        <div style="background:rgba(255,166,87,.08);border:1px solid rgba(255,166,87,.2);border-radius:12px;padding:14px 20px;text-align:center;min-width:120px;">
          <div style="font-size:1.5rem;font-weight:800;color:#ffa657;" id="hoursCount">0</div>
          <div style="font-size:.72rem;color:#8b949e;">Hrs of Learning</div>
        </div>
      </div>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       12. QUOTE
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="quote">
    <div class="quote-card">
      <div class="quote-text">
        <span>Code.</span> Deploy. <span style="color:#bc8cff">Scale.</span> <span style="color:#ff7b72">Repeat.</span>
      </div>
      <div class="quote-author">— Geeta Mehra · Developer Philosophy</div>
      <div style="margin-top:20px;display:flex;justify-content:center;gap:8px;">
        <div style="width:8px;height:8px;border-radius:50%;background:#58a6ff;box-shadow:0 0 8px #58a6ff;"></div>
        <div style="width:8px;height:8px;border-radius:50%;background:#bc8cff;box-shadow:0 0 8px #bc8cff;"></div>
        <div style="width:8px;height:8px;border-radius:50%;background:#ff7b72;box-shadow:0 0 8px #ff7b72;"></div>
      </div>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       13. VISITOR COUNTER
  ═══════════════════════════════════════════════ -->
  <section class="section reveal" id="visitor">
    <div class="section-header">
      <span class="section-icon">👁️</span>
      <h2 class="section-title">Profile Views</h2>
      <div class="section-line"></div>
    </div>

    <div class="visitor-wrap">
      <div class="visitor-label">👋 Thanks for visiting! You are visitor #</div>
      <div class="visitor-counter" id="visitorCounter"></div>
      <div style="margin-top:14px;">
        <img src="https://komarev.com/ghpvc/?username=techgeeta&label=Profile+Views&color=58a6ff&style=for-the-badge&labelColor=0d1117" alt="Profile Views" style="border-radius:8px;" />
      </div>
      <p style="margin-top:12px;font-size:.78rem;color:#8b949e;">🌍 Thanks for stopping by — Let's connect and build something amazing!</p>
    </div>
  </section>

  <div class="glow-divider"></div>

  <!-- ═══════════════════════════════════════════════
       14. FOOTER
  ═══════════════════════════════════════════════ -->
  <footer class="section reveal" id="footer">
    <!-- Wave top -->
    <svg class="footer-wave-top" viewBox="0 0 1440 60" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
      <path fill="#161b22" d="M0,30 C360,60 720,0 1080,30 C1260,45 1380,20 1440,30 L1440,0 L0,0 Z" opacity=".5"/>
    </svg>

    <div class="footer-body">
      <div class="footer-orb1"></div>
      <div class="footer-orb2"></div>

      <div style="font-size:2rem;margin-bottom:12px;position:relative;z-index:1;">✨</div>
      <div class="footer-name">GEETA MEHRA</div>
      <div class="footer-sub">☁️ Cloud & DevOps Enthusiast · MCA @ GEHU · 🚀 Always Learning</div>

      <div class="footer-glow-line"></div>

      <div class="footer-links">
        <a href="https://github.com/techgeeta" target="_blank" class="footer-link">🐙 GitHub</a>
        <span class="footer-sep">·</span>
        <a href="https://www.linkedin.com/in/geeta-mehra-b9261a2b7/" target="_blank" class="footer-link">💼 LinkedIn</a>
        <span class="footer-sep">·</span>
        <a href="mailto:techgeeta@example.com" class="footer-link">📧 Email</a>
        <span class="footer-sep">·</span>
        <a href="#about" class="footer-link">👩‍💻 About</a>
        <span class="footer-sep">·</span>
        <a href="#projects" class="footer-link">💼 Projects</a>
        <span class="footer-sep">·</span>
        <a href="#tech" class="footer-link">🛠 Skills</a>
      </div>

      <div class="footer-glow-line"></div>

      <div class="footer-bottom">
        <div>Made with <span class="footer-heart">❤️</span> &amp; lots of ☕ by <strong style="color:#58a6ff;">Geeta Mehra</strong></div>
        <div style="margin-top:6px;font-size:.72rem;">
          📍 Haldwani, Uttarakhand, India &nbsp;|&nbsp; 🎓 Graphic Era Hill University &nbsp;|&nbsp; 🌟 Open to Opportunities
        </div>
        <div style="margin-top:8px;font-size:.7rem;color:#484f58;">
          © 2025 Geeta Mehra · All Rights Reserved · Built with passion for Cloud &amp; DevOps
        </div>
      </div>
    </div>

    <!-- Wave bottom -->
    <svg viewBox="0 0 1440 60" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none" style="display:block;width:100%;margin-top:-2px;">
      <defs>
        <linearGradient id="footWaveGrad" x1="0" y1="0" x2="1" y2="0">
          <stop offset="0%"   stop-color="#58a6ff" stop-opacity=".4"/>
          <stop offset="50%"  stop-color="#bc8cff" stop-opacity=".4"/>
          <stop offset="100%" stop-color="#ff7b72" stop-opacity=".4"/>
        </linearGradient>
      </defs>
      <path fill="url(#footWaveGrad)"
        d="M0,20 C360,60 720,0 1080,30 C1260,45 1380,10 1440,20 L1440,60 L0,60 Z"/>
    </svg>
  </footer>

</div><!-- /readme-wrapper -->

<!-- ─────────────────────────────────────────────
     README OUTPUT MODAL
───────────────────────────────────────────── -->
<div id="readmeBtn" style="position:fixed;bottom:28px;right:28px;z-index:9999;">
  <button onclick="document.getElementById('readmeModal').style.display='flex'"
    style="background:linear-gradient(135deg,#1f6feb,#bc8cff);color:#fff;border:none;border-radius:14px;padding:14px 22px;font-size:.9rem;font-weight:700;cursor:pointer;box-shadow:0 8px 24px rgba(88,166,255,.4);display:flex;align-items:center;gap:10px;font-family:'Inter',sans-serif;transition:all .3s;"
    onmouseover="this.style.transform='translateY(-3px)';this.style.boxShadow='0 14px 30px rgba(88,166,255,.5)'"
    onmouseout="this.style.transform='translateY(0)';this.style.boxShadow='0 8px 24px rgba(88,166,255,.4)'">
    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><polyline points="10 9 9 9 8 9"/></svg>
    📋 Get README.md
  </button>
</div>

<!-- Modal -->
<div id="readmeModal" style="display:none;position:fixed;inset:0;background:rgba(0,0,0,.85);z-index:99999;align-items:center;justify-content:center;padding:20px;backdrop-filter:blur(8px);">
  <div style="background:#161b22;border:1px solid #30363d;border-radius:20px;max-width:860px;width:100%;max-height:90vh;overflow:hidden;display:flex;flex-direction:column;box-shadow:0 40px 80px rgba(0,0,0,.7);">
    <div style="padding:20px 24px;border-bottom:1px solid #30363d;display:flex;align-items:center;justify-content:space-between;flex-shrink:0;">
      <div>
        <div style="font-family:'Space Grotesk',sans-serif;font-weight:700;color:#e6edf3;font-size:1.1rem;">📄 README.md — Geeta Mehra</div>
        <div style="font-size:.75rem;color:#8b949e;margin-top:2px;">Copy this to your GitHub profile repository</div>
      </div>
      <div style="display:flex;gap:10px;">
        <button onclick="copyReadme()" style="background:linear-gradient(135deg,#238636,#3fb950);color:#fff;border:none;border-radius:8px;padding:8px 16px;font-size:.82rem;font-weight:700;cursor:pointer;">
          📋 Copy All
        </button>
        <button onclick="document.getElementById('readmeModal').style.display='none'" style="background:rgba(255,255,255,.07);color:#e6edf3;border:1px solid #30363d;border-radius:8px;padding:8px 14px;font-size:.82rem;cursor:pointer;">
          ✕ Close
        </button>
      </div>
    </div>
    <div style="overflow-y:auto;flex:1;">
      <pre id="readmeContent" style="padding:24px;font-family:'Fira Code',monospace;font-size:.75rem;color:#e6edf3;line-height:1.7;white-space:pre-wrap;word-break:break-word;margin:0;"></pre>
    </div>
  </div>
</div>

<div id="copyToast" style="position:fixed;bottom:100px;right:28px;background:linear-gradient(135deg,#238636,#3fb950);color:#fff;padding:12px 20px;border-radius:10px;font-size:.85rem;font-weight:700;opacity:0;transition:opacity .3s;pointer-events:none;z-index:999999;">
  ✅ README.md copied to clipboard!
</div>

<script>
// ═══ STARS ═══
(function(){
  const bg = document.getElementById('particles-bg');
  for(let i=0;i<120;i++){
    const s = document.createElement('div');
    s.className = 'star';
    const size = Math.random()*2.5+.5;
    s.style.cssText = `
      width:${size}px;height:${size}px;
      top:${Math.random()*100}%;left:${Math.random()*100}%;
      --dur:${Math.random()*4+2}s;
      --delay:${Math.random()*5}s;
    `;
    bg.appendChild(s);
  }
})();

// ═══ FLOATING ICONS ═══
(function(){
  const icons = ['☁️','⚙️','🚀','🐍','💡','🤖','🧠','🔧','📦','🌐'];
  const wrap = document.getElementById('floatingIcons');
  icons.forEach((icon, i) => {
    const el = document.createElement('div');
    el.className = 'float-icon';
    el.textContent = icon;
    el.style.cssText = `left:${10+i*9}%;--dur:${6+Math.random()*6}s;--delay:${Math.random()*-8}s;bottom:-30px;`;
    wrap.appendChild(el);
  });
})();

// ═══ TYPING ANIMATION ═══
(function(){
  const phrases = [
    'Cloud ☁️  | DevOps ⚙️  | AWS 🚀  | Automation 🔥  | Always Learning',
    'Building Scalable Systems 🏗️  | Automating Everything ⚡',
    'MCA Student @ GEHU 🎓  | Haldwani, India 📍',
    'Open to Internships 💼  | Let\'s Build Together 🤝',
    'Code → Deploy → Scale → Repeat 🔄'
  ];
  let pi=0, ci=0, deleting=false;
  const el = document.getElementById('typed-text');
  function type(){
    const phrase = phrases[pi];
    if(!deleting){
      el.textContent = phrase.slice(0,++ci);
      if(ci===phrase.length){ deleting=true; setTimeout(type,1800); return; }
    } else {
      el.textContent = phrase.slice(0,--ci);
      if(ci===0){ deleting=false; pi=(pi+1)%phrases.length; setTimeout(type,400); return; }
    }
    setTimeout(type, deleting?30:55);
  }
  setTimeout(type, 1200);
})();

// ═══ SCROLL REVEAL ═══
(function(){
  const obs = new IntersectionObserver(entries=>{
    entries.forEach(e=>{ if(e.isIntersecting) e.target.classList.add('revealed'); });
  },{threshold:.08});
  document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));
})();

// ═══ SKILL BARS ═══
(function(){
  const skills = [
    {name:'Cloud (AWS/Azure)', pct:72, color:'#ff9900'},
    {name:'DevOps & CI/CD',    pct:65, color:'#d24939'},
    {name:'Python / ML',       pct:70, color:'#3776ab'},
    {name:'JavaScript',        pct:68, color:'#f7df1e'},
    {name:'Linux / CLI',       pct:75, color:'#ffa657'},
    {name:'C / C++ / Java',    pct:80, color:'#58a6ff'},
  ];
  const wrap = document.getElementById('skillBars');
  skills.forEach(s=>{
    wrap.insertAdjacentHTML('beforeend',`
      <div style="margin-bottom:12px;">
        <div style="display:flex;justify-content:space-between;margin-bottom:4px;">
          <span style="font-size:.75rem;color:#c9d1d9;font-weight:600;">${s.name}</span>
          <span style="font-size:.72rem;color:${s.color};font-family:'Fira Code',monospace;">${s.pct}%</span>
        </div>
        <div style="height:5px;background:rgba(255,255,255,.07);border-radius:3px;overflow:hidden;">
          <div style="height:100%;width:0;background:linear-gradient(90deg,${s.color}88,${s.color});border-radius:3px;transition:width 1.5s ease;" data-w="${s.pct}%" class="bar-fill"></div>
        </div>
      </div>
    `);
  });
  setTimeout(()=>{
    document.querySelectorAll('.bar-fill').forEach(b=>b.style.width=b.dataset.w);
  },600);
})();

// ═══ RADAR CHART ═══
(function(){
  const canvas = document.getElementById('radarChart');
  if(!canvas) return;
  const ctx = canvas.getContext('2d');
  const W=220,H=220,cx=W/2,cy=H/2,R=80;
  const categories = ['Cloud','DevOps','Python','JS','Linux','AI/ML'];
  const values     = [.72,.65,.70,.68,.75,.60];
  const N = categories.length;
  const angle = i => (Math.PI*2/N)*i - Math.PI/2;
  const colors = ['#58a6ff','#ff7b72','#3776ab','#f7df1e','#ffa657','#bc8cff'];

  function draw(){
    ctx.clearRect(0,0,W,H);
    // grid
    for(let r=1;r<=5;r++){
      ctx.beginPath();
      for(let i=0;i<N;i++){
        const a=angle(i), d=(R*r/5);
        i===0?ctx.moveTo(cx+d*Math.cos(a),cy+d*Math.sin(a)):ctx.lineTo(cx+d*Math.cos(a),cy+d*Math.sin(a));
      }
      ctx.closePath();
      ctx.strokeStyle='rgba(48,54,61,.8)';ctx.lineWidth=1;ctx.stroke();
    }
    // spokes
    for(let i=0;i<N;i++){
      ctx.beginPath();ctx.moveTo(cx,cy);
      ctx.lineTo(cx+R*Math.cos(angle(i)),cy+R*Math.sin(angle(i)));
      ctx.strokeStyle='rgba(48,54,61,.6)';ctx.lineWidth=1;ctx.stroke();
    }
    // fill
    ctx.beginPath();
    for(let i=0;i<N;i++){
      const a=angle(i),d=R*values[i];
      i===0?ctx.moveTo(cx+d*Math.cos(a),cy+d*Math.sin(a)):ctx.lineTo(cx+d*Math.cos(a),cy+d*Math.sin(a));
    }
    ctx.closePath();
    const g=ctx.createRadialGradient(cx,cy,0,cx,cy,R);
    g.addColorStop(0,'rgba(88,166,255,.4)');
    g.addColorStop(1,'rgba(188,140,255,.15)');
    ctx.fillStyle=g;ctx.fill();
    ctx.strokeStyle='#58a6ff';ctx.lineWidth=2;ctx.stroke();
    // dots & labels
    for(let i=0;i<N;i++){
      const a=angle(i),d=R*values[i];
      const px=cx+d*Math.cos(a),py=cy+d*Math.sin(a);
      ctx.beginPath();ctx.arc(px,py,4,0,Math.PI*2);
      ctx.fillStyle=colors[i];ctx.fill();
      // label
      const lx=cx+(R+18)*Math.cos(a),ly=cy+(R+18)*Math.sin(a);
      ctx.fillStyle='#8b949e';ctx.font='10px Inter';ctx.textAlign='center';ctx.textBaseline='middle';
      ctx.fillText(categories[i],lx,ly);
    }
  }
  draw();
})();

// ═══ SNAKE CANVAS ═══
(function(){
  const canvas = document.getElementById('snakeCanvas');
  if(!canvas) return;
  canvas.width = canvas.parentElement.offsetWidth - 40 || 900;
  const H = 120, W = canvas.width;
  canvas.height = H;
  const ctx = canvas.getContext('2d');
  const CELL = 12;
  const cols = Math.floor(W/CELL), rows = Math.floor(H/CELL);

  // Generate contribution grid
  const grid = [];
  for(let r=0;r<rows;r++){
    grid[r]=[];
    for(let c=0;c<cols;c++) grid[r][c] = Math.random()<.3?1:0;
  }

  let snake = [{x:0,y:Math.floor(rows/2)}];
  let dir = {x:1,y:0};
  let food = findFood();

  function findFood(){
    for(let c=snake[0].x+1;c<cols;c++){
      if(grid[Math.floor(rows/2)][c]) return {x:c,y:Math.floor(rows/2)};
      for(let r=0;r<rows;r++) if(grid[r][c]) return {x:c,y:r};
    }
    return {x:Math.floor(Math.random()*cols),y:Math.floor(Math.random()*rows)};
  }

  function step(){
    const head={x:snake[0].x+dir.x,y:snake[0].y+dir.y};
    if(head.x>=cols||head.x<0||head.y>=rows||head.y<0){
      snake=[{x:0,y:Math.floor(rows/2)}];dir={x:1,y:0};food=findFood();return;
    }
    snake.unshift(head);
    if(head.x===food.x&&head.y===food.y){
      grid[food.y][food.x]=0;food=findFood();
    } else { snake.pop(); }
    // steer toward food
    const dx=food.x-snake[0].x, dy=food.y-snake[0].y;
    if(Math.abs(dx)>Math.abs(dy)) dir={x:dx>0?1:-1,y:0};
    else dir={x:0,y:dy>0?1:-1};
  }

  function render(){
    ctx.clearRect(0,0,W,H);
    ctx.fillStyle='#0d1117';ctx.fillRect(0,0,W,H);
    // grid cells
    for(let r=0;r<rows;r++){
      for(let c=0;c<cols;c++){
        if(grid[r][c]){
          const intensity = Math.random()>.7?1:.5;
          ctx.fillStyle=`rgba(57,211,83,${0.3+intensity*.4})`;
          ctx.beginPath();ctx.roundRect(c*CELL+1,r*CELL+1,CELL-2,CELL-2,2);ctx.fill();
        } else {
          ctx.fillStyle='rgba(255,255,255,.04)';
          ctx.beginPath();ctx.roundRect(c*CELL+1,r*CELL+1,CELL-2,CELL-2,2);ctx.fill();
        }
      }
    }
    // snake
    snake.forEach((seg,i)=>{
      const t = i/snake.length;
      ctx.fillStyle=`hsl(${140-t*40},70%,${50-t*20}%)`;
      ctx.beginPath();ctx.roundRect(seg.x*CELL+1,seg.y*CELL+1,CELL-2,CELL-2,3);ctx.fill();
    });
    // head eyes
    if(snake.length>0){
      const h=snake[0];
      ctx.fillStyle='#fff';
      ctx.beginPath();ctx.arc(h.x*CELL+4,h.y*CELL+4,2,0,Math.PI*2);ctx.fill();
      ctx.fillStyle='#0d1117';
      ctx.beginPath();ctx.arc(h.x*CELL+4,h.y*CELL+4,1,0,Math.PI*2);ctx.fill();
    }
    // food highlight
    ctx.fillStyle='rgba(88,166,255,.8)';
    ctx.shadowColor='#58a6ff';ctx.shadowBlur=8;
    ctx.beginPath();ctx.roundRect(food.x*CELL+1,food.y*CELL+1,CELL-2,CELL-2,3);ctx.fill();
    ctx.shadowBlur=0;
  }

  setInterval(()=>{step();render();},80);
})();

// ═══ VISITOR COUNTER ═══
(function(){
  const count = Math.floor(Math.random()*800+1200);
  const s = String(count).padStart(6,'0');
  const wrap = document.getElementById('visitorCounter');
  [...s].forEach((d,i)=>{
    if(i>0&&i%3===0) wrap.insertAdjacentHTML('beforeend','<span class="v-sep">,</span>');
    wrap.insertAdjacentHTML('beforeend',`<div class="v-digit" style="animation-delay:${i*.12}s">${d}</div>`);
  });
})();

// ═══ COUNTER ANIMATION ═══
(function(){
  const counters = [
    {id:'linesCount',  target:50000,  suffix:'K+', div:1000},
    {id:'projectsCount',target:12,   suffix:'+',  div:1},
    {id:'techCount',   target:20,    suffix:'+',  div:1},
    {id:'hoursCount',  target:500,   suffix:'+',  div:1},
  ];
  const obs = new IntersectionObserver(entries=>{
    entries.forEach(e=>{
      if(!e.isIntersecting) return;
      counters.forEach(c=>{
        const el=document.getElementById(c.id);
        if(!el) return;
        let v=0;
        const step=c.target/60;
        const timer=setInterval(()=>{
          v=Math.min(v+step,c.target);
          el.textContent=c.div>1?Math.floor(v/c.div)+c.suffix:Math.floor(v)+c.suffix;
          if(v>=c.target) clearInterval(timer);
        },25);
      });
      obs.disconnect();
    });
  },{threshold:.3});
  const fun=document.getElementById('fun');
  if(fun) obs.observe(fun);
})();

// ═══ README CONTENT ═══
const README_CONTENT = `<!-- 🌟 GEETA MEHRA — GITHUB PROFILE README 🌟 -->
<!-- Made with ❤️ | Ultra-Premium Developer Portfolio -->

<div align="center">

<!-- ═══════════ ANIMATED HEADER BANNER ═══════════ -->

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=GEETA%20MEHRA&fontSize=60&fontAlignY=35&desc=☁️%20Cloud%20%26%20DevOps%20Enthusiast%20%7C%20🎓%20MCA%20%40%20GEHU%20%7C%20🚀%20Always%20Learning&descAlignY=55&animation=fadeIn&fontColor=fff" alt="Header Banner"/>

<!-- LIVE STATUS BADGE -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2800&pause=1200&color=58A6FF&center=true&vCenter=true&multiline=false&width=700&lines=Cloud+☁️+|+DevOps+⚙️+|+AWS+🚀+|+Automation+🔥+|+Always+Learning;Building+Scalable+Systems+🏗️+|+Automating+Everything+⚡;MCA+Student+%40+GEHU+🎓+|+Haldwani%2C+India+📍;Open+to+Internships+💼+|+Let's+Build+Together+🤝;Code+→+Deploy+→+Scale+→+Repeat+🔄" alt="Typing SVG" />

<br/>

<img src="https://img.shields.io/badge/📍%20Location-Haldwani%2C%20Uttarakhand-blue?style=for-the-badge&labelColor=0d1117&color=58a6ff"/>
<img src="https://img.shields.io/badge/🎓%20MCA-Graphic%20Era%20Hill%20University-purple?style=for-the-badge&labelColor=0d1117&color=bc8cff"/>
<img src="https://img.shields.io/badge/💼%20Status-Open%20to%20Opportunities-green?style=for-the-badge&labelColor=0d1117&color=3fb950"/>
<img src="https://komarev.com/ghpvc/?username=techgeeta&label=Profile+Views&color=58a6ff&style=for-the-badge&labelColor=0d1117"/>

</div>

---

<!-- ═══════════ ABOUT ME ═══════════ -->

<div align="center">
<h2>👩‍💻 About Me</h2>
</div>

\`\`\`javascript
const geeta = {
  name:      "Geeta Mehra",
  role:      "Cloud & DevOps Enthusiast 🚀",
  education: "MCA @ Graphic Era Hill University, Haldwani",
  location:  "Haldwani, Uttarakhand, India 🇮🇳",
  passion:   ["Cloud Computing ☁️", "DevOps & CI/CD ⚙️", "AI Integration 🧠", "Open Source 🌐"],
  superpower: "Fast Learner · Problem Solver · Team Player",
  status:    "Always Learning & Building 🔥"
};
\`\`\`

> 🎯 *MCA student passionate about Cloud, DevOps, and AI integrations.*
> Strong interest in AWS, CI/CD, automation pipelines. Loves building real-world applications.
> Fast learner + problem solver 💪

---

<!-- ═══════════ WHAT I DO ═══════════ -->

<div align="center">
<h2>🚀 What I Do</h2>

| ☁️ Cloud Computing | ⚙️ DevOps | 🤖 Automation | 🧠 AI Integration |
|:---:|:---:|:---:|:---:|
| AWS · Azure · Cloudflare | Jenkins · Docker · GitHub Actions | Python · Bash · YAML | scikit-learn · Pandas · NumPy |
| EC2 · S3 · Lambda | CI/CD Pipelines | Workflow Automation | ML Model Integration |
| Cloud Architecture | Infrastructure as Code | Scripting & Testing | Data-Driven Features |

</div>

---

<!-- ═══════════ TECH STACK ═══════════ -->

<div align="center">
<h2>🛠 Tech Stack</h2>

**💻 Languages**

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![C++](https://img.shields.io/badge/C++-00427E?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

**☁️ Cloud Platforms**

![AWS](https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)

**⚙️ DevOps & CI/CD**

![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![Apache](https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=apache&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-FC6D26?style=for-the-badge&logo=gitlab&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

**🔧 Tools & Design**

![Canva](https://img.shields.io/badge/Canva-00C4CC?style=for-the-badge&logo=canva&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Cisco](https://img.shields.io/badge/Cisco-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

**🧠 Data / AI / ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

</div>

---

<!-- ═══════════ FEATURED PROJECT ═══════════ -->

<div align="center">
<h2>💼 Featured Project</h2>
</div>

<div align="center">

### 🌟 GramStay AI Booking Platform

> *A full-stack AI-powered booking platform for village homestays in the Jim Corbett region of Uttarakhand.*

![React](https://img.shields.io/badge/React.js-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=flat-square&logo=node.js&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)

| Feature | Description |
|---------|-------------|
| 🤖 AI Recommendations | Personalized homestay suggestions powered by ML |
| 🏠 Homestay Listings | Curated village stays in Jim Corbett region |
| 📅 Booking System | Real-time availability & instant booking |
| 💳 Payments | Secure payment integration |
| 📱 Responsive | Fully responsive across all devices |
| 🌿 Eco Tourism | Supporting sustainable rural tourism in Uttarakhand |

[![GitHub](https://img.shields.io/badge/💻%20GitHub%20Repo-181717?style=for-the-badge&logo=github)](https://github.com/techgeeta)
[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-3fb950?style=for-the-badge&logo=vercel&logoColor=white)](https://github.com/techgeeta)

</div>

---

<!-- ═══════════ GITHUB ANALYTICS ═══════════ -->

<div align="center">
<h2>📊 GitHub Analytics</h2>

<img height="180em" src="https://github-readme-stats.vercel.app/api?username=techgeeta&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=bc8cff&text_color=c9d1d9&border_radius=16"/>
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=techgeeta&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9&border_radius=16&langs_count=8"/>

<img width="100%" src="https://github-readme-streak-stats.herokuapp.com/?user=techgeeta&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=30363d&ring=58a6ff&fire=ff7b72&currStreakNum=e6edf3&sideNums=e6edf3&currStreakLabel=bc8cff&sideLabels=8b949e&dates=8b949e&border_radius=16"/>

<img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=techgeeta&bg_color=0d1117&color=58a6ff&line=bc8cff&point=ff7b72&area=true&hide_border=true&area_color=58a6ff"/>

</div>

---

<!-- ═══════════ SNAKE ANIMATION ═══════════ -->

<div align="center">
<h2>🐍 Contribution Snake</h2>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/techgeeta/techgeeta/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/techgeeta/techgeeta/output/github-contribution-grid-snake.svg"/>
  <img alt="Snake animation" src="https://raw.githubusercontent.com/techgeeta/techgeeta/output/github-contribution-grid-snake-dark.svg"/>
</picture>

*🐍 Watch the snake eat my GitHub contributions!*

</div>

---

<!-- ═══════════ ACHIEVEMENTS ═══════════ -->

<div align="center">
<h2>🏆 Achievements & Certifications</h2>
</div>

| 🏅 Achievement | 📝 Description | 📌 Status |
|---|---|---|
| 🏅 Deloitte Technology Job Simulation | Real-world tech simulation covering software engineering & data analysis | ✅ Completed |
| ☁️ AWS Cloud Foundations | Core AWS services: EC2, S3, Lambda, IAM, cloud architecture | 🔄 In Progress |
| ⚙️ DevOps Tools Mastery | Jenkins, Docker, Apache, Git-based CI/CD workflows | 🔄 In Progress |
| 🎓 MCA @ GEHU | Master of Computer Applications — Cloud, Software Engineering, AI | 📚 Ongoing |
| 🐍 Python for Data Science | Pandas, NumPy, scikit-learn — data analysis & ML models | ✅ Completed |
| 🌐 Open Source Contributor | Contributing to open-source projects & building on GitHub | 🌱 Growing |

---

<!-- ═══════════ CURRENT GOALS ═══════════ -->

<div align="center">
<h2>🎯 Current Goals</h2>

| # | 🎯 Goal | 📈 Progress |
|---|---------|------------|
| 01 | ⚙️ Master DevOps Tools (K8s, Terraform, Ansible) | ██████░░░░ 65% |
| 02 | 🏗️ Build Production-Ready Cloud Systems | █████░░░░░ 50% |
| 03 | 🌍 Contribute to Open Source | ███░░░░░░░ 30% |
| 04 | 💼 Secure Top Tech Job / Internship | ████░░░░░░ 40% |

</div>

---

<!-- ═══════════ CONNECT ═══════════ -->

<div align="center">
<h2>🌐 Connect With Me</h2>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/geeta-mehra-b9261a2b7/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/techgeeta)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:techgeeta@example.com)

<br/>

> 🟢 **Open to Opportunities** — Internships · Part-time · Freelance · Collaborations

</div>

---

<!-- ═══════════ FUN SECTION ═══════════ -->

<div align="center">

☁️ ⚙️ 🚀 🤖 ✨ 🐍 💡

### *"I turn ideas into cloud-powered solutions ☁️✨"*

*Bridging the gap between imagination and infrastructure, one deploy at a time.*

![Lines of Code](https://img.shields.io/badge/Lines%20of%20Code-50K+-58a6ff?style=flat-square&labelColor=0d1117)
![Projects](https://img.shields.io/badge/Projects%20Built-12+-3fb950?style=flat-square&labelColor=0d1117)
![Technologies](https://img.shields.io/badge/Technologies-20+-bc8cff?style=flat-square&labelColor=0d1117)
![Learning Hours](https://img.shields.io/badge/Learning%20Hours-500+-ffa657?style=flat-square&labelColor=0d1117)

</div>

---

<!-- ═══════════ QUOTE ═══════════ -->

<div align="center">

> # 💬 *"Code. Deploy. Scale. Repeat."*
> **— Geeta Mehra · Developer Philosophy**

</div>

---

<!-- ═══════════ VISITOR COUNTER ═══════════ -->

<div align="center">

👋 **Thanks for visiting!**

![Profile Views](https://komarev.com/ghpvc/?username=techgeeta&label=Profile+Views&color=58a6ff&style=for-the-badge&labelColor=0d1117)

*🌍 Thanks for stopping by — Let's connect and build something amazing!*

</div>

---

<!-- ═══════════ FOOTER BANNER ═══════════ -->

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&text=Made%20with%20❤️%20by%20Geeta%20Mehra&fontSize=24&fontAlignY=65&animation=fadeIn&fontColor=fff" alt="Footer Banner"/>

**📍 Haldwani, Uttarakhand, India 🇮🇳 | 🎓 Graphic Era Hill University | ⭐ Star my repos!**

*© 2025 Geeta Mehra · Built with passion for Cloud & DevOps*

</div>

<!-- 
  ✨ Setup Instructions:
  1. Create repo named "techgeeta" (same as username)
  2. Create this file as README.md
  3. For snake animation: Add GitHub Action workflow in .github/workflows/snake.yml
  4. For streak stats: May need to sign up at https://streak-stats.demolab.com/
  5. All badge/stats URLs use your username "techgeeta"
-->`;

document.getElementById('readmeContent').textContent = README_CONTENT;

function copyReadme(){
  navigator.clipboard.writeText(README_CONTENT).then(()=>{
    const t = document.getElementById('copyToast');
    t.style.opacity='1';
    setTimeout(()=>t.style.opacity='0',2800);
  });
}
</script>
</body>
</html>
