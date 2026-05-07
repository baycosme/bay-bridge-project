
<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>BAYBRIDGE PROJECT 第1弾 募集LP — D2C × ドラッグストア攻略プロジェクト</title>
<meta name="description" content="SNSで売れたD2Cブランドを、全国ドラッグストア10,000店舗の棚へ。バイヤー商談から店頭設計まで、ベイコスメが全部引き受けます。第1期 3〜5社限定。" />
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;600;700&family=Montserrat:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet" />
<style>
  :root {
    --navy: #0B2341;
    --navy-deep: #071935;
    --navy-soft: #14325A;
    --gold: #C9A86A;
    --gold-hi: #DDC388;
    --teal: #2E9C9E;
    --teal-hi: #4FB8BA;
    --ink: #0E1A2D;
    --muted: #5A6475;
    --line: rgba(11, 35, 65, .12);
    --bg: #F5F2EC;
    --bg-deep: #EBE6DC;
    --f-sans: 'Noto Sans JP', -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
    --f-display: 'Montserrat', 'Noto Sans JP', sans-serif;
    --f-mono: 'JetBrains Mono', 'Menlo', 'Consolas', monospace;
  }

  * { box-sizing: border-box; }

  html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    font-family: var(--f-sans);
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
    background: var(--bg);
    color: var(--ink);
    scroll-behavior: smooth;
  }

  ::selection { background: var(--gold); color: var(--navy); }

  a { color: inherit; }
  ul { list-style: none; padding: 0; margin: 0; }
  button { font: inherit; }

  /* ─── animations ─── */
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: .4; }
  }
  @keyframes scrollDot {
    0% { transform: scaleY(0); transform-origin: top; }
    50% { transform: scaleY(1); transform-origin: top; }
    50.01% { transform: scaleY(1); transform-origin: bottom; }
    100% { transform: scaleY(0); transform-origin: bottom; }
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ─── shared atoms ─── */
  .container {
    max-width: 1120px;
    margin: 0 auto;
  }

  .section-tag {
    display: flex;
    align-items: center;
    gap: 12px;
    font-family: var(--f-mono);
    font-size: 11px;
    letter-spacing: .24em;
    text-transform: uppercase;
    color: var(--navy);
    margin-bottom: 20px;
  }
  .section-tag .num { color: var(--gold); font-weight: 700; }
  .section-tag .bar { width: 40px; height: 1px; background: var(--line); }
  .section-tag.invert { color: rgba(255, 255, 255, .7); }
  .section-tag.invert .bar { background: rgba(255, 255, 255, .3); }

  .h2 {
    font-family: var(--f-sans);
    font-weight: 700;
    font-size: clamp(28px, 3.2vw, 40px);
    line-height: 1.3;
    letter-spacing: .01em;
    color: var(--navy-deep);
    margin: 0 0 32px;
  }
  .h2.invert { color: #fff; }
  .h2.center { text-align: center; }

  /* ─── btn ─── */
  .btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    font-family: var(--f-sans);
    font-weight: 600;
    letter-spacing: .02em;
    text-decoration: none;
    cursor: pointer;
    border: none;
    transition: transform .18s ease, box-shadow .18s ease, background .18s ease;
    position: relative;
  }
  .btn:hover { transform: translateY(-2px); }
  .btn-lg { padding: 18px 28px; font-size: 15px; min-width: 240px; height: 56px; }
  .btn-md { padding: 12px 18px; font-size: 13px; min-width: 160px; height: 44px; }
  .btn-sm { padding: 8px 14px; font-size: 12px; min-width: 120px; height: 36px; }
  .btn-gold {
    background: linear-gradient(180deg, var(--gold-hi) 0%, var(--gold) 100%);
    color: var(--navy-deep);
    box-shadow: 0 1px 0 rgba(255, 255, 255, .35) inset, 0 8px 24px rgba(201, 168, 106, .35);
  }
  .btn-white-outline {
    background: transparent;
    color: #fff;
    box-shadow: inset 0 0 0 1px rgba(255, 255, 255, .5);
  }
  .btn-full { width: 100%; }

  /* ─── photo placeholder ─── */
  .photo {
    position: relative;
    width: 100%;
    aspect-ratio: 16 / 10;
    color: rgba(255, 255, 255, .45);
    display: flex;
    align-items: flex-end;
    justify-content: flex-start;
    padding: 16px;
    font-family: 'Menlo', 'Consolas', monospace;
    font-size: 11px;
    letter-spacing: .04em;
    background: repeating-linear-gradient(135deg, #0A1A30 0 14px, rgba(255, 255, 255, .035) 14px 15px);
  }
  .photo .label {
    background: rgba(11, 26, 48, .8);
    padding: 4px 8px;
    border: 1px solid rgba(255, 255, 255, .15);
  }
  .photo.aspect-4-5 { aspect-ratio: 4 / 5; }
  .photo.fill { width: 100%; height: 100%; aspect-ratio: auto; }

  /* ─── header ─── */
  .header {
    position: sticky;
    top: 0;
    z-index: 40;
    height: 60px;
    background: rgba(245, 242, 236, .88);
    backdrop-filter: blur(14px);
    -webkit-backdrop-filter: blur(14px);
    border-bottom: 1px solid var(--line);
    display: flex;
    align-items: center;
    padding: 0 40px;
  }
  .header-actions {
    margin-left: auto;
    display: flex;
    align-items: center;
    gap: 20px;
  }
  .header-nav {
    display: flex;
    gap: 24px;
    font-family: var(--f-sans);
    font-size: 12px;
    letter-spacing: .04em;
    color: var(--muted);
  }
  .header-nav a { text-decoration: none; }

  /* ─── logo ─── */
  .logo {
    display: flex;
    align-items: center;
    gap: 10px;
    text-decoration: none;
  }
  .logo-mark {
    width: 36px;
    height: 36px;
    display: block;
    object-fit: contain;
    flex-shrink: 0;
  }
  .footer .logo-mark {
    filter: brightness(0) invert(1);
    opacity: .9;
  }
  .logo-text {
    display: flex;
    flex-direction: column;
    line-height: 1;
  }
  .logo-name {
    font-family: var(--f-display);
    font-size: 15px;
    font-weight: 700;
    letter-spacing: .12em;
    color: var(--navy-deep);
  }
  .logo-sub {
    font-family: var(--f-mono);
    font-size: 8px;
    letter-spacing: .18em;
    color: var(--muted);
    margin-top: 3px;
  }

  /* ─── S1 Hero ─── */
  .hero {
    position: relative;
    min-height: 720px;
    background: var(--navy-deep);
    color: #fff;
    overflow: hidden;
  }
  .hero-kv {
    position: absolute;
    inset: 0;
    will-change: transform;
  }
  .hero-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(180deg, rgba(7, 25, 53, .72) 0%, rgba(7, 25, 53, .85) 60%, rgba(7, 25, 53, .95) 100%);
  }
  .hero-glow {
    position: absolute;
    right: -10%;
    top: -10%;
    width: 500px;
    height: 500px;
    background: radial-gradient(circle at 30% 30%, rgba(201, 168, 106, .18), transparent 60%);
    pointer-events: none;
  }
  .hero-inner {
    position: relative;
    z-index: 2;
    max-width: 1120px;
    margin: 0 auto;
    padding: 88px 40px 120px;
    min-height: 720px;
    display: grid;
    grid-template-columns: .85fr 1.15fr;
    gap: 56px;
    align-items: center;
  }
  .hero-text { text-align: left; }
  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 8px 16px;
    border: 1px solid var(--gold);
    color: var(--gold);
    font-family: var(--f-mono);
    font-size: 11px;
    letter-spacing: .18em;
    margin-bottom: 32px;
  }
  .hero-badge .dot {
    width: 6px;
    height: 6px;
    background: var(--gold);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }
  .hero h1 {
    font-family: var(--f-sans);
    font-weight: 700;
    font-size: clamp(38px, 4.4vw, 56px);
    line-height: 1.22;
    letter-spacing: .01em;
    margin: 0 0 24px;
    color: #fff;
  }
  .hero h1 .gold-mark {
    position: relative;
    color: var(--gold);
  }
  .hero h1 .gold-mark::after {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    bottom: -4px;
    height: 6px;
    background: linear-gradient(90deg, var(--gold) 0%, transparent 100%);
    opacity: .4;
  }
  .hero-lead {
    font-family: var(--f-sans);
    font-size: 20px;
    line-height: 1.7;
    color: rgba(255, 255, 255, .88);
    margin: 0 0 12px;
    max-width: 640px;
    font-weight: 500;
  }
  .hero-sub {
    font-family: var(--f-sans);
    font-size: 14px;
    line-height: 1.8;
    color: rgba(255, 255, 255, .65);
    margin: 0 0 40px;
    max-width: 560px;
  }
  .hero-cta {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    justify-content: flex-start;
    margin-bottom: 36px;
  }
  .hero-promise {
    display: flex;
    flex-direction: column;
    gap: 8px;
    padding: 18px 22px;
    border-left: 2px solid var(--gold);
    background: rgba(255, 255, 255, .04);
    max-width: 520px;
    margin-bottom: 32px;
  }
  .hero-promise-label {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .22em;
    color: var(--gold);
    font-weight: 700;
  }
  .hero-promise-text {
    font-family: var(--f-sans);
    font-size: 16px;
    line-height: 1.65;
    color: rgba(255, 255, 255, .92);
    font-weight: 600;
  }
  .hero-promise-text .hp-em {
    color: var(--gold);
    border-bottom: 1px solid rgba(201, 168, 106, .4);
    padding-bottom: 1px;
    font-family: var(--f-display);
    letter-spacing: .03em;
  }
  .hero-promise-note {
    font-family: var(--f-sans);
    font-size: 11px;
    color: rgba(255, 255, 255, .5);
    font-weight: 400;
    margin-top: 2px;
  }

  .hero-img-wrap { position: relative; }
  .hero-img {
    display: block;
    width: 100%;
    height: auto;
    object-fit: contain;
  }
  .hero-img-frame {
    position: relative;
    border: 1px solid rgba(201, 168, 106, .35);
    padding: 10px;
    background: rgba(11, 35, 65, .4);
  }
  .hero-img-frame .corner {
    position: absolute;
    width: 20px;
    height: 20px;
  }
  .hero-img-frame .corner.tl {
    top: -1px;
    left: -1px;
    border-top: 2px solid var(--gold);
    border-left: 2px solid var(--gold);
  }
  .hero-img-frame .corner.br {
    bottom: -1px;
    right: -1px;
    border-bottom: 2px solid var(--gold);
    border-right: 2px solid var(--gold);
  }
  .shelf-ready {
    position: absolute;
    bottom: -20px;
    right: -20px;
    padding: 12px 20px;
    background: var(--gold);
    color: var(--navy-deep);
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .2em;
    font-weight: 700;
  }

  .scroll-hint {
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    color: rgba(255, 255, 255, .5);
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .2em;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 6px;
  }
  .scroll-hint .line {
    width: 1px;
    height: 32px;
    background: rgba(255, 255, 255, .3);
    animation: scrollDot 2s ease-in-out infinite;
  }

  /* ─── S2 Problems ─── */
  .problems {
    background: var(--bg-deep);
    padding: 120px 40px;
  }
  .problems-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
    margin-top: 48px;
  }
  .problem-card {
    background: #fff;
    border: 1px solid var(--line);
    padding: 32px;
    position: relative;
    opacity: 0;
    transform: translateY(24px);
    transition: transform .6s cubic-bezier(.2, .7, .3, 1), opacity .6s;
  }
  .problem-card.in-view {
    opacity: 1;
    transform: translateY(0);
  }
  .problem-card.in-view:nth-child(1) { transition-delay: 80ms; }
  .problem-card.in-view:nth-child(2) { transition-delay: 160ms; }
  .problem-card.in-view:nth-child(3) { transition-delay: 240ms; }
  .problem-card .pain-no {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .2em;
    color: var(--muted);
    margin-bottom: 20px;
  }
  .problem-card p {
    font-family: var(--f-sans);
    font-size: 16px;
    line-height: 1.8;
    color: var(--ink);
    margin: 20px 0 0;
    font-weight: 500;
  }
  .problem-card .tag {
    margin-top: 24px;
    padding-top: 16px;
    border-top: 1px solid var(--line);
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .18em;
    color: var(--gold);
    font-weight: 700;
  }

  /* ─── S3 About ─── */
  .about {
    background: var(--navy-deep);
    color: #fff;
    padding: 120px 40px;
    position: relative;
    overflow: hidden;
  }
  .about-grid-bg {
    position: absolute;
    inset: 0;
    opacity: .3;
    background-image:
      linear-gradient(rgba(255, 255, 255, .04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255, 255, 255, .04) 1px, transparent 1px);
    background-size: 48px 48px;
    pointer-events: none;
  }
  .about-inner {
    max-width: 1120px;
    margin: 0 auto;
    position: relative;
  }
  .industry-first {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 6px 14px;
    background: var(--gold);
    color: var(--navy-deep);
    font-family: var(--f-mono);
    font-size: 11px;
    letter-spacing: .2em;
    font-weight: 700;
    margin-bottom: 20px;
  }
  .about-headline-row {
    margin: 10px 0 72px;
  }
  .about-headline-row h2 {
    font-family: var(--f-sans);
    font-size: 52px;
    font-weight: 700;
    line-height: 1.35;
    letter-spacing: .01em;
    margin: 0 0 40px;
    text-wrap: pretty;
    color: #fff;
    max-width: 920px;
  }
  .about-headline-row h2 .gold { color: var(--gold); }
  .about-desc {
    font-family: var(--f-sans);
    font-size: 15px;
    line-height: 1.95;
    color: rgba(255, 255, 255, .78);
    max-width: 760px;
    padding-left: 24px;
    border-left: 2px solid var(--gold);
    font-weight: 500;
  }
  .about-desc-tag {
    font-family: var(--f-mono);
    font-size: 11px;
    letter-spacing: .22em;
    color: var(--gold);
    margin-bottom: 14px;
    font-weight: 700;
  }
  .pillars {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    border-top: 1px solid rgba(255, 255, 255, .15);
    border-left: 1px solid rgba(255, 255, 255, .15);
  }
  .pillar {
    border-right: 1px solid rgba(255, 255, 255, .15);
    border-bottom: 1px solid rgba(255, 255, 255, .15);
    padding: 32px;
    position: relative;
    min-height: 280px;
    display: flex;
    flex-direction: column;
  }
  .pillar .no {
    font-family: var(--f-mono);
    font-size: 44px;
    font-weight: 300;
    color: var(--gold);
    line-height: 1;
    margin-bottom: 16px;
  }
  .pillar .accent {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .2em;
    color: rgba(201, 168, 106, .6);
    margin-bottom: 12px;
  }
  .pillar h3 {
    font-family: var(--f-sans);
    font-size: 22px;
    font-weight: 700;
    margin: 0 0 12px;
    color: #fff;
  }
  .pillar p {
    font-family: var(--f-sans);
    font-size: 14px;
    line-height: 1.8;
    color: rgba(255, 255, 255, .7);
    margin: 0;
  }
  .deploy-box {
    margin-top: 72px;
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: center;
    gap: 32px;
    padding: 36px 48px;
    border: 1px solid var(--gold);
    background: rgba(201, 168, 106, .06);
  }
  .deploy-label {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .22em;
    color: var(--gold);
    margin-bottom: 14px;
    font-weight: 700;
  }
  .deploy-headline {
    font-family: var(--f-sans);
    font-size: 24px;
    font-weight: 700;
    line-height: 1.55;
    color: #fff;
    letter-spacing: .01em;
    margin-bottom: 10px;
  }
  .deploy-period {
    font-family: var(--f-display);
    color: var(--gold);
    letter-spacing: .04em;
    white-space: nowrap;
    padding: 0 .1em;
  }
  .deploy-note {
    font-family: var(--f-sans);
    font-size: 11px;
    color: rgba(255, 255, 255, .55);
    font-weight: 400;
  }
  .deploy-tag {
    padding: 10px 18px;
    background: var(--gold);
    color: var(--navy-deep);
    font-family: var(--f-mono);
    font-size: 11px;
    letter-spacing: .2em;
    font-weight: 700;
    white-space: nowrap;
  }

  /* ─── S4 Proof ─── */
  .proof {
    background: var(--bg);
    padding: 120px 40px;
  }
  .proof-headline-row {
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: end;
    gap: 24px;
    margin-bottom: 56px;
  }
  .proof-headline-row .h2 { margin: 0; }
  .proof-headline-row h2 .navy { color: var(--navy); }
  .proof-asof {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .2em;
    color: var(--muted);
    padding-bottom: 8px;
  }
  .stats {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0;
    border-top: 1px solid var(--navy-deep);
    border-bottom: 1px solid var(--navy-deep);
    background: #fff;
  }
  .stat {
    padding: 24px 18px;
    border-right: 1px solid var(--line);
    display: flex;
    flex-direction: column;
    min-height: 200px;
    min-width: 0;
  }
  .stat:last-child { border-right: none; }
  .stat .note {
    font-family: var(--f-mono);
    font-size: 9px;
    letter-spacing: .2em;
    color: var(--muted);
    margin-bottom: auto;
  }
  .stat .num {
    font-family: var(--f-display);
    font-size: clamp(32px, 3.4vw, 48px);
    font-weight: 700;
    line-height: 1.05;
    letter-spacing: -.02em;
    color: var(--navy-deep);
    margin-top: 16px;
    font-feature-settings: "tnum";
    display: flex;
    align-items: baseline;
    flex-wrap: wrap;
    gap: 4px;
  }
  .stat .num .unit {
    font-size: .34em;
    color: var(--muted);
    font-weight: 500;
    letter-spacing: 0;
  }
  .stat .label {
    font-family: var(--f-sans);
    font-size: 12px;
    color: var(--ink);
    margin-top: 12px;
    font-weight: 500;
    line-height: 1.5;
  }

  .network {
    margin-top: 64px;
    padding: 32px 40px;
    background: #fff;
    border: 1px solid var(--line);
    display: grid;
    grid-template-columns: auto 1fr;
    align-items: center;
    gap: 32px;
  }
  .network-label {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .22em;
    color: var(--gold);
    font-weight: 700;
    margin-bottom: 6px;
  }
  .network-title {
    font-family: var(--f-sans);
    font-size: 18px;
    font-weight: 700;
    color: var(--navy-deep);
  }
  .network-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  .network-tag {
    padding: 8px 14px;
    border: 1px solid var(--line);
    font-family: var(--f-sans);
    font-size: 12px;
    color: var(--ink);
    font-weight: 500;
  }
  .network-tag-more {
    color: var(--muted);
    border-style: dashed;
    background: transparent;
    font-style: italic;
  }

  /* ─── S5 Matrix ─── */
  .matrix {
    background: var(--bg-deep);
    padding: 120px 40px;
  }
  .risk-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    margin-top: 40px;
  }
  .risk-card {
    background: #fff;
    border: 1px solid var(--line);
    position: relative;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    transition: transform .25s cubic-bezier(.2, .7, .3, 1), box-shadow .25s;
  }
  .risk-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 16px 40px rgba(11, 35, 65, .1);
  }
  .risk-card::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 4px;
    height: 64px;
    background: var(--gold);
  }
  .risk-num {
    position: absolute;
    top: 18px;
    right: 28px;
    font-family: var(--f-display);
    font-size: 64px;
    font-weight: 700;
    color: rgba(11, 35, 65, .06);
    line-height: 1;
    letter-spacing: -.02em;
    pointer-events: none;
  }
  .risk-card-body {
    padding: 36px 32px 28px;
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }
  .risk-block {
    display: flex;
    flex-direction: column;
  }
  .risk-label {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .22em;
    font-weight: 700;
    margin-bottom: 8px;
  }
  .risk-label.muted { color: var(--muted); }
  .risk-label.gold { color: var(--gold); }
  .risk-text {
    font-family: var(--f-sans);
    font-size: 18px;
    font-weight: 700;
    line-height: 1.55;
    color: var(--navy-deep);
  }
  .risk-block.sol .risk-text { font-weight: 600; }
  .risk-arrow {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    border: 1px solid var(--gold);
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--gold);
  }
  .risk-arrow svg { width: 14px; height: 14px; }
  .risk-evi {
    background: var(--navy-deep);
    color: #fff;
    padding: 18px 32px 18px 36px;
    display: flex;
    align-items: center;
    gap: 16px;
    position: relative;
  }
  .risk-evi::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    width: 4px;
    background: var(--gold);
  }
  .risk-evi-label {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .22em;
    color: var(--gold);
    font-weight: 700;
    white-space: nowrap;
  }
  .risk-evi-text {
    font-family: var(--f-sans);
    font-size: 14px;
    font-weight: 600;
    color: #fff;
    flex: 1;
    line-height: 1.5;
  }

  /* ─── S6 Flow ─── */
  .flow {
    background: var(--bg);
    padding: 120px 40px;
  }
  .flow-grid {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    gap: 14px;
    margin-top: 64px;
    position: relative;
  }
  .flow-rail {
    position: absolute;
    top: 92px;
    left: calc(10% + 8px);
    right: calc(10% + 8px);
    height: 0;
    border-top: 2px dashed var(--gold);
    opacity: .35;
    pointer-events: none;
    z-index: 0;
  }
  .flow-step {
    background: #fff;
    border: 1px solid var(--line);
    padding: 30px 18px 26px;
    position: relative;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: transform .25s cubic-bezier(.2, .7, .3, 1), border-color .25s, box-shadow .25s;
    z-index: 1;
  }
  .flow-step:hover {
    transform: translateY(-6px);
    border-color: var(--gold);
    box-shadow: 0 16px 36px rgba(11, 35, 65, .08);
  }
  .flow-step.start, .flow-step.finale {
    border-color: var(--gold);
    box-shadow: 0 8px 24px rgba(201, 168, 106, .12);
  }
  .flow-badge {
    position: absolute;
    top: -11px;
    left: 50%;
    transform: translateX(-50%);
    padding: 4px 12px;
    background: var(--navy-deep);
    color: var(--gold);
    font-family: var(--f-mono);
    font-size: 9px;
    letter-spacing: .22em;
    font-weight: 700;
    white-space: nowrap;
    z-index: 2;
  }
  .flow-badge.gold {
    background: linear-gradient(180deg, var(--gold-hi) 0%, var(--gold) 100%);
    color: var(--navy-deep);
  }
  .flow-num {
    width: 72px;
    height: 72px;
    border-radius: 50%;
    background: #fff;
    border: 2px solid var(--line);
    color: var(--navy-deep);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: var(--f-display);
    font-weight: 700;
    font-size: 24px;
    margin-bottom: 16px;
    position: relative;
  }
  .flow-step.start .flow-num,
  .flow-step.finale .flow-num {
    background: linear-gradient(180deg, var(--gold-hi) 0%, var(--gold) 100%);
    border-color: var(--gold);
    color: var(--navy-deep);
    box-shadow: 0 8px 22px rgba(201, 168, 106, .35), inset 0 1px 0 rgba(255, 255, 255, .4);
  }
  .flow-meta {
    font-family: var(--f-mono);
    font-size: 9px;
    letter-spacing: .26em;
    color: var(--gold);
    font-weight: 700;
    margin-bottom: 10px;
  }
  .flow-sub {
    font-family: var(--f-mono);
    font-size: 9px;
    letter-spacing: .2em;
    color: var(--muted);
    margin-bottom: 6px;
    font-weight: 700;
  }
  .flow-title {
    font-family: var(--f-sans);
    font-size: 15px;
    font-weight: 700;
    color: var(--navy-deep);
    margin-bottom: 10px;
    line-height: 1.5;
  }
  .flow-desc {
    font-size: 11px;
    line-height: 1.75;
    color: var(--muted);
  }
  .flow-cta {
    margin-top: 56px;
    display: flex;
    justify-content: center;
  }

  /* ─── S7 Overseas ─── */
  .overseas {
    background: var(--bg-deep);
    padding: 80px 40px;
  }
  .overseas-card {
    max-width: 1120px;
    margin: 0 auto;
    background: #2A2F38;
    color: #fff;
    padding: 48px 56px;
    position: relative;
    overflow: hidden;
    display: grid;
    grid-template-columns: 1.1fr .9fr;
    gap: 48px;
    align-items: center;
  }
  .overseas-stripes {
    position: absolute;
    inset: 0;
    opacity: .08;
    background: repeating-linear-gradient(135deg, #fff 0 1px, transparent 1px 12px);
    pointer-events: none;
  }
  .overseas-text { position: relative; }
  .overseas-tag {
    display: inline-block;
    padding: 6px 12px;
    background: rgba(255, 255, 255, .1);
    border: 1px solid rgba(255, 255, 255, .2);
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .22em;
    color: rgba(255, 255, 255, .75);
    margin-bottom: 20px;
  }
  .overseas h2 {
    font-family: var(--f-sans);
    font-size: 34px;
    line-height: 1.3;
    font-weight: 700;
    margin: 0 0 14px;
  }
  .overseas h2 .gold { color: var(--gold); }
  .overseas-text p {
    font-size: 13px;
    line-height: 1.8;
    color: rgba(255, 255, 255, .6);
    margin: 0;
  }

  .overseas-form {
    position: relative;
  }
  .overseas-form-label {
    font-family: var(--f-sans);
    font-size: 13px;
    color: rgba(255, 255, 255, .9);
    margin-bottom: 12px;
    font-weight: 600;
  }
  .overseas-form-row {
    display: flex;
    gap: 8px;
  }
  .overseas-form input[type="email"] {
    flex: 1;
    height: 48px;
    padding: 0 16px;
    background: rgba(255, 255, 255, .08);
    border: 1px solid rgba(255, 255, 255, .2);
    color: #fff;
    font-size: 14px;
    font-family: var(--f-sans);
    outline: none;
  }
  .overseas-form button {
    height: 48px;
    padding: 0 20px;
    background: var(--gold);
    color: var(--navy-deep);
    border: none;
    font-family: var(--f-sans);
    font-weight: 700;
    font-size: 13px;
    letter-spacing: .05em;
    cursor: pointer;
    white-space: nowrap;
  }
  .overseas-success {
    padding: 16px;
    border: 1px solid var(--gold);
    background: rgba(201, 168, 106, .1);
    color: var(--gold);
    font-size: 13px;
  }

  /* ─── S8 FAQ ─── */
  .faq {
    background: var(--bg);
    padding: 120px 40px;
  }
  .faq .container { max-width: 880px; }
  .faq-list {
    margin-top: 40px;
    border-top: 1px solid var(--navy-deep);
  }
  .faq-item { border-bottom: 1px solid var(--line); }
  .faq-q {
    width: 100%;
    text-align: left;
    padding: 24px 8px;
    background: transparent;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: flex-start;
    gap: 20px;
    font-family: var(--f-sans);
  }
  .faq-q .qno {
    font-family: var(--f-mono);
    font-size: 14px;
    color: var(--gold);
    font-weight: 700;
    min-width: 28px;
  }
  .faq-q .qtext {
    flex: 1;
    font-size: 15px;
    font-weight: 600;
    color: var(--navy-deep);
    line-height: 1.5;
  }
  .faq-q .icon {
    width: 20px;
    height: 20px;
    position: relative;
    flex-shrink: 0;
    margin-top: 4px;
  }
  .faq-q .icon::before, .faq-q .icon::after {
    content: '';
    position: absolute;
    background: var(--navy-deep);
  }
  .faq-q .icon::before {
    top: 50%;
    left: 0;
    right: 0;
    height: 1px;
  }
  .faq-q .icon::after {
    top: 0;
    bottom: 0;
    left: 50%;
    width: 1px;
    transition: transform .2s;
  }
  .faq-item.open .faq-q .icon::after { transform: scaleY(0); }
  .faq-a {
    overflow: hidden;
    max-height: 0;
    transition: max-height .3s ease;
  }
  .faq-item.open .faq-a { max-height: 400px; }
  .faq-a-inner {
    padding: 0 40px 28px 48px;
    font-size: 13px;
    line-height: 1.9;
    color: var(--muted);
  }

  /* ─── S9 Form ─── */
  .form-section {
    background: var(--navy-deep);
    padding: 120px 40px;
    position: relative;
    overflow: hidden;
  }
  .form-section::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--gold) 50%, transparent);
  }
  .form-section .container { max-width: 880px; position: relative; }
  .form-lead {
    text-align: center;
    font-size: 14px;
    color: rgba(255, 255, 255, .7);
    margin: -16px 0 48px;
  }
  .form-card {
    background: rgba(255, 255, 255, .02);
    border: 1px solid rgba(255, 255, 255, .1);
    padding: 40px;
  }
  .form-row-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  .field { margin-bottom: 20px; }
  .field label {
    display: block;
    font-family: var(--f-sans);
    font-size: 12px;
    color: #fff;
    margin-bottom: 8px;
    font-weight: 600;
  }
  .field .req {
    color: var(--gold);
    margin-left: 6px;
    font-size: 10px;
  }
  .field input, .field textarea {
    width: 100%;
    padding: 0 14px;
    background: rgba(255, 255, 255, .06);
    border: 1px solid rgba(255, 255, 255, .2);
    color: #fff;
    font-family: var(--f-sans);
    font-size: 14px;
    outline: none;
  }
  .field input { height: 48px; }
  .field textarea {
    padding: 12px 14px;
    resize: vertical;
    min-height: 96px;
  }
  .field.error input, .field.error textarea { border-color: #E57373; }
  .field-error {
    margin-top: 6px;
    font-size: 11px;
    color: #E57373;
  }
  .agree-row {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    margin: 12px 0 24px;
    cursor: pointer;
  }
  .agree-row input { margin-top: 3px; accent-color: var(--gold); width: auto; height: auto; }
  .agree-row span {
    font-size: 12px;
    color: rgba(255, 255, 255, .7);
    line-height: 1.6;
  }
  .agree-row.error span { color: #E57373; }
  .agree-row a {
    color: var(--gold);
    text-decoration: underline;
  }
  .submit-btn {
    width: 100%;
    height: 60px;
    background: linear-gradient(180deg, var(--gold-hi) 0%, var(--gold) 100%);
    color: var(--navy-deep);
    border: none;
    font-family: var(--f-sans);
    font-weight: 700;
    font-size: 15px;
    letter-spacing: .05em;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    box-shadow: 0 8px 32px rgba(201, 168, 106, .3);
  }
  .submit-note {
    margin-top: 16px;
    text-align: center;
    font-size: 11px;
    color: rgba(255, 255, 255, .4);
    font-family: var(--f-mono);
    letter-spacing: .1em;
  }
  .form-success {
    text-align: center;
    padding: 48px;
    border: 1px solid var(--gold);
    background: rgba(201, 168, 106, .06);
  }
  .form-success .check { font-size: 32px; color: var(--gold); margin-bottom: 16px; }
  .form-success .ttl {
    font-family: var(--f-sans);
    font-size: 20px;
    font-weight: 700;
    color: #fff;
    margin-bottom: 10px;
  }
  .form-success .desc {
    font-size: 13px;
    color: rgba(255, 255, 255, .7);
    line-height: 1.8;
  }

  /* ─── Footer ─── */
  .footer {
    background: #060F1F;
    color: rgba(255, 255, 255, .55);
    padding: 56px 40px;
    font-family: var(--f-sans);
    font-size: 12px;
  }
  .footer-grid {
    display: grid;
    grid-template-columns: 1.2fr 1fr 1fr;
    gap: 32px;
    padding-bottom: 32px;
    border-bottom: 1px solid rgba(255, 255, 255, .1);
  }
  .footer-grid p {
    margin-top: 16px;
    line-height: 1.8;
    font-size: 11px;
  }
  .footer-col-label {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .2em;
    color: rgba(255, 255, 255, .4);
    margin-bottom: 12px;
  }
  .footer-col ul {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }
  .footer-col a { text-decoration: none; }
  .footer-meta {
    padding-top: 24px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 12px;
    font-size: 10px;
    font-family: var(--f-mono);
    letter-spacing: .1em;
    color: rgba(255, 255, 255, .3);
  }

  /* ─── Floating CTA ─── */
  .float-cta {
    position: fixed;
    bottom: 20px;
    right: 24px;
    z-index: 30;
    transform: translateY(120px);
    opacity: 0;
    transition: transform .35s cubic-bezier(.2, .8, .3, 1), opacity .35s;
    pointer-events: none;
  }
  .float-cta.show {
    transform: translateY(0);
    opacity: 1;
    pointer-events: auto;
  }
  .float-cta a {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 16px 24px;
    background: var(--gold);
    color: var(--navy-deep);
    font-family: var(--f-sans);
    font-weight: 700;
    font-size: 13px;
    letter-spacing: .05em;
    text-decoration: none;
    box-shadow: 0 12px 32px rgba(201, 168, 106, .4), 0 0 0 1px rgba(255, 255, 255, .3) inset;
    justify-content: center;
  }
  .float-cta .pulse-dot {
    width: 8px;
    height: 8px;
    background: var(--navy-deep);
    border-radius: 50%;
    animation: pulse 2s infinite;
  }

  /* ─── S2 Concept ─── */
  .concept {
    background: var(--bg);
    padding: 120px 40px;
    position: relative;
    overflow: hidden;
  }
  .concept::before {
    content: '';
    position: absolute;
    top: 0;
    left: 50%;
    width: 1px;
    height: 56px;
    background: var(--teal);
    opacity: .5;
  }
  .concept-headline-row {
    display: grid;
    grid-template-columns: 1.25fr .75fr;
    gap: 64px;
    align-items: end;
    margin: 8px 0 72px;
  }
  .concept-headline-row .h2 { margin: 0; }
  .concept-gold {
    position: relative;
    color: var(--teal);
    padding: 0 .04em;
  }
  .concept-gold::after {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    bottom: -6px;
    height: 4px;
    background: linear-gradient(90deg, var(--teal) 0%, transparent 100%);
    opacity: .4;
  }
  .concept-lead-tag {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .22em;
    color: var(--teal);
    margin-bottom: 12px;
    font-weight: 700;
  }
  .concept-lead p {
    font-family: var(--f-sans);
    font-size: 14px;
    line-height: 1.95;
    color: var(--ink);
    margin: 0;
    font-weight: 500;
  }
  .concept-lead p .em {
    color: var(--teal);
    font-weight: 700;
  }

  .bridges {
    background: #fff;
    border-top: 1px solid var(--navy-deep);
    border-bottom: 1px solid var(--navy-deep);
  }
  .bridge-row {
    display: grid;
    grid-template-columns: 1fr 1.3fr 1fr;
    align-items: center;
    padding: 36px 40px;
    border-bottom: 1px solid var(--line);
    gap: 32px;
  }
  .bridge-row:last-child { border-bottom: none; }
  .bridge-row.future { background: rgba(11, 35, 65, .02); }
  .bridge-side-label {
    font-family: var(--f-mono);
    font-size: 10px;
    letter-spacing: .2em;
    color: var(--muted);
    margin-bottom: 8px;
    font-weight: 700;
  }
  .bridge-side-text {
    font-family: var(--f-sans);
    font-size: 16px;
    font-weight: 600;
    color: var(--navy-deep);
    line-height: 1.55;
  }
  .bridge-side-text .accent { color: var(--teal); }
  .bridge-from { text-align: right; }
  .bridge-to { text-align: left; }
  .bridge-mid {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    color: var(--teal);
  }
  .bridge-mid.muted { color: var(--muted); opacity: .55; }
  .bridge-arc {
    width: 100%;
    max-width: 220px;
    height: auto;
    display: block;
  }
  .bridge-mid-label {
    font-family: var(--f-mono);
    font-size: 11px;
    letter-spacing: .22em;
    font-weight: 700;
    color: inherit;
  }
  .bridge-mid-sub {
    font-family: var(--f-mono);
    font-size: 8px;
    letter-spacing: .22em;
    color: var(--muted);
    margin-top: -4px;
  }

  .concept-closing {
    margin-top: 56px;
    padding-top: 40px;
    border-top: 1px solid var(--line);
    text-align: center;
    font-family: var(--f-sans);
    font-size: 18px;
    font-weight: 700;
    color: var(--navy-deep);
    letter-spacing: .04em;
    line-height: 1.6;
  }
  .concept-closing .gold {
    color: var(--teal);
  }
  .concept-closing-mark {
    display: inline-block;
    color: var(--teal);
    margin-right: 12px;
    letter-spacing: 0;
  }

  /* ─── SP (< 768px) ─── */
  @media (max-width: 767px) {
    .header { padding: 0 16px; gap: 8px; }
    .header-nav { display: none; }
    .header-actions { gap: 8px; }
    .logo-mark { width: 30px; height: 30px; }
    .logo-name { font-size: 12px; letter-spacing: .08em; }
    .logo-sub { font-size: 7px; }

    .hero { min-height: 640px; }
    .hero-inner {
      grid-template-columns: 1fr;
      gap: 0;
      padding: 48px 20px 80px;
      min-height: 640px;
    }
    .hero-text { text-align: center; }
    .hero-badge { font-size: 10px; margin-bottom: 24px; }
    .hero h1 { font-size: 38px; }
    .hero-lead { font-size: 16px; margin-left: auto; margin-right: auto; }
    .hero-sub { font-size: 13px; margin-left: auto; margin-right: auto; }
    .hero-cta { justify-content: center; flex-direction: column; margin-bottom: 28px; }
    .hero-promise { max-width: none; padding: 14px 16px; }
    .hero-promise-text { font-size: 14px; }
    .hero-img-wrap { display: none; }

    .concept { padding: 64px 20px; }
    .concept-headline-row {
      grid-template-columns: 1fr;
      gap: 24px;
      margin-bottom: 40px;
    }
    .bridge-row {
      grid-template-columns: 1fr;
      padding: 24px 20px;
      gap: 12px;
      text-align: center;
    }
    .bridge-from, .bridge-to { text-align: center; }
    .bridge-from { order: 1; }
    .bridge-mid { order: 2; }
    .bridge-to { order: 3; }
    .bridge-arc { max-width: 180px; }
    .concept-closing { font-size: 15px; margin-top: 32px; padding-top: 28px; }

    .problems { padding: 64px 20px; }
    .problems-grid { grid-template-columns: 1fr; gap: 16px; }

    .about { padding: 64px 20px; }
    .about-headline-row { margin-bottom: 40px; }
    .about-headline-row h2 { font-size: 30px; line-height: 1.4; margin-bottom: 28px; }
    .about-desc { font-size: 14px; padding-left: 18px; }
    .pillars { grid-template-columns: 1fr; border-left: none; }
    .pillar { border-right: none; }
    .deploy-box { grid-template-columns: 1fr; padding: 24px; }
    .deploy-headline { font-size: 18px; line-height: 1.6; }
    .deploy-period { display: inline-block; }

    .proof { padding: 64px 20px; }
    .proof-headline-row { grid-template-columns: 1fr; }
    .stats { grid-template-columns: repeat(2, 1fr); }
    .stat {
      padding: 20px;
      min-height: 140px;
      border-right: none;
      border-bottom: 1px solid var(--line);
    }
    .stat:nth-child(odd) { border-right: 1px solid var(--line); }
    .stat:nth-child(3), .stat:nth-child(4) { border-bottom: none; }
    .stat .num { font-size: 36px; }
    .network {
      margin-top: 40px;
      padding: 20px;
      grid-template-columns: 1fr;
    }

    .matrix { padding: 64px 20px; }
    .risk-grid { grid-template-columns: 1fr; gap: 14px; margin-top: 32px; }
    .risk-card-body { padding: 28px 20px 20px; gap: 12px; }
    .risk-num { font-size: 48px; top: 14px; right: 20px; }
    .risk-text { font-size: 16px; }
    .risk-arrow { width: 28px; height: 28px; }
    .risk-evi { padding: 14px 20px 14px 24px; gap: 12px; }
    .risk-evi-text { font-size: 13px; }

    .flow { padding: 64px 20px; }
    .flow-grid {
      grid-template-columns: 1fr;
      gap: 14px;
      margin-top: 48px;
    }
    .flow-rail { display: none; }
    .flow-step {
      padding: 22px 22px 22px 26px;
      flex-direction: row;
      align-items: center;
      gap: 18px;
      text-align: left;
    }
    .flow-step .flow-num { width: 56px; height: 56px; font-size: 20px; margin-bottom: 0; flex-shrink: 0; }
    .flow-step-text {
      flex: 1;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
    }
    .flow-meta, .flow-sub, .flow-title, .flow-desc { text-align: left; }
    .flow-meta { margin-bottom: 4px; }
    .flow-sub { margin-bottom: 4px; }
    .flow-title { font-size: 15px; margin-bottom: 4px; }
    .flow-desc { font-size: 12px; line-height: 1.6; }
    .flow-badge { left: 26px; transform: none; top: -10px; }

    .overseas { padding: 48px 20px; }
    .overseas-card {
      grid-template-columns: 1fr;
      gap: 24px;
      padding: 28px;
    }
    .overseas h2 { font-size: 24px; }
    .overseas-form-row { flex-direction: column; }

    .faq { padding: 64px 20px; }
    .faq-q { padding: 20px 0; }
    .faq-q .qtext { font-size: 14px; }
    .faq-a-inner { padding: 0 0 20px 48px; }

    .form-section { padding: 64px 20px; }
    .form-card { padding: 24px; }
    .form-row-2 { grid-template-columns: 1fr; gap: 0; }

    .footer { padding: 40px 20px; }
    .footer-grid { grid-template-columns: 1fr; }

    .float-cta {
      right: 12px;
      left: 12px;
    }
    .float-cta a { padding: 14px 18px; width: 100%; }

    .scroll-hint { display: none; }

    .btn-lg.btn-full-sp { width: 100%; min-width: 0; padding: 12px 18px; font-size: 13px; height: 44px; }
    .btn-md.btn-full-sp { width: 100%; min-width: 0; }
  }
</style>
</head>
<body>

<!-- ─── HEADER ─── -->
<header class="header">
  <a href="#" class="logo">
    <img class="logo-mark" src="baybridge-mark.png" alt="BAYBRIDGE PROJECT" />
    <span class="logo-text">
      <span class="logo-name">BAYBRIDGE PROJECT</span>
      <span class="logo-sub">by BAYCOSMETICS</span>
    </span>
  </a>
  <div class="header-actions">
    <nav class="header-nav">
      <a href="#about">プロジェクト</a>
      <a href="#proof">実績</a>
      <a href="#flow">参加の流れ</a>
      <a href="#faq">FAQ</a>
    </nav>
    <a href="https://meetings-na2.hubspot.com/contact5" class="btn btn-md btn-gold header-cta">
      <span class="cta-pc">無料個別相談を申し込む</span>
      <span class="cta-sp">相談する</span>
    </a>
  </div>
</header>

<!-- ─── S1 HERO ─── -->
<section class="hero">
  <div class="hero-kv" id="heroKv">
    <div class="photo fill">
      <span class="label">[ KV — ドラッグストア化粧品棚（パララックス） ]</span>
    </div>
  </div>
  <div class="hero-overlay"></div>
  <div class="hero-glow"></div>

  <div class="hero-inner">
    <div class="hero-text">
      <div class="hero-badge">
        <span class="dot"></span>
        第1期 3〜5社限定
      </div>
      <h1>
        SNSで売れた。<br />
        次は<span class="gold-mark">全国棚</span>へ。
      </h1>

      <div class="hero-promise">
        <span class="hero-promise-label">OUR PROMISE</span>
        <span class="hero-promise-text">あなたのブランドを、<span class="hp-em">2026.10 〜 2027.04</span> までに、全国の棚へ。</span>
        <span class="hero-promise-note">※商品によって変動あり</span>
      </div>

      <div class="hero-cta">
        <a href="https://meetings-na2.hubspot.com/contact5" class="btn btn-lg btn-gold btn-full-sp">
          無料個別相談を申し込む
          <svg width="14" height="14" viewBox="0 0 24 24" fill="none"><path d="M5 12h14M13 5l7 7-7 7" stroke="currentColor" stroke-width="2"/></svg>
        </a>
      </div>
    </div>

    <div class="hero-img-wrap">
      <div class="hero-img-frame">
        <img class="hero-img" src="kv-hero2.jpg" alt="化粧品" />
        <span class="corner tl"></span>
        <span class="corner br"></span>
      </div>
      <div class="shelf-ready">SHELF · READY</div>
    </div>
  </div>

  <div class="scroll-hint">
    SCROLL
    <span class="line"></span>
  </div>
</section>

<!-- ─── S2 CONCEPT ─── -->
<section class="concept" id="concept">
  <div class="container">
    <div class="section-tag"><span class="num">01</span><span class="bar"></span><span>OUR NAME / THE BRIDGE</span></div>

    <div class="concept-headline-row">
      <h2 class="h2">
        BAYBRIDGE PROJECTとは、<br />
        ベイコスメティックスが架ける、<br />
        <span class="concept-gold">橋渡し</span>の名前です。
      </h2>
      <div class="concept-lead">
        <div class="concept-lead-tag">CONCEPT · 名前に込めた想い</div>
        <p>
          <span class="em">BAY</span>（ベイコスメティックス）+ <span class="em">BRIDGE</span>（橋渡し）。<br />
          私たちは、ブランドの「今」と、まだ見ぬ「新しい可能性」との間に、橋を架ける存在でありたい。それが、このプロジェクトの名前に込めた想いです。
        </p>
      </div>
    </div>

    <div class="bridges">
      <div class="bridge-row">
        <div class="bridge-from">
          <div class="bridge-side-label">FROM · 今のブランド</div>
          <div class="bridge-side-text">SNS · ECで愛される<br />D2Cブランド</div>
        </div>
        <div class="bridge-mid">
          <svg class="bridge-arc" viewBox="0 0 220 60" fill="none" aria-hidden="true">
            <line x1="0" y1="50" x2="220" y2="50" stroke="currentColor" stroke-width="0.5" stroke-dasharray="2 4" opacity="0.35" />
            <path d="M10 48 Q110 4, 210 48" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" />
            <line x1="44" y1="32" x2="44" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="78" y1="20" x2="78" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="110" y1="13" x2="110" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="142" y1="20" x2="142" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="176" y1="32" x2="176" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="10" y1="42" x2="10" y2="55" stroke="currentColor" stroke-width="1.6" />
            <line x1="210" y1="42" x2="210" y2="55" stroke="currentColor" stroke-width="1.6" />
          </svg>
          <div class="bridge-mid-label">BAYBRIDGE PROJECT</div>
          <div class="bridge-mid-sub">橋渡し</div>
        </div>
        <div class="bridge-to">
          <div class="bridge-side-label">TO · 新しい可能性</div>
          <div class="bridge-side-text">全国 <span class="accent">10,000店舗</span> の<br />ドラッグストアの棚へ</div>
        </div>
      </div>

      <div class="bridge-row">
        <div class="bridge-from">
          <div class="bridge-side-label">FROM · 今のブランド</div>
          <div class="bridge-side-text">EC・SNSで生まれた<br />初動の売上</div>
        </div>
        <div class="bridge-mid">
          <svg class="bridge-arc" viewBox="0 0 220 60" fill="none" aria-hidden="true">
            <line x1="0" y1="50" x2="220" y2="50" stroke="currentColor" stroke-width="0.5" stroke-dasharray="2 4" opacity="0.35" />
            <path d="M10 48 Q110 4, 210 48" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" />
            <line x1="44" y1="32" x2="44" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="78" y1="20" x2="78" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="110" y1="13" x2="110" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="142" y1="20" x2="142" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="176" y1="32" x2="176" y2="48" stroke="currentColor" stroke-width="0.8" />
            <line x1="10" y1="42" x2="10" y2="55" stroke="currentColor" stroke-width="1.6" />
            <line x1="210" y1="42" x2="210" y2="55" stroke="currentColor" stroke-width="1.6" />
          </svg>
          <div class="bridge-mid-label">BAYBRIDGE PROJECT</div>
          <div class="bridge-mid-sub">橋渡し</div>
        </div>
        <div class="bridge-to">
          <div class="bridge-side-label">TO · 新しい可能性</div>
          <div class="bridge-side-text">リアル店舗での<br /><span class="accent">確かな存在感</span></div>
        </div>
      </div>

    </div>

    <div class="concept-closing">
      <span class="concept-closing-mark">─</span>
      ベイコスメが架ける<span class="gold">橋渡し</span>を、あなたのブランドにも。
    </div>
  </div>
</section>

<!-- ─── S3 PROBLEMS ─── -->
<section class="problems">
  <div class="container">
    <div class="section-tag"><span class="num">02</span><span class="bar"></span><span>PAIN POINTS</span></div>
    <h2 class="h2">こんなお悩み、<br />ありませんか？</h2>

    <div class="problems-grid">
      <div class="problem-card js-fadeup">
        <div class="pain-no">PAIN · 01</div>
        <svg viewBox="0 0 48 48" width="48" height="48" fill="none" stroke="#071935" stroke-width="1.25">
          <path d="M6 24h10l4-4 4 2 4-2 4 4h10"/>
          <path d="M18 22l4 4 4-4 4 4"/>
          <circle cx="12" cy="18" r="3"/>
          <circle cx="36" cy="18" r="3"/>
          <g stroke="#C9A86A" stroke-width="2">
            <line x1="34" y1="8" x2="44" y2="18"/>
            <line x1="44" y1="8" x2="34" y2="18"/>
          </g>
        </svg>
        <p>バイヤーとのコネクションがなく、どこに連絡すれば良いか分からない。</p>
        <div class="tag">コネクション</div>
      </div>
      <div class="problem-card js-fadeup">
        <div class="pain-no">PAIN · 02</div>
        <svg viewBox="0 0 48 48" width="48" height="48" fill="none" stroke="#071935" stroke-width="1.25">
          <rect x="6" y="10" width="36" height="32"/>
          <line x1="6" y1="20" x2="42" y2="20"/>
          <line x1="6" y1="30" x2="42" y2="30"/>
          <rect x="10" y="12" width="4" height="7"/>
          <rect x="18" y="22" width="4" height="7"/>
          <rect x="28" y="12" width="4" height="7"/>
          <rect x="34" y="32" width="4" height="9"/>
          <g stroke="#C9A86A" stroke-width="2">
            <line x1="34" y1="8" x2="44" y2="18"/>
            <line x1="44" y1="8" x2="34" y2="18"/>
          </g>
        </svg>
        <p>EC向けパッケージが店頭では映えないかもしれない、という不安がある。</p>
        <div class="tag">プロダクト</div>
      </div>
      <div class="problem-card js-fadeup">
        <div class="pain-no">PAIN · 03</div>
        <svg viewBox="0 0 48 48" width="48" height="48" fill="none" stroke="#071935" stroke-width="1.25">
          <path d="M8 18l16-8 16 8v20l-16 8-16-8z"/>
          <path d="M8 18l16 8 16-8"/>
          <line x1="24" y1="26" x2="24" y2="46"/>
          <g stroke="#C9A86A" stroke-width="2">
            <line x1="34" y1="8" x2="44" y2="18"/>
            <line x1="44" y1="8" x2="34" y2="18"/>
          </g>
        </svg>
        <p>初期ロットを抱えるのが怖く、リアル店舗参入に踏み切れない。</p>
        <div class="tag">リスク</div>
      </div>
    </div>
  </div>
</section>

<!-- ─── S3 ABOUT ─── -->
<section class="about" id="about">
  <div class="about-grid-bg"></div>
  <div class="about-inner">
    <div class="section-tag invert"><span class="num">03</span><span class="bar"></span><span>THE PROGRAM</span></div>

    <div class="industry-first">
      <span>★</span> 業界初
    </div>

    <div class="about-headline-row">
      <h2>
        リスクを最小化しながら、<br />
        <span class="gold">リアル市場へのデビュー</span>を<br />
        実現する唯一のOEMプログラム。
      </h2>
    </div>

    <div class="pillars">
      <div class="pillar">
        <div class="no">01</div>
        <div class="accent">NEGOTIATION</div>
        <h3>商談 · 全面代行</h3>
        <p>卸・バイヤーとの商談をベイコスメが全面代行。既存コネクションをそのまま提供します。</p>
      </div>
      <div class="pillar">
        <div class="no">02</div>
        <div class="accent">PRODUCT</div>
        <h3>店頭設計 · 最適化</h3>
        <p>店頭陳列・棚割りを想定した処方とパッケージ設計を支援。ECのままでは勝てない店頭へ。</p>
      </div>
      <div class="pillar">
        <div class="no">03</div>
        <div class="accent">RISK</div>
        <h3>ロット · リスク最小化</h3>
        <p>配架数量から逆算したロット設計で、在庫リスクと財務インパクトを最小化します。</p>
      </div>
    </div>

    <div class="deploy-box">
      <div>
        <div class="deploy-label">DELIVERY PROMISE</div>
        <div class="deploy-headline">あなたのブランドを、<span class="deploy-period">2026.10 〜 2027.04</span> までに、全国の棚へ。</div>
        <div class="deploy-note">※商品によって変動あり</div>
      </div>
      <div class="deploy-tag">第1期 3〜5社限定 · 濃厚支援モデル</div>
    </div>
  </div>
</section>

<!-- ─── S4 PROOF ─── -->
<section class="proof" id="proof">
  <div class="container">
    <div class="section-tag"><span class="num">04</span><span class="bar"></span><span>WHY BAYCOSMETICS</span></div>

    <div class="proof-headline-row">
      <h2 class="h2">
        机上の空論ではなく、<br />
        <span class="navy">自分たちが実際に売ってきた。</span>
      </h2>
      <div class="proof-asof">AS OF 2026.04</div>
    </div>

    <div class="stats">
      <div class="stat">
        <div class="note">Brand Placement</div>
        <div class="num">10,000<span class="unit">店舗</span></div>
        <div class="label">自社ブランド配架</div>
      </div>
      <div class="stat">
        <div class="note">Owned Formulations</div>
        <div class="num">1,000<span class="unit">以上</span></div>
        <div class="label">自社保有処方数</div>
      </div>
      <div class="stat">
        <div class="note">Brands Launched</div>
        <div class="num">200+<span class="unit">ブランド</span></div>
        <div class="label">立ち上げ支援</div>
      </div>
      <div class="stat">
        <div class="note">Min. Lot</div>
        <div class="num">3,000〜<span class="unit">本</span></div>
        <div class="label">最小ロット / リードタイム -3ヶ月</div>
      </div>
    </div>

    <div class="network">
      <div>
        <div class="network-label">DISTRIBUTION NETWORK</div>
        <div class="network-title">卸 · バイヤーネットワーク</div>
      </div>
      <div class="network-tags">
        <div class="network-tag">ドンキホーテ様</div>
        <div class="network-tag">ロフト様</div>
        <div class="network-tag">マツモトキヨシ様</div>
        <div class="network-tag">ツルハ様</div>
        <div class="network-tag">スギ薬局様</div>
        <div class="network-tag network-tag-more">など</div>
      </div>
    </div>
  </div>
</section>

<!-- ─── S5 MATRIX ─── -->
<section class="matrix">
  <div class="container">
    <div class="section-tag"><span class="num">05</span><span class="bar"></span><span>RISK / SOLUTION</span></div>
    <h2 class="h2">あなたの不安は、<br />全部こちらで引き受けます。</h2>

    <div class="risk-grid">
      <div class="risk-card">
        <div class="risk-num">01</div>
        <div class="risk-card-body">
          <div class="risk-block">
            <div class="risk-label muted">不安 · PAIN</div>
            <div class="risk-text">バイヤー接点なし</div>
          </div>
          <div class="risk-arrow">
            <svg viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M12 5v14M6 13l6 6 6-6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </div>
          <div class="risk-block sol">
            <div class="risk-label gold">解決 · SOLUTION</div>
            <div class="risk-text">卸・バイヤー商談を全面代行</div>
          </div>
        </div>
        <div class="risk-evi">
          <div class="risk-evi-label">EVIDENCE</div>
          <div class="risk-evi-text">全国 10,000店舗 配架実績</div>
        </div>
      </div>

      <div class="risk-card">
        <div class="risk-num">02</div>
        <div class="risk-card-body">
          <div class="risk-block">
            <div class="risk-label muted">不安 · PAIN</div>
            <div class="risk-text">店頭向け処方 · パッケージ知見なし</div>
          </div>
          <div class="risk-arrow">
            <svg viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M12 5v14M6 13l6 6 6-6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </div>
          <div class="risk-block sol">
            <div class="risk-label gold">解決 · SOLUTION</div>
            <div class="risk-text">店頭想定の商品設計支援</div>
          </div>
        </div>
        <div class="risk-evi">
          <div class="risk-evi-label">EVIDENCE</div>
          <div class="risk-evi-text">200ブランド 立ち上げ経験</div>
        </div>
      </div>

      <div class="risk-card">
        <div class="risk-num">03</div>
        <div class="risk-card-body">
          <div class="risk-block">
            <div class="risk-label muted">不安 · PAIN</div>
            <div class="risk-text">初期ロット・在庫リスク</div>
          </div>
          <div class="risk-arrow">
            <svg viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M12 5v14M6 13l6 6 6-6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </div>
          <div class="risk-block sol">
            <div class="risk-label gold">解決 · SOLUTION</div>
            <div class="risk-text">配架数量逆算のロット設計</div>
          </div>
        </div>
        <div class="risk-evi">
          <div class="risk-evi-label">EVIDENCE</div>
          <div class="risk-evi-text">3,000本〜 / リードタイム -3ヶ月</div>
        </div>
      </div>

      <div class="risk-card">
        <div class="risk-num">04</div>
        <div class="risk-card-body">
          <div class="risk-block">
            <div class="risk-label muted">不安 · PAIN</div>
            <div class="risk-text">店頭映えへの不安</div>
          </div>
          <div class="risk-arrow">
            <svg viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M12 5v14M6 13l6 6 6-6" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </div>
          <div class="risk-block sol">
            <div class="risk-label gold">解決 · SOLUTION</div>
            <div class="risk-text">棚割り · POP · 販促まで一貫</div>
          </div>
        </div>
        <div class="risk-evi">
          <div class="risk-evi-label">EVIDENCE</div>
          <div class="risk-evi-text">電通出身マーケターの販促企画</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ─── S6 FLOW ─── -->
<section class="flow" id="flow">
  <div class="container">
    <div class="section-tag"><span class="num">06</span><span class="bar"></span><span>HOW IT WORKS</span></div>
    <h2 class="h2">参加までの、5ステップ。</h2>

    <div class="flow-grid">
      <div class="flow-rail"></div>

      <div class="flow-step start">
        <span class="flow-badge">START HERE</span>
        <div class="flow-num">01</div>
        <div class="flow-meta">STEP 01</div>
        <div class="flow-sub">ヒアリング</div>
        <div class="flow-title">無料個別相談</div>
        <div class="flow-desc">まずはここから。オンラインで60分、現状と目標をうかがいます。</div>
      </div>

      <div class="flow-step">
        <div class="flow-num">02</div>
        <div class="flow-meta">STEP 02</div>
        <div class="flow-sub">合意形成</div>
        <div class="flow-title">プロジェクト参加審査</div>
        <div class="flow-desc">方向性と座組みを合意。NDA締結の上で本格検討へ。</div>
      </div>

      <div class="flow-step">
        <div class="flow-num">03</div>
        <div class="flow-meta">STEP 03</div>
        <div class="flow-sub">店頭前提の設計</div>
        <div class="flow-title">商品開発 · 処方設計</div>
        <div class="flow-desc">店頭想定の処方・パッケージ・POPまでを同時設計。</div>
      </div>

      <div class="flow-step">
        <div class="flow-num">04</div>
        <div class="flow-meta">STEP 04</div>
        <div class="flow-sub">ベイコスメが代行</div>
        <div class="flow-title">バイヤー商談</div>
        <div class="flow-desc">全国DgSチェーンへ。商談交渉はすべて当社が担当。</div>
      </div>

      <div class="flow-step finale">
        <span class="flow-badge gold">GOAL</span>
        <div class="flow-num">05</div>
        <div class="flow-meta">STEP 05</div>
        <div class="flow-sub">市場デビュー</div>
        <div class="flow-title">ドラッグストア配架</div>
        <div class="flow-desc">2026.10〜2027.04 の間に全国棚デビュー。以降の運用も伴走。</div>
      </div>
    </div>

    <div class="flow-cta">
      <a href="https://meetings-na2.hubspot.com/contact5" class="btn btn-lg btn-gold btn-full-sp">
        無料個別相談を申し込む
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none"><path d="M5 12h14M13 5l7 7-7 7" stroke="currentColor" stroke-width="2"/></svg>
      </a>
    </div>
  </div>
</section>

<!-- ─── S7 FAQ ─── -->
<section class="faq" id="faq">
  <div class="container">
    <div class="section-tag"><span class="num">07</span><span class="bar"></span><span>FAQ</span></div>
    <h2 class="h2">よくあるご質問。</h2>

    <div class="faq-list" id="faqList">
      <div class="faq-item">
        <button class="faq-q" type="button">
          <span class="qno">Q01</span>
          <span class="qtext">参加費用はかかりますか？</span>
          <span class="icon"></span>
        </button>
        <div class="faq-a"><div class="faq-a-inner">初期費用は無料です。採択後、商品開発とOEM製造の段階で通常のOEM発注費用が発生します。詳細は個別相談にてご案内します。</div></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" type="button">
          <span class="qno">Q02</span>
          <span class="qtext">OEM発注は必須ですか？</span>
          <span class="icon"></span>
        </button>
        <div class="faq-a"><div class="faq-a-inner">はい、本プログラムは弊社工場でのOEM製造が前提です。既存処方の移管も含め、柔軟にご相談いただけます。</div></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" type="button">
          <span class="qno">Q03</span>
          <span class="qtext">最低ロット数はいくつですか？</span>
          <span class="icon"></span>
        </button>
        <div class="faq-a"><div class="faq-a-inner">3,000本〜のスモールロットで対応可能です。配架店舗数から逆算したロット設計を行います。</div></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" type="button">
          <span class="qno">Q04</span>
          <span class="qtext">配架は保証されるのですか？</span>
          <span class="icon"></span>
        </button>
        <div class="faq-a"><div class="faq-a-inner">商談は全面代行しますが、最終的な採用判断はバイヤー側に委ねられます。過去の採択実績と採用率は個別相談でお伝えします。</div></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" type="button">
          <span class="qno">Q05</span>
          <span class="qtext">すでに他のOEM会社を使っていても参加できますか？</span>
          <span class="icon"></span>
        </button>
        <div class="faq-a"><div class="faq-a-inner">可能です。既存処方の継続使用、または店頭向けの別SKU開発など、ケースに応じて設計します。</div></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" type="button">
          <span class="qno">Q06</span>
          <span class="qtext">どのくらいの期間でドラッグストアに並びますか？</span>
          <span class="icon"></span>
        </button>
        <div class="faq-a"><div class="faq-a-inner">採択〜配架まで最短6ヶ月。標準リードタイムから3ヶ月の短縮を実現しています。</div></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" type="button">
          <span class="qno">Q07</span>
          <span class="qtext">競合ブランドと同時募集になる可能性は？</span>
          <span class="icon"></span>
        </button>
        <div class="faq-a"><div class="faq-a-inner">第1期は3〜5社限定、かつカテゴリ重複を避ける方針です。初動のご相談順を優先します。</div></div>
      </div>
      <div class="faq-item">
        <button class="faq-q" type="button">
          <span class="qno">Q08</span>
          <span class="qtext">守秘義務（処方・ブランド情報）はどう担保されますか？</span>
          <span class="icon"></span>
        </button>
        <div class="faq-a"><div class="faq-a-inner">審査フェーズ前にNDAを締結します。処方・顧客データは厳重に管理し、担当チームのみがアクセス可能な体制です。</div></div>
      </div>
    </div>
  </div>
</section>

<!-- ─── S9 FORM ─── -->
<section class="form-section" id="form">
  <div class="container">
    <div class="section-tag invert"><span class="num">08</span><span class="bar"></span><span>GET STARTED</span></div>
    <h2 class="h2 invert center">まずは、<span style="color: var(--gold);">無料個別相談</span>から。</h2>
    <p class="form-lead">第1期 3〜5社限定。ご相談は早めに。</p>

    <div id="formMount" class="form-card">
      <script src="https://js-na2.hsforms.net/forms/embed/242734872.js" defer></script>
      <div class="hs-form-frame" data-region="na2" data-form-id="0b901e78-a016-487b-a21b-9673dea6a049" data-portal-id="242734872"></div>
      <div class="submit-note">* 事務局より 48時間以内にフォローします</div>
    </div>
  </div>
</section>

<!-- ─── FOOTER ─── -->
<footer class="footer">
  <div class="container">
    <div class="footer-grid">
      <div>
        <a href="#" class="logo">
          <img class="logo-mark" src="baybridge-mark.png" alt="BAYBRIDGE PROJECT" />
          <span class="logo-text">
            <span class="logo-name" style="color: rgba(255,255,255,.85);">BAYBRIDGE PROJECT</span>
            <span class="logo-sub" style="color: rgba(255,255,255,.4);">by BAYCOSMETICS</span>
          </span>
        </a>
        <p>
          株式会社ベイコスメティックス<br />
          BAYBRIDGE PROJECT事務局<br />
          baybridge@baycosme.com
        </p>
      </div>
      <div class="footer-col">
        <div class="footer-col-label">COMPANY</div>
        <ul>
          <li><a href="#">会社情報</a></li>
          <li><a href="#">事業紹介</a></li>
          <li><a href="#">採用情報</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <div class="footer-col-label">LEGAL</div>
        <ul>
          <li><a href="#">プライバシーポリシー</a></li>
          <li><a href="#">特定商取引法</a></li>
          <li><a href="#">利用規約</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-meta">
      <span>© 2026 BAYCOSMETICS INC. ALL RIGHTS RESERVED.</span>
      <span>BAYBRIDGE PROJECT / DRUGSTORE OEM PROGRAM</span>
    </div>
  </div>
</footer>

<!-- ─── FLOATING CTA ─── -->
<div class="float-cta" id="floatCta">
  <a href="https://meetings-na2.hubspot.com/contact5">
    <span class="pulse-dot"></span>
    無料個別相談を申し込む
    <svg width="14" height="14" viewBox="0 0 24 24" fill="none"><path d="M5 12h14M13 5l7 7-7 7" stroke="currentColor" stroke-width="2"/></svg>
  </a>
</div>

<style>
  /* PC/SP出し分け（ヘッダーCTA・ロゴ） */
  .cta-sp { display: none; }
  @media (max-width: 767px) {
    .cta-pc { display: none; }
    .cta-sp { display: inline; }
    .header-cta { min-width: 0; padding: 8px 14px; font-size: 12px; height: 36px; }
  }
</style>

<script>
(function () {
  'use strict';

  // ─── Hero parallax ───
  const heroKv = document.getElementById('heroKv');
  const floatCta = document.getElementById('floatCta');
  let ticking = false;
  function onScroll() {
    if (ticking) return;
    ticking = true;
    requestAnimationFrame(() => {
      const y = window.scrollY || window.pageYOffset || 0;
      heroKv.style.transform = `translateY(${y * 0.3}px) scale(1.05)`;
      if (y > 600) floatCta.classList.add('show');
      else floatCta.classList.remove('show');
      ticking = false;
    });
  }
  window.addEventListener('scroll', onScroll, { passive: true });
  onScroll();

  // ─── Fade-up on view ───
  if ('IntersectionObserver' in window) {
    const io = new IntersectionObserver((entries) => {
      entries.forEach((e) => {
        if (e.isIntersecting) {
          e.target.classList.add('in-view');
          io.unobserve(e.target);
        }
      });
    }, { threshold: 0.15 });
    document.querySelectorAll('.js-fadeup').forEach((el) => io.observe(el));
  } else {
    document.querySelectorAll('.js-fadeup').forEach((el) => el.classList.add('in-view'));
  }

  // ─── FAQ accordion ───
  document.querySelectorAll('#faqList .faq-q').forEach((btn) => {
    btn.addEventListener('click', () => {
      const item = btn.closest('.faq-item');
      const wasOpen = item.classList.contains('open');
      document.querySelectorAll('#faqList .faq-item').forEach((it) => it.classList.remove('open'));
      if (!wasOpen) item.classList.add('open');
    });
  });

})();
</script>
</body>
</html>
