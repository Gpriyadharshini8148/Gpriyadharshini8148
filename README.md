<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Priyadharshini G — GitHub Profile README v2</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;600&family=Playfair+Display:ital,wght@0,700;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #070B14;
    --surface: #0D1120;
    --surface2: #131829;
    --surface3: #1A2035;
    --border: #1E2640;
    --border2: #263050;
    --accent: #4F8EF7;        /* electric blue – backend primary */
    --accent2: #2FFFB4;       /* neon mint – secondary */
    --accent3: #FF6B6B;       /* coral – ML/AI */
    --accent4: #FFD93D;       /* gold – highlights */
    --text: #EEF0F8;
    --muted: #7B849E;
    --faint: #3A4060;
    --backend-glow: rgba(79,142,247,0.15);
    --ml-glow: rgba(255,107,107,0.12);
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Grotesk', sans-serif;
    min-height: 100vh;
    padding: 2rem 1.5rem 4rem;
    position: relative;
    overflow-x: hidden;
  }

  /* Animated grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(79,142,247,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(79,142,247,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container { max-width: 900px; margin: 0 auto; position: relative; z-index: 1; }

  /* ─── HEADER ─── */
  .header {
    border: 1px solid var(--border2);
    border-radius: 20px;
    padding: 2.5rem 2.5rem 2rem;
    background: var(--surface);
    margin-bottom: 1.25rem;
    position: relative;
    overflow: hidden;
  }
  .header-glow {
    position: absolute;
    top: -80px; right: -80px;
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(79,142,247,0.12) 0%, transparent 65%);
    pointer-events: none;
  }
  .header-glow2 {
    position: absolute;
    bottom: -60px; left: 10%;
    width: 250px; height: 250px;
    background: radial-gradient(circle, rgba(47,255,180,0.07) 0%, transparent 65%);
    pointer-events: none;
  }
  .header-inner {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 2rem;
    align-items: start;
    position: relative;
    z-index: 1;
  }
  .chip {
    display: inline-flex; align-items: center; gap: 6px;
    font-family: 'JetBrains Mono', monospace;
    font-size: 11px; letter-spacing: 0.12em; text-transform: uppercase;
    padding: 4px 12px; border-radius: 100px;
  }
  .chip-blue { background: rgba(79,142,247,0.12); border: 1px solid rgba(79,142,247,0.3); color: var(--accent); }
  .chip-green { background: rgba(47,255,180,0.1); border: 1px solid rgba(47,255,180,0.25); color: var(--accent2); }
  .chip-red { background: rgba(255,107,107,0.1); border: 1px solid rgba(255,107,107,0.25); color: var(--accent3); }
  .chip-gold { background: rgba(255,217,61,0.1); border: 1px solid rgba(255,217,61,0.25); color: var(--accent4); }
  .dot-pulse { width: 6px; height: 6px; border-radius: 50%; background: currentColor; animation: pulse 2s infinite; }
  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.4;transform:scale(0.7)} }

  .name-block { margin: 14px 0 12px; }
  h1 {
    font-family: 'Playfair Display', serif;
    font-size: 48px;
    line-height: 1.05;
    color: var(--text);
    letter-spacing: -1px;
  }
  h1 em { font-style: italic; color: var(--accent); }
  .tagline {
    font-size: 14px;
    color: var(--muted);
    line-height: 1.7;
    margin-top: 10px;
    max-width: 500px;
  }
  .tagline strong { color: var(--accent2); font-weight: 600; }

  .social-row { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 20px; }
  .social-btn {
    display: inline-flex; align-items: center; gap: 7px;
    padding: 7px 14px;
    border-radius: 9px;
    font-size: 12px; font-family: 'JetBrains Mono', monospace;
    border: 1px solid var(--border2);
    background: var(--surface2);
    color: var(--muted);
    text-decoration: none;
    transition: all 0.2s;
    cursor: pointer;
  }
  .social-btn:hover { border-color: var(--accent); color: var(--accent); background: rgba(79,142,247,0.07); }
  .social-btn.linkedin:hover { border-color: #0A66C2; color: #4A9EF0; background: rgba(10,102,194,0.08); }

  .avatar-wrap { display: flex; flex-direction: column; align-items: center; gap: 10px; }
  .avatar {
    width: 90px; height: 90px; border-radius: 18px;
    background: linear-gradient(135deg, #2A4EAA, #4F8EF7);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif; font-size: 32px; font-weight: 700; color: white;
    box-shadow: 0 8px 30px rgba(79,142,247,0.35), 0 0 0 1px rgba(79,142,247,0.2);
    position: relative; overflow: hidden;
  }
  .avatar::after {
    content: '';
    position: absolute; inset: 0;
    background: linear-gradient(135deg, rgba(255,255,255,0.15) 0%, transparent 60%);
  }
  .gpa-badge {
    font-family: 'JetBrains Mono', monospace; font-size: 10px;
    color: var(--accent4); background: rgba(255,217,61,0.08);
    border: 1px solid rgba(255,217,61,0.2); border-radius: 6px;
    padding: 3px 9px; text-align: center;
  }

  /* ─── BACKEND HERO BANNER ─── */
  .backend-banner {
    background: linear-gradient(120deg, rgba(79,142,247,0.1) 0%, rgba(13,17,32,0.8) 50%, rgba(47,255,180,0.06) 100%);
    border: 1px solid rgba(79,142,247,0.3);
    border-radius: 16px;
    padding: 1.4rem 1.75rem;
    margin-bottom: 1.25rem;
    display: flex;
    align-items: center;
    gap: 20px;
    position: relative;
    overflow: hidden;
  }
  .backend-banner::before {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 4px;
    background: linear-gradient(180deg, var(--accent), var(--accent2));
    border-radius: 4px 0 0 4px;
  }
  .bb-icon { font-size: 32px; flex-shrink: 0; }
  .bb-title { font-size: 13px; font-weight: 700; color: var(--accent); letter-spacing: 0.05em; margin-bottom: 5px; text-transform: uppercase; font-family: 'JetBrains Mono', monospace; }
  .bb-desc { font-size: 13px; color: var(--muted); line-height: 1.6; }
  .bb-desc strong { color: var(--text); }
  .bb-stack { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 10px; }
  .bb-badge {
    font-size: 11px; font-family: 'JetBrains Mono', monospace;
    padding: 3px 10px; border-radius: 5px;
    background: rgba(79,142,247,0.12); border: 1px solid rgba(79,142,247,0.3); color: var(--accent);
    font-weight: 500;
  }

  /* ─── GRID LAYOUT ─── */
  .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 1.25rem; margin-bottom: 1.25rem; }
  .grid-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 1.25rem; margin-bottom: 1.25rem; }

  /* ─── CARDS ─── */
  .card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 1.5rem;
    position: relative;
    overflow: hidden;
  }
  .card-label {
    font-size: 10px; font-family: 'JetBrains Mono', monospace;
    color: var(--faint); letter-spacing: 0.15em; text-transform: uppercase;
    margin-bottom: 16px; display: flex; align-items: center; gap: 8px;
  }
  .card-label::after { content: ''; flex: 1; height: 1px; background: var(--border); }

  /* ─── STATS ─── */
  .stat-row { display: grid; grid-template-columns: repeat(4, 1fr); gap: 10px; margin-bottom: 1.25rem; }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 1.1rem 1rem;
    text-align: center;
    position: relative; overflow: hidden;
    transition: border-color 0.2s, transform 0.2s;
    cursor: default;
  }
  .stat-card:hover { border-color: var(--accent); transform: translateY(-2px); }
  .stat-card::before {
    content: ''; position: absolute; bottom: 0; left: 0; right: 0;
    height: 2px; opacity: 0; transition: opacity 0.2s;
  }
  .stat-card:hover::before { opacity: 1; }
  .stat-card.s1::before { background: var(--accent); }
  .stat-card.s2::before { background: var(--accent2); }
  .stat-card.s3::before { background: var(--accent3); }
  .stat-card.s4::before { background: var(--accent4); }
  .stat-num {
    font-family: 'Playfair Display', serif; font-size: 28px; line-height: 1; margin-bottom: 5px;
  }
  .stat-num.blue { color: var(--accent); }
  .stat-num.green { color: var(--accent2); }
  .stat-num.red { color: var(--accent3); }
  .stat-num.gold { color: var(--accent4); }
  .stat-lbl { font-size: 11px; color: var(--muted); font-family: 'JetBrains Mono', monospace; }

  /* ─── COMMIT TRACKER ─── */
  .commit-tracker {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 1.5rem;
    margin-bottom: 1.25rem;
  }
  .ct-header {
    display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;
    flex-wrap: wrap; gap: 10px;
  }
  .ct-title-block { display: flex; flex-direction: column; gap: 4px; }
  .ct-title {
    font-size: 13px; font-weight: 600; color: var(--text);
    display: flex; align-items: center; gap: 8px;
  }
  .ct-subtitle { font-size: 11px; color: var(--muted); font-family: 'JetBrains Mono', monospace; }
  .ct-controls { display: flex; gap: 8px; align-items: center; }
  .ct-btn {
    font-size: 11px; font-family: 'JetBrains Mono', monospace;
    padding: 5px 12px; border-radius: 7px;
    border: 1px solid var(--border2); background: var(--surface2);
    color: var(--muted); cursor: pointer; transition: all 0.2s;
  }
  .ct-btn:hover, .ct-btn.active { border-color: var(--accent); color: var(--accent); background: rgba(79,142,247,0.08); }
  .ct-btn.add { border-color: rgba(47,255,180,0.3); color: var(--accent2); background: rgba(47,255,180,0.07); }
  .ct-btn.add:hover { background: rgba(47,255,180,0.14); }

  /* Contribution grid */
  .contrib-wrap { overflow-x: auto; padding-bottom: 4px; }
  .contrib-grid {
    display: grid;
    grid-template-rows: repeat(7, 13px);
    grid-auto-flow: column;
    gap: 3px;
    min-width: max-content;
  }
  .contrib-cell {
    width: 13px; height: 13px; border-radius: 3px;
    cursor: pointer; transition: transform 0.15s, box-shadow 0.15s;
    position: relative;
  }
  .contrib-cell:hover { transform: scale(1.3); z-index: 10; }
  .contrib-cell.l0 { background: var(--surface3); border: 1px solid var(--border); }
  .contrib-cell.l1 { background: rgba(79,142,247,0.25); border: 1px solid rgba(79,142,247,0.4); }
  .contrib-cell.l2 { background: rgba(79,142,247,0.50); border: 1px solid rgba(79,142,247,0.6); }
  .contrib-cell.l3 { background: rgba(79,142,247,0.75); border: 1px solid rgba(79,142,247,0.85); }
  .contrib-cell.l4 { background: #4F8EF7; border: 1px solid #6BA4F9; box-shadow: 0 0 6px rgba(79,142,247,0.5); }
  .contrib-cell.today { box-shadow: 0 0 0 2px var(--accent2) !important; }

  .contrib-legend { display: flex; align-items: center; gap: 6px; margin-top: 10px; justify-content: flex-end; }
  .contrib-legend span { font-size: 10px; color: var(--muted); font-family: 'JetBrains Mono', monospace; }
  .legend-cell { width: 12px; height: 12px; border-radius: 2px; }

  /* Streak stats */
  .streak-row { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; margin-top: 16px; }
  .streak-item {
    background: var(--surface2); border: 1px solid var(--border);
    border-radius: 10px; padding: 12px; text-align: center;
  }
  .streak-num { font-family: 'Playfair Display', serif; font-size: 22px; color: var(--accent); margin-bottom: 3px; }
  .streak-lbl { font-size: 10px; color: var(--muted); font-family: 'JetBrains Mono', monospace; }

  /* Log today modal */
  .log-form {
    background: var(--surface2); border: 1px solid var(--border2);
    border-radius: 12px; padding: 16px; margin-top: 16px;
    display: none;
  }
  .log-form.open { display: block; animation: slideDown 0.2s ease; }
  @keyframes slideDown { from{opacity:0;transform:translateY(-8px)} to{opacity:1;transform:translateY(0)} }
  .log-row { display: flex; gap: 10px; flex-wrap: wrap; align-items: flex-end; }
  .log-field { display: flex; flex-direction: column; gap: 5px; flex: 1; min-width: 120px; }
  .log-field label { font-size: 10px; color: var(--muted); font-family: 'JetBrains Mono', monospace; text-transform: uppercase; letter-spacing: 0.1em; }
  .log-field input, .log-field select {
    background: var(--surface3); border: 1px solid var(--border2);
    border-radius: 7px; color: var(--text); padding: 7px 10px;
    font-family: 'JetBrains Mono', monospace; font-size: 12px;
    outline: none;
  }
  .log-field input:focus, .log-field select:focus { border-color: var(--accent); }
  .log-field input[type="number"] { width: 80px; }
  .log-submit {
    padding: 8px 16px; border-radius: 7px;
    background: var(--accent); border: none; color: white;
    font-family: 'Space Grotesk', sans-serif; font-weight: 600; font-size: 12px;
    cursor: pointer; transition: background 0.2s; flex-shrink: 0;
  }
  .log-submit:hover { background: #3A7DE8; }

  /* Commit log feed */
  .commit-feed { margin-top: 14px; display: flex; flex-direction: column; gap: 6px; max-height: 160px; overflow-y: auto; }
  .commit-feed::-webkit-scrollbar { width: 4px; }
  .commit-feed::-webkit-scrollbar-track { background: transparent; }
  .commit-feed::-webkit-scrollbar-thumb { background: var(--border2); border-radius: 2px; }
  .commit-entry {
    display: flex; align-items: center; gap: 10px;
    padding: 8px 12px;
    background: var(--surface2); border: 1px solid var(--border);
    border-radius: 8px; font-size: 11px; font-family: 'JetBrains Mono', monospace;
    transition: border-color 0.15s;
  }
  .commit-entry:hover { border-color: var(--border2); }
  .commit-date { color: var(--muted); flex-shrink: 0; }
  .commit-msg { color: var(--text); flex: 1; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
  .commit-tag {
    font-size: 9px; padding: 2px 7px; border-radius: 4px; flex-shrink: 0;
  }
  .tag-backend { background: rgba(79,142,247,0.15); color: var(--accent); border: 1px solid rgba(79,142,247,0.3); }
  .tag-ml { background: rgba(255,107,107,0.12); color: var(--accent3); border: 1px solid rgba(255,107,107,0.25); }
  .tag-other { background: var(--surface3); color: var(--muted); border: 1px solid var(--border); }
  .commit-count { color: var(--accent2); font-weight: 600; flex-shrink: 0; }

  /* ─── BACKEND DEEP DIVE ─── */
  .backend-section {
    background: var(--surface);
    border: 1px solid rgba(79,142,247,0.25);
    border-radius: 16px;
    padding: 1.5rem;
    margin-bottom: 1.25rem;
    position: relative; overflow: hidden;
  }
  .backend-section::before {
    content: 'BACKEND';
    position: absolute; top: 16px; right: 20px;
    font-family: 'Playfair Display', serif; font-size: 80px; font-style: italic;
    color: rgba(79,142,247,0.04); pointer-events: none; line-height: 1;
    user-select: none;
  }
  .bs-grid { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 12px; }
  .bs-item {
    background: var(--surface2); border: 1px solid var(--border);
    border-radius: 11px; padding: 1rem;
    transition: border-color 0.2s, transform 0.2s; cursor: default;
  }
  .bs-item:hover { border-color: rgba(79,142,247,0.4); transform: translateY(-2px); }
  .bs-icon { font-size: 20px; margin-bottom: 8px; }
  .bs-name { font-size: 13px; font-weight: 600; color: var(--text); margin-bottom: 4px; }
  .bs-desc { font-size: 11px; color: var(--muted); line-height: 1.5; font-family: 'JetBrains Mono', monospace; }
  .bs-bar-wrap { margin-top: 8px; height: 3px; background: var(--border); border-radius: 2px; overflow: hidden; }
  .bs-bar { height: 100%; background: linear-gradient(90deg, var(--accent), var(--accent2)); border-radius: 2px; transition: width 1s ease; }

  /* ─── EXPERIENCE ─── */
  .exp-item {
    display: flex; gap: 14px; padding-bottom: 20px; position: relative;
  }
  .exp-item:not(:last-child)::after {
    content: ''; position: absolute; left: 17px; top: 36px; bottom: 0;
    width: 1px; background: var(--border);
  }
  .exp-dot {
    width: 36px; height: 36px; border-radius: 10px;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0; font-size: 15px; position: relative; z-index: 1;
  }
  .exp-dot.backend { background: rgba(79,142,247,0.12); border: 1px solid rgba(79,142,247,0.3); }
  .exp-dot.ml { background: rgba(255,107,107,0.1); border: 1px solid rgba(255,107,107,0.25); }
  .exp-role { font-size: 14px; font-weight: 600; color: var(--text); margin-bottom: 2px; }
  .exp-company { font-size: 12px; color: var(--accent); font-family: 'JetBrains Mono', monospace; margin-bottom: 8px; }
  .exp-bullets { list-style: none; display: flex; flex-direction: column; gap: 5px; }
  .exp-bullets li { font-size: 12px; color: var(--muted); display: flex; gap: 8px; align-items: flex-start; line-height: 1.5; }
  .exp-bullets li::before { content: '→'; color: var(--faint); flex-shrink: 0; }
  .exp-bullets li strong { color: var(--accent); }

  /* ─── PROJECTS ─── */
  .project-card {
    background: var(--surface2); border: 1px solid var(--border);
    border-radius: 13px; padding: 1.25rem; margin-bottom: 10px;
    position: relative; overflow: hidden; transition: border-color 0.2s, transform 0.2s;
  }
  .project-card:hover { border-color: var(--accent); transform: translateX(3px); }
  .project-card:last-child { margin-bottom: 0; }
  .project-card::before {
    content: ''; position: absolute; top: 0; left: 0;
    width: 3px; height: 100%; border-radius: 3px 0 0 3px;
  }
  .pc-blue::before { background: var(--accent); }
  .pc-green::before { background: var(--accent2); }
  .pc-red::before { background: var(--accent3); }
  .pc-grad::before { background: linear-gradient(180deg, var(--accent), var(--accent2)); }
  .project-header { display: flex; align-items: flex-start; justify-content: space-between; gap: 8px; margin-bottom: 7px; }
  .project-name { font-size: 14px; font-weight: 600; color: var(--text); display: flex; align-items: center; gap: 8px; }
  .acc-pill {
    font-size: 10px; font-family: 'JetBrains Mono', monospace;
    padding: 2px 9px; border-radius: 4px;
    background: rgba(47,255,180,0.1); color: var(--accent2);
    border: 1px solid rgba(47,255,180,0.25); white-space: nowrap;
  }
  .project-desc { font-size: 12px; color: var(--muted); line-height: 1.7; margin-bottom: 10px; }
  .tag-row { display: flex; flex-wrap: wrap; gap: 5px; }
  .tag {
    font-size: 10px; font-family: 'JetBrains Mono', monospace;
    padding: 2px 8px; border-radius: 4px;
    border: 1px solid var(--border); color: var(--faint);
    transition: border-color 0.15s, color 0.15s;
  }
  .tag.backend-tag { border-color: rgba(79,142,247,0.25); color: rgba(79,142,247,0.7); }
  .tag.ml-tag { border-color: rgba(255,107,107,0.25); color: rgba(255,107,107,0.7); }

  /* ─── TECH STACK TABS ─── */
  .tabs { display: flex; gap: 6px; margin-bottom: 14px; flex-wrap: wrap; }
  .tab-btn {
    font-size: 11px; font-family: 'JetBrains Mono', monospace;
    padding: 5px 12px; border-radius: 7px;
    border: 1px solid var(--border); background: transparent; color: var(--muted);
    cursor: pointer; transition: all 0.2s;
  }
  .tab-btn:hover { border-color: var(--border2); color: var(--text); }
  .tab-btn.active.backend { border-color: var(--accent); color: var(--accent); background: rgba(79,142,247,0.08); }
  .tab-btn.active.ml { border-color: var(--accent3); color: var(--accent3); background: rgba(255,107,107,0.08); }
  .tab-btn.active.tools { border-color: var(--accent2); color: var(--accent2); background: rgba(47,255,180,0.07); }
  .tab-panel { display: none; }
  .tab-panel.active { display: block; animation: fadeIn 0.2s; }
  @keyframes fadeIn { from{opacity:0} to{opacity:1} }
  .badge-row { display: flex; flex-wrap: wrap; gap: 7px; }
  .badge {
    font-size: 11px; font-family: 'JetBrains Mono', monospace;
    padding: 5px 11px; border-radius: 7px;
    border: 1px solid var(--border); background: var(--surface2); color: var(--muted);
    transition: all 0.2s; cursor: default;
  }
  .badge:hover { transform: translateY(-2px); }
  .badge.b { border-color: rgba(79,142,247,0.35); color: #78AAFF; background: rgba(79,142,247,0.08); }
  .badge.m { border-color: rgba(255,107,107,0.3); color: #FF9898; background: rgba(255,107,107,0.07); }
  .badge.t { border-color: rgba(47,255,180,0.3); color: #2FFFB4; background: rgba(47,255,180,0.06); }

  /* ─── CERTS ─── */
  .cert-item {
    display: flex; align-items: center; gap: 12px;
    padding: 10px 12px; background: var(--surface2);
    border-radius: 9px; border: 1px solid var(--border);
    font-size: 12px; color: var(--muted); margin-bottom: 8px;
    transition: border-color 0.2s;
  }
  .cert-item:hover { border-color: var(--border2); }
  .cert-item:last-child { margin-bottom: 0; }
  .cert-icon { font-size: 16px; flex-shrink: 0; }
  .cert-name { color: var(--text); font-size: 13px; }
  .cert-org { font-family: 'JetBrains Mono', monospace; font-size: 10px; color: var(--faint); margin-top: 1px; }

  /* ─── FOOTER ─── */
  .footer {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 2rem; text-align: center; margin-top: 1.25rem;
    position: relative; overflow: hidden;
  }
  .footer::before {
    content: ''; position: absolute; inset: 0;
    background: radial-gradient(ellipse at center bottom, rgba(79,142,247,0.06) 0%, transparent 60%);
    pointer-events: none;
  }
  .footer-title { font-family: 'Playfair Display', serif; font-size: 24px; margin-bottom: 6px; }
  .footer-sub { font-size: 13px; color: var(--muted); margin-bottom: 20px; }
  .footer-btns { display: flex; gap: 10px; justify-content: center; flex-wrap: wrap; }
  .fb {
    padding: 10px 22px; border-radius: 9px;
    font-size: 13px; font-weight: 600;
    cursor: pointer; border: 1px solid transparent;
    text-decoration: none; display: inline-flex; align-items: center; gap: 8px;
    transition: all 0.2s;
  }
  .fb.primary { background: var(--accent); color: white; }
  .fb.primary:hover { background: #3A7DE8; transform: translateY(-1px); box-shadow: 0 4px 16px rgba(79,142,247,0.35); }
  .fb.linkedin { background: #0A66C2; color: white; }
  .fb.linkedin:hover { background: #0856A8; transform: translateY(-1px); box-shadow: 0 4px 16px rgba(10,102,194,0.4); }
  .fb.secondary { background: transparent; color: var(--text); border-color: var(--border); }
  .fb.secondary:hover { border-color: var(--accent); color: var(--accent); }

  /* ─── COPY SECTION ─── */
  .copy-section {
    background: var(--surface); border: 1px solid var(--border);
    border-radius: 14px; padding: 1.5rem; margin-top: 2rem;
  }
  .copy-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 14px; }
  .copy-title { font-size: 12px; font-family: 'JetBrains Mono', monospace; color: var(--muted); }
  .copy-btn {
    font-size: 11px; padding: 6px 14px; border-radius: 7px;
    border: 1px solid var(--border); background: var(--surface2); color: var(--muted);
    cursor: pointer; font-family: 'JetBrains Mono', monospace; display: flex; align-items: center; gap: 6px;
    transition: all 0.2s;
  }
  .copy-btn:hover { border-color: var(--accent); color: var(--accent); }
  textarea {
    width: 100%; background: var(--surface2); border: 1px solid var(--border);
    border-radius: 8px; color: var(--muted); font-family: 'JetBrains Mono', monospace;
    font-size: 11px; line-height: 1.6; padding: 1rem; resize: vertical; min-height: 200px; outline: none;
  }

  /* ─── TOOLTIP ─── */
  .tooltip {
    position: fixed; z-index: 1000;
    background: var(--surface3); border: 1px solid var(--border2);
    border-radius: 7px; padding: 5px 10px;
    font-size: 10px; font-family: 'JetBrains Mono', monospace; color: var(--text);
    pointer-events: none; display: none; white-space: nowrap;
    box-shadow: 0 4px 14px rgba(0,0,0,0.4);
  }

  @media(max-width:600px) {
    .header-inner { grid-template-columns: 1fr; }
    .avatar-wrap { flex-direction: row; margin-top: 16px; }
    .grid-2, .stat-row, .streak-row { grid-template-columns: 1fr; }
    h1 { font-size: 34px; }
    .bs-grid { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>
<div class="container">

<!-- TOOLTIP -->
<div class="tooltip" id="tooltip"></div>

<!-- ─── HEADER ─── -->
<div class="header">
  <div class="header-glow"></div>
  <div class="header-glow2"></div>
  <div class="header-inner">
    <div>
      <div class="chip chip-green"><div class="dot-pulse"></div>Open to backend opportunities</div>
      <div class="name-block">
        <h1>Priyadharshini <em>G</em></h1>
      </div>
      <p class="tagline">
        <strong>Backend & ML Engineer</strong> who ships production-ready APIs and deep learning models —
        obsessive about clean architecture, query performance, and model accuracy.
      </p>
      <div class="social-row">
        <a class="social-btn linkedin" href="https://www.linkedin.com/in/priyadharshini-g-17bbaa27b" target="_blank">
          <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          LinkedIn
        </a>
        <a class="social-btn" href="mailto:gpriyampt@gmail.com">✉ Email</a>
        <a class="social-btn" href="https://github.com/Gpriyadharshini8148" target="_blank">
          <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/></svg>
          GitHub
        </a>
        <span class="chip chip-gold">CS'26 · Annamalai University</span>
      </div>
    </div>
    <div class="avatar-wrap">
      <div class="avatar">PG</div>
      <div class="gpa-badge">CGPA 9.52 / 10</div>
    </div>
  </div>
</div>

<!-- ─── BACKEND HERO ─── -->
<div class="backend-banner">
  <div class="bb-icon">⚙️</div>
  <div style="flex:1">
    <div class="bb-title">// Core Expertise · Backend Engineering</div>
    <div class="bb-desc">
      <strong>Production-grade REST APIs</strong> with Django REST Framework &amp; Flask.
      Specialized in <strong>PostgreSQL schema design</strong>, Docker-based CI/CD, query optimization,
      and building scalable, maintainable backend systems.
    </div>
    <div class="bb-stack">
      <span class="bb-badge">Django REST</span>
      <span class="bb-badge">Flask</span>
      <span class="bb-badge">PostgreSQL</span>
      <span class="bb-badge">Docker</span>
      <span class="bb-badge">Kafka</span>
      <span class="bb-badge">Celery</span>
      <span class="bb-badge">Redis</span>
      <span class="bb-badge">AWS</span>
    </div>
  </div>
</div>

<!-- ─── STATS ROW ─── -->
<div class="stat-row">
  <div class="stat-card s1">
    <div class="stat-num blue">10<sup style="font-size:16px">+</sup></div>
    <div class="stat-lbl">REST APIs shipped</div>
  </div>
  <div class="stat-card s2">
    <div class="stat-num green">95<sup style="font-size:16px">%</sup></div>
    <div class="stat-lbl">Best model accuracy</div>
  </div>
  <div class="stat-card s3">
    <div class="stat-num red">~30<sup style="font-size:14px">%</sup></div>
    <div class="stat-lbl">DB query speedup</div>
  </div>
  <div class="stat-card s4">
    <div class="stat-num gold">9.46</div>
    <div class="stat-lbl">CGPA / 10</div>
  </div>
</div>

<!-- ─── COMMIT TRACKER ─── -->
<div class="commit-tracker">
  <div class="ct-header">
    <div class="ct-title-block">
      <div class="ct-title">
        <span>📊</span> Daily Commit Tracker
        <span class="chip chip-green" id="commit-today-chip" style="font-size:10px"></span>
      </div>
      <div class="ct-subtitle">Track your coding activity · click a cell to inspect · log today's commits</div>
    </div>
    <div class="ct-controls">
      <button class="ct-btn active" onclick="setView('year')" id="btn-year">Year</button>
      <button class="ct-btn" onclick="setView('month')" id="btn-month">Month</button>
      <button class="ct-btn add" onclick="toggleLogForm()">+ Log Today</button>
    </div>
  </div>

  <!-- Grid -->
  <div class="contrib-wrap">
    <div class="contrib-grid" id="contrib-grid"></div>
  </div>
  <div class="contrib-legend">
    <span>Less</span>
    <div class="legend-cell l0" style="background:var(--surface3);border:1px solid var(--border);"></div>
    <div class="legend-cell l1" style="background:rgba(79,142,247,0.25);"></div>
    <div class="legend-cell l2" style="background:rgba(79,142,247,0.50);"></div>
    <div class="legend-cell l3" style="background:rgba(79,142,247,0.75);"></div>
    <div class="legend-cell l4" style="background:#4F8EF7;"></div>
    <span>More</span>
  </div>

  <!-- Streak stats -->
  <div class="streak-row">
    <div class="streak-item">
      <div class="streak-num" id="streak-current">0</div>
      <div class="streak-lbl">Current Streak</div>
    </div>
    <div class="streak-item">
      <div class="streak-num" id="streak-longest">0</div>
      <div class="streak-lbl">Longest Streak</div>
    </div>
    <div class="streak-item">
      <div class="streak-num" id="streak-total">0</div>
      <div class="streak-lbl">Total Commits</div>
    </div>
  </div>

  <!-- Log form -->
  <div class="log-form" id="log-form">
    <div class="log-row">
      <div class="log-field">
        <label>Message</label>
        <input type="text" id="log-msg" placeholder="feat: add user auth endpoint" style="flex:1;min-width:200px"/>
      </div>
      <div class="log-field">
        <label>Count</label>
        <input type="number" id="log-count" min="1" max="20" value="1" style="width:70px"/>
      </div>
      <div class="log-field">
        <label>Type</label>
        <select id="log-type">
          <option value="backend">Backend</option>
          <option value="ml">ML / AI</option>
          <option value="other">Other</option>
        </select>
      </div>
      <button class="log-submit" onclick="logCommit()">Commit →</button>
    </div>
  </div>

  <!-- Feed -->
  <div class="commit-feed" id="commit-feed"></div>
</div>

<!-- ─── BACKEND DEEP DIVE ─── -->
<div class="backend-section" style="margin-bottom:1.25rem;">
  <div class="card-label">Backend engineering stack</div>
  <div class="bs-grid">
    <div class="bs-item">
      <div class="bs-icon">🐍</div>
      <div class="bs-name">Django REST Framework</div>
      <div class="bs-desc">10+ production APIs · ViewSets · Serializers · Auth middleware</div>
      <div class="bs-bar-wrap"><div class="bs-bar" style="width:90%"></div></div>
    </div>
    <div class="bs-item">
      <div class="bs-icon">🌶️</div>
      <div class="bs-name">Flask</div>
      <div class="bs-desc">Microservices · ML model serving · REST APIs · Blueprints</div>
      <div class="bs-bar-wrap"><div class="bs-bar" style="width:85%"></div></div>
    </div>
    <div class="bs-item">
      <div class="bs-icon">🐘</div>
      <div class="bs-name">PostgreSQL</div>
      <div class="bs-desc">Schema design · Query optimization (~30% speedup) · Indexing</div>
      <div class="bs-bar-wrap"><div class="bs-bar" style="width:80%"></div></div>
    </div>
    <div class="bs-item">
      <div class="bs-icon">🐳</div>
      <div class="bs-name">Docker</div>
      <div class="bs-desc">Containerization · CI/CD pipelines · Multi-stage builds</div>
      <div class="bs-bar-wrap"><div class="bs-bar" style="width:75%"></div></div>
    </div>
    <div class="bs-item">
      <div class="bs-icon">📨</div>
      <div class="bs-name">Kafka + Celery</div>
      <div class="bs-desc">Async task queues · Event streaming · Background workers</div>
      <div class="bs-bar-wrap"><div class="bs-bar" style="width:65%"></div></div>
    </div>
    <div class="bs-item">
      <div class="bs-icon">☁️</div>
      <div class="bs-name">AWS + System Design</div>
      <div class="bs-desc">EC2 · S3 · Learning distributed systems & Kafka streams</div>
      <div class="bs-bar-wrap"><div class="bs-bar" style="width:55%"></div></div>
    </div>
  </div>
</div>

<!-- ─── EXPERIENCE + TECH ─── -->
<div class="grid-2">
  <div class="card">
    <div class="card-label">Experience</div>
    <div>
      <div class="exp-item">
        <div class="exp-dot backend">⚙</div>
        <div>
          <div class="exp-role">SDE Intern <span class="chip chip-blue" style="font-size:9px;padding:2px 7px;vertical-align:middle;">Backend</span></div>
          <div class="exp-company">Cyces Innovation Lab · Jan 2026 – Present</div>
          <ul class="exp-bullets">
            <li>Built <strong>10+ RESTful APIs</strong> with Django REST Framework</li>
            <li>PostgreSQL schema design, cut query time <strong>~30%</strong></li>
            <li>Docker CI/CD + Git feature branching workflows</li>
          </ul>
        </div>
      </div>
      <div class="exp-item">
        <div class="exp-dot ml">🧠</div>
        <div>
          <div class="exp-role">ML Research Intern</div>
          <div class="exp-company">NIT Puducherry · May – Jun 2025</div>
          <ul class="exp-bullets">
            <li>CNN models achieving <strong>90%+ accuracy</strong> (TF · Keras)</li>
            <li>Flask integration, reduced inference latency 25%</li>
            <li>OpenCV preprocessing for real-world robustness</li>
          </ul>
        </div>
      </div>
    </div>
  </div>

  <div class="card">
    <div class="card-label">Tech stack</div>
    <div class="tabs">
      <button class="tab-btn active backend" onclick="switchTab('backend', this, 'backend')">⚙ Backend</button>
      <button class="tab-btn" onclick="switchTab('ml', this, 'ml')">🧠 ML / AI</button>
      <button class="tab-btn" onclick="switchTab('tools', this, 'tools')">🛠 Tools</button>
    </div>
    <div class="tab-panel active" id="tab-backend">
      <div class="badge-row">
        <span class="badge b">Python</span>
        <span class="badge b">Django REST</span>
        <span class="badge b">Flask</span>
        <span class="badge b">PostgreSQL</span>
        <span class="badge b">Docker</span>
        <span class="badge b">Kafka</span>
        <span class="badge b">Celery</span>
        <span class="badge b">Redis</span>
        <span class="badge b">REST API</span>
        <span class="badge b">SQLite</span>
      </div>
    </div>
    <div class="tab-panel" id="tab-ml">
      <div class="badge-row">
        <span class="badge m">TensorFlow</span>
        <span class="badge m">Keras</span>
        <span class="badge m">OpenCV</span>
        <span class="badge m">MediaPipe</span>
        <span class="badge m">Scikit-Learn</span>
        <span class="badge m">PyTorch</span>
        <span class="badge m">IndicBERT</span>
        <span class="badge m">XLM-R</span>
        <span class="badge m">CNN+LSTM</span>
        <span class="badge m">NLP</span>
      </div>
    </div>
    <div class="tab-panel" id="tab-tools">
      <div class="badge-row">
        <span class="badge t">Git</span>
        <span class="badge t">AWS</span>
        <span class="badge t">Postman</span>
        <span class="badge t">Firebase</span>
        <span class="badge t">Power BI</span>
        <span class="badge t">React.js</span>
        <span class="badge t">MySQL</span>
        <span class="badge t">Android Studio</span>
      </div>
    </div>
  </div>
</div>

<!-- ─── PROJECTS ─── -->
<div class="card" style="margin-bottom:1.25rem;">
  <div class="card-label">Featured projects</div>
  <div class="project-card pc-blue">
    <div class="project-header">
      <div class="project-name">🤟 AI Model for Assisting the Deaf</div>
      <span class="acc-pill">95%+ accuracy</span>
    </div>
    <p class="project-desc">Real-time two-way communication using MediaPipe hand landmark extraction + CNN. Integrated speech-to-text, multilingual translation, and audio feedback. Deployed via Flask with SQLite-backed session management.</p>
    <div class="tag-row">
      <span class="tag backend-tag">Flask</span>
      <span class="tag ml-tag">TensorFlow</span>
      <span class="tag ml-tag">Keras</span>
      <span class="tag ml-tag">MediaPipe</span>
      <span class="tag ml-tag">OpenCV</span>
      <span class="tag backend-tag">SQLite</span>
    </div>
  </div>
  <div class="project-card pc-green">
    <div class="project-header">
      <div class="project-name">🫁 Pneumonia Detection using ML</div>
      <span class="acc-pill">92% test accuracy</span>
    </div>
    <p class="project-desc">Binary chest X-ray classifier on 5,000+ images. CNN with iterative hyperparameter tuning. Automated OpenCV preprocessing pipeline. Evaluated with F1-score, precision, recall, and confusion matrix.</p>
    <div class="tag-row">
      <span class="tag">Python</span>
      <span class="tag ml-tag">TensorFlow</span>
      <span class="tag ml-tag">Keras</span>
      <span class="tag ml-tag">Scikit-Learn</span>
      <span class="tag ml-tag">OpenCV</span>
    </div>
  </div>
  <div class="project-card pc-red">
    <div class="project-header">
      <div class="project-name">✈️ TravelGo — Android Travel Planner</div>
    </div>
    <p class="project-desc">Full Android app with itinerary creation, real-time weather, and location-based recommendations. Firebase authentication and real-time data sync. Optimized UI/UX across multiple screen sizes.</p>
    <div class="tag-row">
      <span class="tag">Java</span>
      <span class="tag">Android Studio</span>
      <span class="tag">Firebase</span>
      <span class="tag">XML</span>
    </div>
  </div>
  <div class="project-card pc-grad">
    <div class="project-header">
      <div class="project-name">🗣️ Tanglish Sentiment &amp; Emotion Analyser <span style="font-size:10px;color:var(--muted);font-weight:400">· Final Year Thesis</span></div>
      <span class="acc-pill">94% accuracy</span>
    </div>
    <p class="project-desc">Hybrid CNN+LSTM+Transformer architecture for Tamil-English code-mixed NLP using IndicBERT and XLM-R. Served via Flask REST APIs. Live React.js dashboard for social media analytics, customer feedback monitoring, and political opinion mining.</p>
    <div class="tag-row">
      <span class="tag backend-tag">Flask</span>
      <span class="tag">React.js</span>
      <span class="tag ml-tag">TensorFlow</span>
      <span class="tag ml-tag">PyTorch</span>
      <span class="tag ml-tag">IndicBERT</span>
      <span class="tag ml-tag">XLM-R</span>
      <span class="tag ml-tag">CNN+LSTM</span>
      <span class="tag">Twitter API</span>
      <span class="tag backend-tag">MySQL</span>
    </div>
  </div>
</div>

<!-- ─── CERTS + GH STATS ─── -->
<div class="grid-2">
  <div class="card">
    <div class="card-label">Certifications</div>
    <div class="cert-item">
      <span class="cert-icon">☁️</span>
      <div><div class="cert-name">Cloud Computing</div><div class="cert-org">NPTEL · IIT Kharagpur</div></div>
    </div>
    <div class="cert-item">
      <span class="cert-icon">🌐</span>
      <div><div class="cert-name">Social Networks</div><div class="cert-org">NPTEL</div></div>
    </div>
    <div class="cert-item">
      <span class="cert-icon">📊</span>
      <div><div class="cert-name">Data for Everyone</div><div class="cert-org">Google Career Certificates</div></div>
    </div>
    <div class="cert-item">
      <span class="cert-icon">🔐</span>
      <div><div class="cert-name">Cybersecurity Analyst Simulation</div><div class="cert-org">Tata Group · Forage</div></div>
    </div>
  </div>
  <div class="card">
    <div class="card-label">GitHub live stats</div>
    <div style="display:flex;flex-direction:column;gap:8px;">
      <img src="https://github-readme-stats.vercel.app/api?username=Gpriyadharshini8148&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&bg_color=0D1120&title_color=4F8EF7&icon_color=2FFFB4&text_color=7B849E" style="width:100%;border-radius:8px;" loading="lazy" alt="GitHub stats" onerror="this.style.display='none'"/>
      <img src="https://streak-stats.demolab.com?user=Gpriyadharshini8148&theme=tokyonight&hide_border=true&background=0D1120&ring=4F8EF7&fire=2FFFB4&currStreakLabel=4F8EF7" style="width:100%;border-radius:8px;" loading="lazy" alt="Streak stats" onerror="this.style.display='none'"/>
    </div>
    <div style="margin-top:12px;padding:10px 12px;background:var(--surface2);border-radius:8px;border:1px solid rgba(255,217,61,0.15);">
      <div style="font-size:11px;color:var(--accent4);font-family:'JetBrains Mono',monospace;margin-bottom:3px;">⚡ Fun fact</div>
      <div style="font-size:12px;color:var(--muted);line-height:1.6;">I tune CNN hyperparameters the same way I debug APIs — methodically, with logs.</div>
    </div>
  </div>
</div>

<!-- ─── FOOTER ─── -->
<div class="footer">
  <div class="footer-title">Let's build something together</div>
  <div class="footer-sub">Open to backend development roles · SDE internships · Open source collaboration</div>
  <div class="footer-btns">
    <a class="fb primary" href="mailto:gpriyampt@gmail.com">✉ gpriyampt@gmail.com</a>
    <a class="fb linkedin" href="https://www.linkedin.com/in/priyadharshini-g-17bbaa27b" target="_blank">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      Connect on LinkedIn
    </a>
    <a class="fb secondary" href="https://github.com/Gpriyadharshini8148" target="_blank">⌥ GitHub</a>
  </div>
</div>

<!-- ─── README COPY ─── -->
<div class="copy-section">
  <div class="copy-header">
    <span class="copy-title">README.md — ready to paste into your GitHub profile repo</span>
    <button class="copy-btn" onclick="copyReadme()">📋 <span id="clbl">Copy markdown</span></button>
  </div>
  <textarea id="readme-md" readonly>
<h1 align="center">Hi, I'm Priyadharshini G 👋</h1>

<p align="center">
  <b>Backend & ML Engineer · CS'26 · Chennai, India</b><br>
  <i>"I build things that work in production — reliable APIs, accurate models, clean code."</i>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/priyadharshini-g-17bbaa27b"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white"/></a>&nbsp;
  <a href="mailto:gpriyampt@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=flat&logo=gmail&logoColor=white"/></a>&nbsp;
  <img src="https://komarev.com/ghpvc/?username=Gpriyadharshini8148&style=flat&color=4F8EF7" alt="views"/>
</p>

---

## ⚙️ Backend Engineering (Core Focus)

> Production-grade REST APIs · PostgreSQL · Docker · CI/CD

| | |
|---|---|
| 🔭 **Now** | SDE Intern @ **Cyces Innovation Lab**, Chennai |
| 🛠 **Backend** | Django REST · Flask · PostgreSQL · Docker · Kafka · Celery |
| 🧠 **ML/AI** | TensorFlow · Keras · OpenCV · MediaPipe · PyTorch |
| 🌱 **Learning** | System design · Kafka streams · AWS deployment |
| 💬 **Ask me** | APIs · CNNs · DB schema optimization |
| 📫 **Reach me** | gpriyampt@gmail.com |
| ⚡ **Fun fact** | I tune CNN hyperparameters the same way I debug APIs — methodically, with logs |

---

## 🛠 Tech Stack

**⚙️ Backend & API**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django_REST-092E20?style=flat&logo=django&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=flat&logo=celery&logoColor=white)

**🧠 ML / AI**
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat&logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![scikit-learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat&logoColor=white)

**🛠 Tools & Cloud**
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat&logo=postman&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Gpriyadharshini8148&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" height="160"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Gpriyadharshini8148&layout=compact&theme=tokyonight&hide_border=true" height="160"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=Gpriyadharshini8148&theme=tokyonight&hide_border=true" height="140"/>
</p>

---

## 💼 Experience

**⚙️ SDE Intern · Cyces Innovation Lab, Chennai** *(Jan 2026 – Present)*
→ Built 10+ RESTful APIs with Django REST Framework
→ PostgreSQL schema design; reduced query response time ~30%
→ Docker-based CI/CD workflows with Git feature branching

**🧠 ML Intern · NIT Puducherry, Karaikkal** *(May 2025 – Jun 2025)*
→ Built CNN models achieving 90%+ accuracy (TensorFlow, Keras)
→ Integrated models into Flask app, cutting inference latency 25%
→ OpenCV preprocessing pipelines for real-world image robustness

---

## 🚀 Featured Projects

### 🤟 AI Model for Assisting the Deaf
> Real-time two-way communication · MediaPipe + CNN · **95%+ gesture accuracy**
- Bidirectional deaf–hearing communication system
- Integrated speech-to-text, multilingual translation, and audio feedback
- Deployed via Flask with SQLite-backed session management

`Flask` `TensorFlow` `Keras` `MediaPipe` `OpenCV` `SQLite`

---

### 🫁 Pneumonia Detection using ML
> Binary chest X-ray classifier · **5,000+ images** · **92% test accuracy**
- CNN architecture with iterative hyperparameter tuning
- Automated OpenCV preprocessing pipeline
- Evaluated: precision, recall, F1-score, confusion matrix

`Python` `TensorFlow` `Keras` `Scikit-Learn` `OpenCV`

---

### ✈️ TravelGo — Android Travel Planner
> Itinerary creation · real-time weather · Firebase real-time sync
- Full-featured Android app with location-based recommendations
- Firebase authentication and real-time data sync

`Java` `XML` `Android Studio` `Firebase`

---

### 🗣️ Tanglish Sentiment & Emotion Analyser *(Final Year Thesis)*
> Code-mixed Tamil-English NLP · Hybrid CNN+LSTM+Transformer · **94% accuracy**
- Hybrid deep learning architecture: CNN + LSTM + Transformer (IndicBERT, XLM-R)
- Served trained models via Flask REST APIs
- Real-time React.js dashboard for sentiment & emotion visualization

`Flask` `React.js` `TensorFlow` `PyTorch` `IndicBERT` `XLM-R` `CNN+LSTM` `Twitter API` `MySQL` `NLP`

---

## 📈 By the Numbers

| Metric | Value |
|---|---|
| REST APIs shipped | 10+ |
| Best CNN accuracy | 95%+ |
| Thesis model accuracy | 94% |
| DB query speedup | ~30% |
| Inference latency cut | 25% |
| CGPA | 9.46 / 10 |

---

## 🏅 Certifications

- ☁️ **Cloud Computing** — NPTEL (IIT Kharagpur)
- 🌐 **Social Networks** — NPTEL
- 📊 **Data for Everyone** — Google Career Certificates
- 🔐 **Cybersecurity Analyst Simulation** — Tata Group (Forage)

---

<p align="center">
  <b>Open to backend development opportunities</b><br>
  <i>Let's build something reliable together.</i><br><br>
  <a href="mailto:gpriyampt@gmail.com"><img src="https://img.shields.io/badge/Say%20Hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/></a>
  <a href="https://www.linkedin.com/in/priyadharshini-g-17bbaa27b"><img src="https://img.shields.io/badge/Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
</p>
  </textarea>
</div>

</div><!-- /container -->

<script>
// ─── COMMIT DATA ───
const STORAGE_KEY = 'pg_commits_v1';

function loadData() {
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    return raw ? JSON.parse(raw) : {};
  } catch { return {}; }
}

function saveData(data) {
  try { localStorage.setItem(STORAGE_KEY, JSON.stringify(data)); } catch {}
}

// Seed some realistic commits if empty
function seedData() {
  const data = loadData();
  if (Object.keys(data).length > 0) return data;

  const today = new Date();
  const msgs = [
    ['feat: add user authentication endpoint','backend'],
    ['fix: resolve N+1 query in orders API','backend'],
    ['feat: PostgreSQL schema for analytics','backend'],
    ['chore: Dockerize dev environment','backend'],
    ['feat: Celery task for email async','backend'],
    ['fix: CNN model inference latency','ml'],
    ['feat: OpenCV preprocessing pipeline','ml'],
    ['feat: Flask route for model serving','backend'],
    ['docs: update API documentation','other'],
    ['refactor: optimise DB indexes','backend'],
    ['feat: Kafka consumer for events','backend'],
    ['test: add unit tests for auth','backend'],
  ];

  let i = 0;
  for (let d = 180; d >= 0; d -= Math.floor(Math.random() * 5 + 1)) {
    const date = new Date(today);
    date.setDate(date.getDate() - d);
    const key = dateKey(date);
    const count = Math.floor(Math.random() * 6) + 1;
    const m = msgs[i % msgs.length];
    data[key] = { count, msg: m[0], type: m[1] };
    i++;
  }
  saveData(data);
  return data;
}

function dateKey(d) {
  return d.toISOString().slice(0,10);
}

function todayKey() {
  return dateKey(new Date());
}

// ─── VIEW STATE ───
let currentView = 'year';
let commitData = seedData();

function setView(v) {
  currentView = v;
  document.getElementById('btn-year').classList.toggle('active', v === 'year');
  document.getElementById('btn-month').classList.toggle('active', v === 'month');
  renderGrid();
}

// ─── RENDER GRID ───
function renderGrid() {
  const grid = document.getElementById('contrib-grid');
  grid.innerHTML = '';
  const tooltip = document.getElementById('tooltip');

  const today = new Date();
  today.setHours(0,0,0,0);

  let days = currentView === 'year' ? 365 : 30;

  // For year view: start from Sunday of the week 365 days ago
  const startDate = new Date(today);
  startDate.setDate(startDate.getDate() - days);
  if (currentView === 'year') {
    // align to Sunday
    startDate.setDate(startDate.getDate() - startDate.getDay());
  }

  const totalDays = Math.round((today - startDate) / 86400000) + 1;

  if (currentView === 'year') {
    grid.style.gridTemplateRows = 'repeat(7, 13px)';
    for (let i = 0; i < totalDays; i++) {
      const d = new Date(startDate);
      d.setDate(d.getDate() + i);
      const key = dateKey(d);
      const entry = commitData[key];
      const count = entry ? entry.count : 0;
      const level = count === 0 ? 0 : count <= 1 ? 1 : count <= 3 ? 2 : count <= 5 ? 3 : 4;
      const cell = document.createElement('div');
      cell.className = `contrib-cell l${level}${key === todayKey() ? ' today' : ''}`;
      cell.addEventListener('mouseenter', e => {
        tooltip.style.display = 'block';
        tooltip.textContent = count > 0 ? `${count} commit${count>1?'s':''} · ${key}` : `No commits · ${key}`;
      });
      cell.addEventListener('mousemove', e => {
        tooltip.style.left = (e.clientX + 12) + 'px';
        tooltip.style.top = (e.clientY - 28) + 'px';
      });
      cell.addEventListener('mouseleave', () => { tooltip.style.display = 'none'; });
      grid.appendChild(cell);
    }
  } else {
    // Month view: single row
    grid.style.gridTemplateRows = '13px';
    for (let i = 0; i < 30; i++) {
      const d = new Date(today);
      d.setDate(d.getDate() - (29 - i));
      const key = dateKey(d);
      const entry = commitData[key];
      const count = entry ? entry.count : 0;
      const level = count === 0 ? 0 : count <= 1 ? 1 : count <= 3 ? 2 : count <= 5 ? 3 : 4;
      const cell = document.createElement('div');
      cell.className = `contrib-cell l${level}${key === todayKey() ? ' today' : ''}`;
      cell.style.width = '18px'; cell.style.height = '18px';
      cell.addEventListener('mouseenter', e => {
        tooltip.style.display = 'block';
        tooltip.textContent = count > 0 ? `${count} commit${count>1?'s':''} · ${key}` : `No commits · ${key}`;
      });
      cell.addEventListener('mousemove', e => {
        tooltip.style.left = (e.clientX + 12) + 'px';
        tooltip.style.top = (e.clientY - 28) + 'px';
      });
      cell.addEventListener('mouseleave', () => { tooltip.style.display = 'none'; });
      grid.appendChild(cell);
    }
  }

  updateStreaks();
  renderFeed();
  updateTodayChip();
}

function updateStreaks() {
  const today = new Date(); today.setHours(0,0,0,0);
  let current = 0, longest = 0, streak = 0, total = 0;

  // total
  Object.values(commitData).forEach(e => total += (e.count || 0));

  // current streak (backwards from today)
  for (let i = 0; i < 365; i++) {
    const d = new Date(today); d.setDate(d.getDate() - i);
    if (commitData[dateKey(d)]?.count > 0) { current++; }
    else { break; }
  }

  // longest streak
  const sorted = Object.keys(commitData).sort();
  let s = 0, prev = null;
  for (const k of sorted) {
    if (commitData[k].count > 0) {
      if (prev) {
        const diff = (new Date(k) - new Date(prev)) / 86400000;
        if (diff === 1) { s++; } else { s = 1; }
      } else { s = 1; }
      if (s > longest) longest = s;
      prev = k;
    }
  }

  document.getElementById('streak-current').textContent = current;
  document.getElementById('streak-longest').textContent = longest;
  document.getElementById('streak-total').textContent = total;
}

function renderFeed() {
  const feed = document.getElementById('commit-feed');
  const entries = Object.entries(commitData)
    .filter(([,v]) => v.count > 0)
    .sort((a,b) => b[0].localeCompare(a[0]))
    .slice(0, 8);

  feed.innerHTML = entries.map(([date, e]) => `
    <div class="commit-entry">
      <span class="commit-date">${date}</span>
      <span class="commit-msg">${e.msg || 'commit'}</span>
      <span class="commit-tag tag-${e.type || 'other'}">${e.type || 'other'}</span>
      <span class="commit-count">×${e.count}</span>
    </div>
  `).join('');
}

function updateTodayChip() {
  const chip = document.getElementById('commit-today-chip');
  const t = commitData[todayKey()];
  if (t && t.count > 0) {
    chip.textContent = `✓ ${t.count} today`;
    chip.style.display = 'inline-flex';
  } else {
    chip.style.display = 'none';
  }
}

// ─── LOG FORM ───
function toggleLogForm() {
  const f = document.getElementById('log-form');
  f.classList.toggle('open');
}

function logCommit() {
  const msg = document.getElementById('log-msg').value.trim() || 'commit';
  const count = parseInt(document.getElementById('log-count').value) || 1;
  const type = document.getElementById('log-type').value;
  const key = todayKey();

  if (commitData[key]) {
    commitData[key].count += count;
    commitData[key].msg = msg;
    commitData[key].type = type;
  } else {
    commitData[key] = { count, msg, type };
  }

  saveData(commitData);
  renderGrid();
  document.getElementById('log-msg').value = '';
  document.getElementById('log-count').value = '1';

  // flash feedback
  const btn = document.querySelector('.log-submit');
  btn.textContent = '✓ Committed!';
  btn.style.background = 'var(--accent2)';
  btn.style.color = '#0D1120';
  setTimeout(() => { btn.textContent = 'Commit →'; btn.style.background = ''; btn.style.color = ''; }, 1500);
}

// ─── TABS ───
function switchTab(panel, btn, style) {
  document.querySelectorAll('.tab-panel').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b => { b.classList.remove('active','backend','ml','tools'); });
  document.getElementById('tab-' + panel).classList.add('active');
  btn.classList.add('active', style);
}

// ─── COPY ───
function copyReadme() {
  const ta = document.getElementById('readme-md');
  ta.select();
  navigator.clipboard.writeText(ta.value).then(() => {
    document.getElementById('clbl').textContent = '✓ Copied!';
    setTimeout(() => document.getElementById('clbl').textContent = 'Copy markdown', 2000);
  });
}

// ─── INIT ───
document.addEventListener('DOMContentLoaded', () => {
  renderGrid();
});
</script>
</body>
</html>
