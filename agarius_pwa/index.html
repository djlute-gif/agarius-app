<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AGARIUS — Resonancia Total v3.0</title>
<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Orbitron:wght@400;700;900&display=swap" rel="stylesheet">
<style>
  :root {
    --cyan:   #00ffcc;
    --red:    #ff3300;
    --gold:   #ffcc00;
    --blue:   #0088ff;
    --purple: #cc00ff;
    --green:  #00ff44;
    --bg:     #030303;
    --panel:  #080808;
    --border: #1a1a1a;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--cyan);
    font-family: 'Share Tech Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Scanline overlay */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,255,204,0.015) 2px,
      rgba(0,255,204,0.015) 4px
    );
    pointer-events: none;
    z-index: 9999;
  }

  header {
    text-align: center;
    padding: 18px 0 10px;
    border-bottom: 1px solid #111;
    letter-spacing: 8px;
  }
  header h1 {
    font-family: 'Orbitron', sans-serif;
    font-size: 1.6rem;
    font-weight: 900;
    color: var(--cyan);
    text-shadow: 0 0 20px var(--cyan), 0 0 40px rgba(0,255,204,0.3);
  }
  header p { font-size: 0.65rem; color: #444; letter-spacing: 4px; margin-top: 4px; }

  /* ── MAIN LAYOUT ── */
  .layout {
    display: grid;
    grid-template-columns: 480px 1fr;
    grid-template-rows: auto auto;
    gap: 12px;
    padding: 12px;
    max-width: 1200px;
    margin: 0 auto;
  }

  /* ── AGARIUS NUCLEUS ── */
  #nucleus-wrap {
    grid-row: 1 / 3;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }

  #agarius-container {
    position: relative;
    width: 420px;
    height: 420px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    background: radial-gradient(circle, #050505 0%, #000 100%);
    border: 1px solid #111;
    flex-shrink: 0;
  }

  .anillo {
    position: absolute;
    border-radius: 50%;
    border: 1px solid rgba(0,255,204,0.08);
    transition: border-color 0.15s, transform 0.15s;
  }

  #core {
    width: 44px; height: 44px;
    background: #fff;
    border-radius: 50%;
    box-shadow: 0 0 30px #fff, 0 0 60px rgba(255,255,255,0.3);
    z-index: 10;
    transition: background 0.1s, box-shadow 0.1s;
    cursor: pointer;
  }

  /* ── OSCILOSCOPIO ── */
  #oscilo-wrap {
    width: 420px;
    background: var(--panel);
    border: 1px solid var(--border);
    padding: 8px;
  }
  #oscilo-label {
    font-size: 0.6rem;
    color: #333;
    letter-spacing: 3px;
    margin-bottom: 4px;
  }
  #osciloscopio { display: block; width: 100%; }

  /* ── SPECTRUM ── */
  #spectrum-wrap {
    width: 420px;
    background: var(--panel);
    border: 1px solid var(--border);
    padding: 8px;
  }
  #spectrum-label { font-size: 0.6rem; color: #333; letter-spacing: 3px; margin-bottom: 4px; }
  #spectrum { display: block; width: 100%; }

  /* ── RIGHT PANEL ── */
  .right-panel { display: flex; flex-direction: column; gap: 10px; }

  /* ── MONITOR ── */
  #monitor-raid {
    background: var(--panel);
    border: 1px solid var(--border);
    border-left: 3px solid var(--cyan);
    padding: 10px 12px;
    height: 160px;
    overflow-y: auto;
    font-size: 0.72rem;
    line-height: 1.6;
  }
  #monitor-raid::-webkit-scrollbar { width: 4px; }
  #monitor-raid::-webkit-scrollbar-thumb { background: #222; }
  .log-ok   { color: var(--cyan); }
  .log-warn { color: var(--gold); }
  .log-err  { color: var(--red);  border-left: 2px solid var(--red); padding-left: 6px; }
  .log-hi   { color: #fff; text-shadow: 0 0 8px var(--cyan); }

  /* ── CONTROLES PRINCIPALES ── */
  #main-controls {
    background: var(--panel);
    border: 1px solid var(--border);
    padding: 12px;
  }
  .section-title {
    font-size: 0.6rem;
    color: #333;
    letter-spacing: 4px;
    margin-bottom: 8px;
    border-bottom: 1px solid #111;
    padding-bottom: 4px;
  }

  /* ── TECLADO NOTAS ── */
  #teclado {
    display: grid;
    grid-template-columns: repeat(8, 1fr);
    gap: 5px;
    margin-bottom: 10px;
  }

  .key {
    background: #000;
    border: 1px solid var(--cyan);
    color: var(--cyan);
    padding: 12px 4px;
    cursor: pointer;
    font-family: 'Orbitron', sans-serif;
    font-size: 0.65rem;
    font-weight: 700;
    text-align: center;
    transition: all 0.08s;
    user-select: none;
  }
  .key:hover  { background: rgba(0,255,204,0.1); }
  .key:active, .key.active { background: var(--cyan); color: #000; box-shadow: 0 0 15px var(--cyan); }
  .key.sharp  { border-color: var(--gold); color: var(--gold); }
  .key.sharp:active, .key.sharp.active { background: var(--gold); color: #000; box-shadow: 0 0 15px var(--gold); }

  /* ── ONDAS ── */
  #wave-selector {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 5px;
    margin-bottom: 10px;
  }
  .wave-btn {
    background: #000;
    border: 1px solid #333;
    color: #555;
    padding: 8px;
    cursor: pointer;
    font-family: 'Share Tech Mono', monospace;
    font-size: 0.7rem;
    text-align: center;
    transition: all 0.1s;
  }
  .wave-btn.active { border-color: var(--cyan); color: var(--cyan); background: rgba(0,255,204,0.08); }
  .wave-btn:hover  { border-color: #555; color: #888; }

  /* ── EFECTOS ── */
  #efectos {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 5px;
    margin-bottom: 10px;
  }
  .fx-btn {
    background: #000;
    border: 1px solid #222;
    color: #444;
    padding: 9px 4px;
    cursor: pointer;
    font-size: 0.65rem;
    text-align: center;
    transition: all 0.1s;
    font-family: 'Share Tech Mono', monospace;
  }
  .fx-btn.active { border-color: var(--purple); color: var(--purple); background: rgba(204,0,255,0.06); }
  .fx-btn:hover  { border-color: #444; color: #666; }

  /* ── SLIDERS ── */
  .sliders-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 8px;
    margin-bottom: 10px;
  }
  .slider-wrap label {
    display: block;
    font-size: 0.58rem;
    color: #444;
    letter-spacing: 2px;
    margin-bottom: 3px;
  }
  .slider-wrap span { color: var(--cyan); font-size: 0.65rem; }
  input[type=range] {
    width: 100%;
    accent-color: var(--cyan);
    height: 3px;
    cursor: pointer;
  }

  /* ── BOTONES ACCIÓN ── */
  #action-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 6px;
  }
  .action-btn {
    background: #000;
    border: 1px solid;
    padding: 12px 6px;
    cursor: pointer;
    font-family: 'Orbitron', sans-serif;
    font-size: 0.6rem;
    font-weight: 700;
    letter-spacing: 1px;
    transition: all 0.1s;
  }
  .action-btn.cyan   { border-color: var(--cyan);   color: var(--cyan);   }
  .action-btn.red    { border-color: var(--red);    color: var(--red);    }
  .action-btn.green  { border-color: var(--green);  color: var(--green);  }
  .action-btn.gold   { border-color: var(--gold);   color: var(--gold);   }
  .action-btn.blue   { border-color: var(--blue);   color: var(--blue);   }
  .action-btn.purple { border-color: var(--purple); color: var(--purple); }
  .action-btn:hover  { filter: brightness(1.4); }
  .action-btn:active { filter: brightness(2); transform: scale(0.97); }

  /* ── SEQUENCER ── */
  #sequencer-wrap {
    background: var(--panel);
    border: 1px solid var(--border);
    padding: 12px;
  }
  #seq-grid {
    display: grid;
    grid-template-columns: repeat(16, 1fr);
    gap: 3px;
    margin-bottom: 8px;
  }
  .seq-cell {
    height: 28px;
    background: #0a0a0a;
    border: 1px solid #1a1a1a;
    cursor: pointer;
    transition: background 0.1s;
    border-radius: 2px;
  }
  .seq-cell.on   { background: var(--cyan); box-shadow: 0 0 6px var(--cyan); }
  .seq-cell.beat { border-color: #2a2a2a; }
  .seq-cell.playing { outline: 2px solid var(--gold); }

  #seq-controls { display: flex; gap: 8px; align-items: center; }
  #seq-controls select, #seq-controls input[type=range] { flex: 1; }
  #seq-bpm-val { color: var(--gold); font-size: 0.7rem; min-width: 50px; }

  /* ── STATUS BAR ── */
  #status-bar {
    display: flex;
    gap: 20px;
    padding: 6px 12px;
    background: #050505;
    border-top: 1px solid #0f0f0f;
    font-size: 0.6rem;
    color: #333;
    letter-spacing: 2px;
  }
  #status-bar span { color: var(--cyan); }

  /* ── ANIMACIONES ── */
  @keyframes pulse-ring {
    0%   { transform: scale(1);    opacity: 0.5; }
    50%  { transform: scale(1.04); opacity: 1;   }
    100% { transform: scale(1);    opacity: 0.5; }
  }
  .ring-pulse { animation: pulse-ring 0.3s ease; }

  @keyframes glow-core {
    0%   { box-shadow: 0 0 30px currentColor; }
    50%  { box-shadow: 0 0 80px currentColor, 0 0 120px currentColor; }
    100% { box-shadow: 0 0 30px currentColor; }
  }



  /* ── SECUENCIADOR MELÓDICO ── */
  #sequencer-wrap { background: var(--panel); border: 1px solid var(--border); padding: 12px; }

  #seq-note-row {
    display: grid;
    grid-template-columns: repeat(16, 1fr);
    gap: 2px;
    margin-bottom: 2px;
  }
  .seq-note-label {
    font-size: 0.5rem;
    text-align: center;
    color: #444;
    letter-spacing: 0;
    padding: 2px 0;
    cursor: pointer;
    border: 1px solid #111;
    background: #050505;
    transition: color 0.1s, border-color 0.1s;
    user-select: none;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .seq-note-label:hover { color: var(--cyan); border-color: #333; }
  .seq-note-label.has-note { color: var(--cyan); }

  #seq-piano-roll {
    display: grid;
    grid-template-columns: repeat(16, 1fr);
    gap: 2px;
    margin-bottom: 2px;
  }
  .seq-pitch-col {
    display: flex;
    flex-direction: column;
    gap: 2px;
  }
  .seq-pitch-cell {
    height: 14px;
    background: #080808;
    border: 1px solid #111;
    cursor: pointer;
    transition: background 0.08s;
    border-radius: 1px;
    position: relative;
  }
  .seq-pitch-cell:hover { background: #1a1a1a; }
  .seq-pitch-cell.selected {
    background: var(--cyan);
    box-shadow: 0 0 6px var(--cyan);
  }
  .seq-pitch-cell.is-sharp { background: #0d0d0d; }
  .seq-pitch-cell.is-sharp.selected { background: var(--gold); box-shadow: 0 0 6px var(--gold); }
  .seq-pitch-cell.playing-cell { outline: 2px solid #fff; }

  #seq-active-row {
    display: grid;
    grid-template-columns: repeat(16, 1fr);
    gap: 2px;
    margin-bottom: 8px;
  }
  .seq-active-btn {
    height: 20px;
    background: #0a0a0a;
    border: 1px solid #1a1a1a;
    cursor: pointer;
    border-radius: 2px;
    transition: all 0.08s;
    position: relative;
  }
  .seq-active-btn.on {
    background: rgba(0,255,204,0.15);
    border-color: var(--cyan);
  }
  .seq-active-btn.playing { outline: 2px solid var(--gold); }
  .seq-active-btn .step-num {
    position: absolute;
    top: 2px; left: 0; right: 0;
    text-align: center;
    font-size: 0.45rem;
    color: #333;
  }

  #seq-controls {
    display: flex;
    gap: 8px;
    align-items: center;
    flex-wrap: wrap;
    margin-bottom: 6px;
  }
  #seq-scale-row {
    display: flex;
    align-items: center;
    gap: 8px;
    flex-wrap: wrap;
  }


  /* ── HZ PANEL ── */
  #hz-panel { background:#050505; border:1px solid #1a1a1a; padding:10px; margin-bottom:10px; }
  .hz-range-row { display:flex; align-items:center; gap:8px; margin-bottom:6px; }
  .hz-zone { font-size:0.55rem; letter-spacing:2px; min-width:58px; text-align:center;
    padding:3px 6px; border:1px solid currentColor; }
  .hz-main-slider-wrap { flex:1; position:relative; }
  #hz-bar-bg { display:flex; height:3px; margin-top:2px; border-radius:2px; overflow:hidden; }
  #hz-bar-zone-audio { flex:300;  background:rgba(0,255,204,0.4); }
  #hz-bar-zone-mid   { flex:3700; background:rgba(0,136,255,0.4); }
  #hz-bar-zone-high  { flex:16000;background:rgba(204,0,255,0.3); }
  #hz-bar-zone-ultra { flex:4000; background:rgba(255,51,0,0.5);  }
  .hz-readout { text-align:right; min-width:70px; }
  #hz-val-big { font-family:'Orbitron',sans-serif; font-size:1.1rem; font-weight:700; color:var(--cyan); }
  #hz-unit    { font-size:0.6rem; color:#555; margin-left:2px; }
  .hz-fine-row { display:flex; align-items:center; gap:6px; margin-bottom:6px; }
  .hz-btn { background:#000; border:1px solid #333; color:#666; padding:4px 8px;
    font-family:'Share Tech Mono',monospace; font-size:0.6rem; cursor:pointer; }
  .hz-btn:hover { border-color:var(--cyan); color:var(--cyan); }
  .hz-btn.active { border-color:var(--red); color:var(--red); }
  .hz-presets { display:flex; flex-wrap:wrap; gap:4px; align-items:center; }
  .hz-preset { background:#000; border:1px solid #222; color:#555; padding:4px 7px;
    font-family:'Share Tech Mono',monospace; font-size:0.6rem; cursor:pointer; border-radius:2px; }
  .hz-preset:hover { border-color:#555; color:#888; }
  .hz-preset.ultra { border-color:#330000; color:#ff3300; opacity:0.7; }
  .hz-preset.ultra:hover { opacity:1; border-color:var(--red); }

  /* ── CHORD PANEL ── */
  #chord-panel { background:#050505; border:1px solid #1a1a1a; padding:10px; margin-bottom:10px; }
  #chord-root-row, #chord-type-row { display:flex; align-items:center; gap:6px; margin-bottom:6px; flex-wrap:wrap; }
  #chord-roots, #chord-types { display:flex; gap:3px; flex-wrap:wrap; flex:1; }
  .chord-root-btn {
    background:#000; border:1px solid #1a1a1a; color:#444;
    padding:5px 7px; font-family:'Share Tech Mono',monospace; font-size:0.62rem;
    cursor:pointer; transition:all 0.08s; min-width:28px; text-align:center;
  }
  .chord-root-btn:hover { border-color:#444; color:#777; }
  .chord-root-btn.active { border-color:var(--cyan); color:var(--cyan); background:rgba(0,255,204,0.08); }
  .chord-root-btn.sharp { border-color:#222; color:#333; }
  .chord-root-btn.sharp.active { border-color:var(--gold); color:var(--gold); background:rgba(255,204,0,0.08); }

  .chord-type-btn {
    background:#000; border:1px solid #1a1a1a; color:#444;
    padding:5px 8px; font-family:'Share Tech Mono',monospace; font-size:0.58rem;
    cursor:pointer; transition:all 0.08s; text-align:center; white-space:nowrap;
  }
  .chord-type-btn:hover { border-color:#444; color:#777; }
  .chord-type-btn.active { border-color:var(--purple); color:var(--purple); background:rgba(204,0,255,0.08); }

  #chord-action-row { display:flex; gap:6px; align-items:center; margin-bottom:6px; flex-wrap:wrap; }
  .chord-play-btn {
    background:#000; border:1px solid var(--green); color:var(--green);
    padding:8px 12px; font-family:'Orbitron',sans-serif; font-size:0.6rem; font-weight:700;
    cursor:pointer; transition:all 0.1s; letter-spacing:1px;
  }
  .chord-play-btn:hover { background:var(--green); color:#000; }
  .chord-play-btn.arp { border-color:var(--blue); color:var(--blue); }
  .chord-play-btn.arp:hover { background:var(--blue); color:#000; }
  .chord-play-btn.inv { border-color:var(--gold); color:var(--gold); }
  .chord-play-btn.inv:hover { background:var(--gold); color:#000; }

  #chord-display {
    font-size:0.65rem; color:#555; letter-spacing:2px; padding:4px 0;
    border-top:1px solid #111; margin-top:2px;
  }

  /* ── JACK PANEL ── */
  #jack-panel { display: flex; flex-direction: column; gap: 8px; margin-bottom: 10px; }
  #jack-diagram { background: #050505; border: 1px solid #111; padding: 8px 12px; }
  #jack-controls { display: flex; flex-direction: column; gap: 6px; }
  .jack-block { background: #050505; border: 1px solid #1a1a1a; padding: 8px 10px; transition: border-color 0.2s; }
  .jack-block.active-block { border-color: var(--cyan); }
  .jack-block-title { font-size: 0.62rem; color: #555; letter-spacing: 2px; margin-bottom: 6px; }
  .jack-row { display: flex; align-items: center; gap: 8px; }
  .jack-toggle { background: #000; border: 1px solid var(--cyan); color: var(--cyan); padding: 6px 10px;
    font-family: 'Share Tech Mono', monospace; font-size: 0.65rem; cursor: pointer; white-space: nowrap;
    transition: all 0.1s; min-width: 110px; text-align: center; }
  .jack-toggle.off { border-color: #333; color: #444; }
  .jack-toggle:hover { filter: brightness(1.4); }
  .jack-slider-wrap { display: flex; align-items: center; gap: 6px; flex: 1; font-size: 0.6rem; color: #444; }
  .jack-slider-wrap input[type=range] { flex: 1; accent-color: var(--cyan); }
  .jack-val { color: var(--cyan); min-width: 32px; text-align: right; }
  .jack-meter-wrap { display: flex; align-items: center; gap: 4px; margin-top: 5px; height: 8px; }
  .jack-meter-label { font-size: 0.55rem; color: #333; min-width: 12px; }
  .jack-meter-bar { flex: 1; height: 6px; background: #0a0a0a; border: 1px solid #111; overflow: hidden; }
  .jack-meter-fill { height: 100%; width: 0%; transition: width 0.05s; }
  .jack-meter-fill.cyan { background: var(--cyan); box-shadow: 0 0 4px var(--cyan); }
  .jack-meter-fill.red  { background: var(--red);  box-shadow: 0 0 4px var(--red);  }

  /* Responsive mobile */
  @media (max-width: 900px) {
    .layout { grid-template-columns: 1fr; }
    #nucleus-wrap { grid-row: auto; }
    #agarius-container { width: 320px; height: 320px; }
    #oscilo-wrap, #spectrum-wrap { width: 320px; }
  }
</style>
</head>
<body>

<header>
  <h1>AGARIUS</h1>
  <p>RESONANCIA TOTAL v3.0 — SYNESLINK KERNEL</p>
</header>

<div class="layout">

  <!-- ══ NÚCLEO VISUAL ══ -->
  <div id="nucleus-wrap">
    <div id="agarius-container">
      <div id="core"></div>
    </div>

    <div id="oscilo-wrap">
      <div id="oscilo-label">OSCILOSCOPIO — DOMINIO TEMPORAL</div>
      <canvas id="osciloscopio" width="404" height="80"></canvas>
    </div>

    <div id="spectrum-wrap">
      <div id="spectrum-label">ESPECTRO — DOMINIO FRECUENCIAL</div>
      <canvas id="spectrum" width="404" height="80"></canvas>
    </div>
  </div>

  <!-- ══ PANEL DERECHO ══ -->
  <div class="right-panel">

    <!-- Monitor -->
    <div id="monitor-raid">
      <div class="log-ok">> AGARIUS_KERNEL v3.0 INICIADO</div>
      <div class="log-ok">> SISTEMA LISTO — HAZ CLICK PARA ACTIVAR AUDIO</div>
    </div>

    <!-- Controles principales -->
    <div id="main-controls">

      <div class="section-title">TECLADO CROMÁTICO — 2 OCTAVAS</div>
      <div id="teclado"></div>

      <div class="section-title">FORMA DE ONDA</div>
      <div id="wave-selector">
        <div class="wave-btn active" data-wave="sine">SENO</div>
        <div class="wave-btn" data-wave="square">CUAD</div>
        <div class="wave-btn" data-wave="sawtooth">SIERRA</div>
        <div class="wave-btn" data-wave="triangle">TRIANG</div>
      </div>

      <div class="section-title">EFECTOS</div>
      <div id="efectos">
        <div class="fx-btn" id="fx-reverb">REVERB</div>
        <div class="fx-btn" id="fx-delay">DELAY</div>
        <div class="fx-btn" id="fx-distort">DISTORT</div>
        <div class="fx-btn" id="fx-flanger">FLANGER</div>
        <div class="fx-btn" id="fx-lpf">FILTRO LP</div>
        <div class="fx-btn" id="fx-hpf">FILTRO HP</div>
      </div>

      <div class="section-title">PARÁMETROS</div>
      <div class="sliders-grid">
        <div class="slider-wrap">
          <label>VOLUMEN: <span id="vol-val">70</span>%</label>
          <input type="range" id="slider-vol" min="0" max="100" value="70">
        </div>
        <div class="slider-wrap">
          <label>DURACIÓN: <span id="dur-val">0.8</span>s</label>
          <input type="range" id="slider-dur" min="1" max="30" value="8">
        </div>
        <div class="slider-wrap">
          <label>ATAQUE: <span id="atk-val">0.01</span>s</label>
          <input type="range" id="slider-atk" min="1" max="20" value="1">
        </div>
        <div class="slider-wrap">
          <label>OCTAVA: <span id="oct-val">4</span></label>
          <input type="range" id="slider-oct" min="2" max="7" value="4">
        </div>
      </div>

      <!-- ══ CONTROL DE FRECUENCIA DIRECTA ══ -->
      <div class="section-title">🔬 FRECUENCIA DIRECTA — AUDIBLE → ULTRASÓNICO</div>
      <div id="hz-panel">
        <div class="hz-range-row">
          <div class="hz-zone" id="hz-zone-label">AUDIBLE</div>
          <div class="hz-main-slider-wrap">
            <input type="range" id="slider-hz" min="1" max="24000" value="440" step="1"
                   oninput="onHzSlider(this.value)" style="width:100%;accent-color:var(--cyan);">
            <div id="hz-bar-bg">
              <div id="hz-bar-zone-audio"  title="Graves 20-300Hz"></div>
              <div id="hz-bar-zone-mid"    title="Medios 300-4kHz"></div>
              <div id="hz-bar-zone-high"   title="Agudos 4-20kHz"></div>
              <div id="hz-bar-zone-ultra"  title="Ultrasónico 20-24kHz"></div>
            </div>
          </div>
          <div class="hz-readout">
            <span id="hz-val-big">440</span>
            <span id="hz-unit">Hz</span>
          </div>
        </div>
        <div class="hz-fine-row">
          <span style="color:#444;font-size:0.58rem;letter-spacing:2px;">FINO:</span>
          <input type="range" id="slider-hz-fine" min="-50" max="50" value="0" step="0.1"
                 oninput="onHzFine(this.value)" style="flex:1;accent-color:var(--gold);">
          <span id="hz-fine-val" style="color:var(--gold);font-size:0.6rem;min-width:40px;">±0 Hz</span>
          <button class="hz-btn" onclick="resetHzFine()">RESET</button>
          <button class="hz-btn" id="hz-play-btn" onclick="toggleHzContinuo()">▶ EMIT</button>
        </div>
        <div class="hz-presets">
          <span style="color:#444;font-size:0.55rem;letter-spacing:2px;">PRESETS:</span>
          <button class="hz-preset" onclick="setHz(20)"    title="Infrasonido límite">20</button>
          <button class="hz-preset" onclick="setHz(40)"    title="Sub-bass">40</button>
          <button class="hz-preset" onclick="setHz(110)"   title="La2">110</button>
          <button class="hz-preset" onclick="setHz(220)"   title="La3">220</button>
          <button class="hz-preset" onclick="setHz(432)"   title="La432 - afinación alternativa">432</button>
          <button class="hz-preset" onclick="setHz(440)"   title="La4 estándar">440</button>
          <button class="hz-preset" onclick="setHz(528)"   title="Mi5 - frecuencia solfeggio">528</button>
          <button class="hz-preset" onclick="setHz(741)"   title="Sol5">741</button>
          <button class="hz-preset" onclick="setHz(963)"   title="Si5">963</button>
          <button class="hz-preset" onclick="setHz(1000)"  title="1 kHz">1k</button>
          <button class="hz-preset" onclick="setHz(4000)"  title="4 kHz">4k</button>
          <button class="hz-preset" onclick="setHz(8000)"  title="8 kHz">8k</button>
          <button class="hz-preset" onclick="setHz(16000)" title="16 kHz">16k</button>
          <button class="hz-preset ultra" onclick="setHz(18000)" title="Inicio zona ultrasónica">18k</button>
          <button class="hz-preset ultra" onclick="setHz(20000)" title="Límite audición humana">20k</button>
          <button class="hz-preset ultra" onclick="setHz(22000)" title="Ultrasónico">22k</button>
          <button class="hz-preset ultra" onclick="setHz(24000)" title="Máximo hardware típico">24k</button>
        </div>
      </div>

      <!-- ══ PANEL JACK TRRS ══ -->
      <div class="section-title">🔌 CONECTOR JACK TRRS — ENTRADA / SALIDA</div>
      <div id="jack-panel">
        <div id="jack-diagram">
          <svg viewBox="0 0 260 48" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:48px;">
            <rect x="0" y="16" width="220" height="16" rx="8" fill="#111" stroke="#333" stroke-width="1"/>
            <rect x="220" y="20" width="30" height="8" rx="4" fill="#555"/>
            <rect x="58"  y="14" width="6" height="20" fill="#1a1a1a"/>
            <rect x="98"  y="14" width="6" height="20" fill="#1a1a1a"/>
            <rect x="138" y="14" width="6" height="20" fill="#1a1a1a"/>
            <text x="35"  y="11" fill="#00ffcc" font-size="7" font-family="monospace" text-anchor="middle">L-OUT</text>
            <text x="78"  y="11" fill="#00ffcc" font-size="7" font-family="monospace" text-anchor="middle">R-OUT</text>
            <text x="118" y="11" fill="#555"    font-size="7" font-family="monospace" text-anchor="middle">GND</text>
            <text x="158" y="11" fill="#ff3300" font-size="7" font-family="monospace" text-anchor="middle">MIC-IN</text>
            <circle id="dot-out-l" cx="35"  cy="38" r="3" fill="#1a1a1a"/>
            <circle id="dot-out-r" cx="78"  cy="38" r="3" fill="#1a1a1a"/>
            <circle id="dot-mic"   cx="158" cy="38" r="3" fill="#1a1a1a"/>
          </svg>
        </div>
        <div id="jack-controls">
          <div class="jack-block" id="blk-out">
            <div class="jack-block-title">📤 SALIDA AURICULARES</div>
            <div class="jack-row">
              <button class="jack-toggle" id="btn-out" onclick="toggleSalida()">● ACTIVO</button>
              <div class="jack-slider-wrap">
                <span>VOL OUT</span>
                <input type="range" id="jack-vol-out" min="0" max="100" value="70" oninput="setVolOut(this.value)">
                <span id="jack-vol-out-val" class="jack-val">70%</span>
              </div>
            </div>
            <div class="jack-meter-wrap">
              <div class="jack-meter-label">L</div>
              <div class="jack-meter-bar"><div class="jack-meter-fill cyan" id="meter-out-l"></div></div>
              <div class="jack-meter-label">R</div>
              <div class="jack-meter-bar"><div class="jack-meter-fill cyan" id="meter-out-r"></div></div>
            </div>
          </div>
          <div class="jack-block" id="blk-in">
            <div class="jack-block-title">📥 ENTRADA MIC JACK</div>
            <div class="jack-row">
              <button class="jack-toggle off" id="btn-mic" onclick="toggleEntrada()">○ INACTIVO</button>
              <div class="jack-slider-wrap">
                <span>GAIN IN</span>
                <input type="range" id="jack-gain-in" min="0" max="300" value="100" oninput="setGainIn(this.value)">
                <span id="jack-gain-in-val" class="jack-val">100%</span>
              </div>
            </div>
            <div class="jack-meter-wrap">
              <div class="jack-meter-label">IN</div>
              <div class="jack-meter-bar" style="flex:1"><div class="jack-meter-fill red" id="meter-in"></div></div>
            </div>
            <div class="jack-row" style="margin-top:6px;">
              <button class="jack-toggle off" id="btn-thru" onclick="toggleThru()">○ MONITOR THRU</button>
              <div class="jack-slider-wrap">
                <span>THRU VOL</span>
                <input type="range" id="jack-thru-vol" min="0" max="100" value="50" oninput="setThruVol(this.value)">
                <span id="jack-thru-val" class="jack-val">50%</span>
              </div>
            </div>
          </div>
          <div class="jack-block" id="blk-simul">
            <div class="jack-block-title">⚡ MODO SIMULTÁNEO — EMITIR + ESCUCHAR</div>
            <div class="jack-row">
              <button class="jack-toggle off" id="btn-simul" onclick="toggleSimultaneo()">○ DESACTIVADO</button>
              <span style="font-size:0.62rem;color:#555;flex:1;padding-left:8px;">Activa salida Y entrada al mismo tiempo por el jack TRRS</span>
            </div>
            <div id="simul-status" style="font-size:0.6rem;color:#333;margin-top:4px;letter-spacing:1px;">— ESPERANDO ACTIVACIÓN —</div>
          </div>
        </div>
      </div>

      <!-- ══ PANEL DE ACORDES ══ -->
      <div class="section-title">🎸 ACORDES — RAÍZ + TIPO</div>
      <div id="chord-panel">
        <div id="chord-root-row">
          <span style="font-size:0.58rem;color:#444;letter-spacing:2px;">RAÍZ:</span>
          <div id="chord-roots"></div>
        </div>
        <div id="chord-type-row">
          <span style="font-size:0.58rem;color:#444;letter-spacing:2px;">TIPO:</span>
          <div id="chord-types"></div>
        </div>
        <div id="chord-action-row">
          <button class="chord-play-btn" onclick="tocarAcorde()">▶ TOCAR ACORDE</button>
          <button class="chord-play-btn arp" onclick="tocarAcordeArpegio()">〰 ARPEGIO</button>
          <button class="chord-play-btn inv" onclick="tocarAcordeInversion()">↕ INVERSIÓN</button>
          <div style="display:flex;align-items:center;gap:6px;margin-left:auto;">
            <span style="font-size:0.58rem;color:#444;">OCT</span>
            <select id="chord-oct" style="background:#000;border:1px solid #333;color:var(--cyan);padding:3px;font-family:'Share Tech Mono',monospace;font-size:0.65rem;">
              <option value="2">2</option>
              <option value="3">3</option>
              <option value="4" selected>4</option>
              <option value="5">5</option>
            </select>
          </div>
        </div>
        <div id="chord-display">— SELECCIONA RAÍZ Y TIPO —</div>
      </div>

      <div class="section-title">ACCIONES RÁPIDAS</div>
      <div id="action-row">
        <button class="action-btn red"    onclick="emitirDisonancia()">⚡ DISONANCIA</button>
        <button class="action-btn blue"   onclick="arpegio()">🌊 ARPEGIO</button>
        <button class="action-btn purple" onclick="barrido()">〰 BARRIDO</button>
        <button class="action-btn cyan"   onclick="toggleSimultaneo()">🔌 JACK DUAL</button>
      </div>
    </div>

    <!-- Secuenciador Melódico -->
    <div id="sequencer-wrap">
      <div class="section-title">SECUENCIADOR MELÓDICO — 16 PASOS</div>

      <!-- Cabecera de notas por paso -->
      <div id="seq-note-row"></div>

      <!-- Cuadrícula de pasos (piano roll simplificado) -->
      <div id="seq-piano-roll"></div>

      <!-- Fila de activación ON/OFF por paso -->
      <div id="seq-active-row"></div>

      <!-- Controles -->
      <div id="seq-controls">
        <div style="display:flex;align-items:center;gap:6px;flex:1;">
          <span style="font-size:0.6rem;color:#444;letter-spacing:2px;">BPM</span>
          <input type="range" id="seq-bpm" min="40" max="220" value="120" style="flex:1;">
          <span id="seq-bpm-val" style="color:var(--gold);font-size:0.7rem;min-width:55px;">120 BPM</span>
        </div>
        <div style="display:flex;align-items:center;gap:6px;flex:1;">
          <span style="font-size:0.6rem;color:#444;letter-spacing:2px;">PASOS</span>
          <input type="range" id="seq-steps" min="4" max="16" value="16" style="flex:1;">
          <span id="seq-steps-val" style="color:var(--cyan);font-size:0.7rem;min-width:30px;">16</span>
        </div>
        <button class="action-btn green" id="seq-play-btn" onclick="toggleSequencer()" style="padding:8px 14px;font-size:0.6rem;">▶ PLAY</button>
        <button class="action-btn gold"  onclick="randomizeMelody()" style="padding:8px 14px;font-size:0.6rem;">🎲 RANDOM</button>
        <button class="action-btn red"   onclick="clearSeq()" style="padding:8px 14px;font-size:0.6rem;">✕ CLEAR</button>
      </div>

      <!-- Selector de escala -->
      <div id="seq-scale-row">
        <span style="font-size:0.6rem;color:#444;letter-spacing:2px;">ESCALA:</span>
        <select id="seq-scale" onchange="aplicarEscala()" style="background:#000;border:1px solid #333;color:var(--cyan);padding:4px 6px;font-family:'Share Tech Mono',monospace;font-size:0.65rem;">
          <option value="cromática">CROMÁTICA</option>
          <option value="mayor" selected>MAYOR</option>
          <option value="menor">MENOR NAT.</option>
          <option value="pentatonica">PENTATÓNICA</option>
          <option value="blues">BLUES</option>
          <option value="dórica">DÓRICA</option>
          <option value="frigia">FRIGIA</option>
        </select>
        <span style="font-size:0.6rem;color:#444;letter-spacing:2px;">RAÍZ:</span>
        <select id="seq-root" onchange="aplicarEscala()" style="background:#000;border:1px solid #333;color:var(--cyan);padding:4px 6px;font-family:'Share Tech Mono',monospace;font-size:0.65rem;">
          <option value="0">DO</option>
          <option value="1">DO#</option>
          <option value="2">RE</option>
          <option value="3">RE#</option>
          <option value="4">MI</option>
          <option value="5">FA</option>
          <option value="6">FA#</option>
          <option value="7" selected>SOL</option>
          <option value="8">SOL#</option>
          <option value="9">LA</option>
          <option value="10">LA#</option>
          <option value="11">SI</option>
        </select>
        <span style="font-size:0.6rem;color:#444;letter-spacing:2px;">OCT:</span>
        <select id="seq-oct-base" style="background:#000;border:1px solid #333;color:var(--cyan);padding:4px 6px;font-family:'Share Tech Mono',monospace;font-size:0.65rem;">
          <option value="3">3</option>
          <option value="4" selected>4</option>
          <option value="5">5</option>
        </select>
      </div>
    </div>

  </div><!-- .right-panel -->
</div><!-- .layout -->

<div id="status-bar">
  <div>AUDIO: <span id="st-audio">INACTIVO</span></div>
  <div>MIC: <span id="st-mic">OFF</span></div>
  <div>ONDA: <span id="st-wave">SINE</span></div>
  <div>FX: <span id="st-fx">NINGUNO</span></div>
  <div>NOTA: <span id="st-nota">—</span></div>
  <div>FREQ: <span id="st-freq">— Hz</span></div>
  <div>SEQ: <span id="st-seq">PARADO</span></div>
</div>

<script>
// ══════════════════════════════════════════
//  AGARIUS KERNEL v3.0
// ══════════════════════════════════════════

let audioCtx, analyzerNode, micSource, dataArray, freqArray;
let masterGain, reverbNode, delayNode, distortNode, flangerNode, lpfNode, hpfNode;
let seqInterval = null, seqStep = 0, seqRunning = false;

// Estado
const state = {
  wave:    'sine',
  volume:  0.7,
  duration:0.8,
  attack:  0.01,
  octave:  4,
  fx:      { reverb: false, delay: false, distort: false, flanger: false, lpf: false, hpf: false }
};

// ── NOTAS CROMÁTICAS (2 octavas desde C3) ──
const NOTAS = [
  { name:'C',  freq:130.81, sharp:false },
  { name:'C#', freq:138.59, sharp:true  },
  { name:'D',  freq:146.83, sharp:false },
  { name:'D#', freq:155.56, sharp:true  },
  { name:'E',  freq:164.81, sharp:false },
  { name:'F',  freq:174.61, sharp:false },
  { name:'F#', freq:185.00, sharp:true  },
  { name:'G',  freq:196.00, sharp:false },
  { name:'G#', freq:207.65, sharp:true  },
  { name:'A',  freq:220.00, sharp:false },
  { name:'A#', freq:233.08, sharp:true  },
  { name:'B',  freq:246.94, sharp:false },
  { name:'C2', freq:261.63, sharp:false },
  { name:'D2', freq:293.66, sharp:false },
  { name:'E2', freq:329.63, sharp:false },
  { name:'G2', freq:392.00, sharp:false },
];

// ── CONSTRUIR TECLADO ──
const tecladoEl = document.getElementById('teclado');
NOTAS.forEach(nota => {
  const btn = document.createElement('div');
  btn.className = 'key' + (nota.sharp ? ' sharp' : '');
  btn.textContent = nota.name;
  btn.dataset.freq = nota.freq;
  btn.dataset.name = nota.name;
  btn.addEventListener('mousedown', () => tocar(nota.freq, nota.name));
  btn.addEventListener('touchstart', (e) => { e.preventDefault(); tocar(nota.freq, nota.name); });
  tecladoEl.appendChild(btn);
});

// (bloque seq-grid antiguo eliminado — ahora usa piano roll)

// ── INIT AUDIO ──
async function initAudio() {
  if (audioCtx) return;
  audioCtx    = new (window.AudioContext || window.webkitAudioContext)();
  masterGain  = audioCtx.createGain();
  masterGain.gain.value = state.volume;
  masterGain.connect(audioCtx.destination);

  // Analyser para osciloscopio
  analyzerNode = audioCtx.createAnalyser();
  analyzerNode.fftSize = 2048;
  masterGain.connect(analyzerNode);
  dataArray = new Uint8Array(analyzerNode.frequencyBinCount);
  freqArray = new Uint8Array(analyzerNode.frequencyBinCount);

  // Crear nodos de efectos
  await crearEfectos();

  log('AUDIO CONTEXT INICIADO', 'log-ok');
  document.getElementById('st-audio').textContent = 'ACTIVO';
  document.getElementById('dot-out-l').setAttribute('fill', '#00ffcc');
  document.getElementById('dot-out-r').setAttribute('fill', '#00ffcc');
  document.getElementById('blk-out').classList.add('active-block');
  drawLoop();
  actualizarMetrosOut();
}

async function crearEfectos() {
  // Reverb (convolver con buffer sintético)
  reverbNode = audioCtx.createConvolver();
  const revLen = audioCtx.sampleRate * 2.5;
  const revBuf = audioCtx.createBuffer(2, revLen, audioCtx.sampleRate);
  for (let c = 0; c < 2; c++) {
    const ch = revBuf.getChannelData(c);
    for (let i = 0; i < revLen; i++) ch[i] = (Math.random() * 2 - 1) * Math.pow(1 - i / revLen, 2.5);
  }
  reverbNode.buffer = revBuf;
  reverbNode.connect(masterGain);

  // Delay
  delayNode = audioCtx.createDelay(1.0);
  delayNode.delayTime.value = 0.3;
  const delFb = audioCtx.createGain();
  delFb.gain.value = 0.4;
  delayNode.connect(delFb);
  delFb.connect(delayNode);
  delayNode.connect(masterGain);

  // Distorsión (waveshaper)
  distortNode = audioCtx.createWaveShaper();
  distortNode.curve = makeDistCurve(300);
  distortNode.oversample = '4x';
  distortNode.connect(masterGain);

  // Flanger (delay muy corto + LFO)
  flangerNode = audioCtx.createDelay(0.02);
  const flangerLFO   = audioCtx.createOscillator();
  const flangerDepth = audioCtx.createGain();
  flangerLFO.frequency.value = 0.5;
  flangerDepth.gain.value = 0.003;
  flangerLFO.connect(flangerDepth);
  flangerDepth.connect(flangerNode.delayTime);
  flangerLFO.start();
  flangerNode.connect(masterGain);

  // Filtros
  lpfNode = audioCtx.createBiquadFilter();
  lpfNode.type = 'lowpass';
  lpfNode.frequency.value = 800;
  lpfNode.connect(masterGain);

  hpfNode = audioCtx.createBiquadFilter();
  hpfNode.type = 'highpass';
  hpfNode.frequency.value = 600;
  hpfNode.connect(masterGain);
}

function makeDistCurve(amount) {
  const n = 256, curve = new Float32Array(n);
  for (let i = 0; i < n; i++) {
    const x = (i * 2) / n - 1;
    curve[i] = ((Math.PI + amount) * x) / (Math.PI + amount * Math.abs(x));
  }
  return curve;
}

// ── TOCAR NOTA ──
function tocar(freq, nombre) {
  if (!audioCtx) { initAudio().then(() => tocar(freq, nombre)); return; }
  if (audioCtx.state === 'suspended') audioCtx.resume();

  const octMult = Math.pow(2, state.octave - 4);
  const f = freq * octMult;

  const osc  = audioCtx.createOscillator();
  const gain = audioCtx.createGain();
  osc.type = state.wave;
  osc.frequency.value = f;

  gain.gain.setValueAtTime(0, audioCtx.currentTime);
  gain.gain.linearRampToValueAtTime(state.volume * 0.8, audioCtx.currentTime + state.attack);
  gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + state.duration);

  osc.connect(gain);

  // Conectar a efectos activos
  const destinos = [masterGain];
  if (state.fx.reverb)  destinos.push(reverbNode);
  if (state.fx.delay)   destinos.push(delayNode);
  if (state.fx.distort) destinos.push(distortNode);
  if (state.fx.flanger) destinos.push(flangerNode);
  if (state.fx.lpf)     destinos.push(lpfNode);
  if (state.fx.hpf)     destinos.push(hpfNode);
  destinos.forEach(d => gain.connect(d));

  osc.start();
  osc.stop(audioCtx.currentTime + state.duration + 0.05);

  // Visual
  pulsarCore(freq);
  flashKey(nombre);
  document.getElementById('st-nota').textContent = nombre || '?';
  document.getElementById('st-freq').textContent = Math.round(f) + ' Hz';
  log(`▶ ${nombre || '?'} | ${Math.round(f)}Hz | ${state.wave.toUpperCase()} | oct${state.octave}`, 'log-hi');
}

function flashKey(nombre) {
  document.querySelectorAll('.key').forEach(k => {
    if (k.dataset.name === nombre) {
      k.classList.add('active');
      setTimeout(() => k.classList.remove('active'), state.duration * 800);
    }
  });
}

function pulsarCore(freq) {
  const colors = {
    low:  '#ff3300',
    mid:  '#00ffcc',
    high: '#cc00ff',
    vhigh:'#ffcc00'
  };
  let color = freq < 200 ? colors.low : freq < 400 ? colors.mid : freq < 600 ? colors.high : colors.vhigh;
  const core = document.getElementById('core');
  core.style.backgroundColor = color;
  core.style.boxShadow = `0 0 60px ${color}, 0 0 100px ${color}`;
  // Pulsar anillos
  document.querySelectorAll('.anillo').forEach((r, i) => {
    setTimeout(() => {
      r.style.borderColor = color.replace(')', `, ${0.4 - i * 0.04})`).replace('rgb', 'rgba');
    }, i * 30);
  });
  setTimeout(() => {
    core.style.backgroundColor = '#fff';
    core.style.boxShadow = '0 0 30px #fff';
    document.querySelectorAll('.anillo').forEach(r => r.style.borderColor = 'rgba(0,255,204,0.08)');
  }, state.duration * 1000 + 100);
}

// ── ACCIONES RÁPIDAS ──
function emitirDisonancia() {
  if (!audioCtx) { initAudio().then(emitirDisonancia); return; }
  const freqs = [315, 317, 313, 320];
  freqs.forEach((f, i) => {
    setTimeout(() => tocar(f, 'DIS'), i * 80);
  });
}

function acordeMayor() {
  const base = 261.63;
  [base, base * 1.25, base * 1.5].forEach((f, i) => {
    setTimeout(() => tocar(f, 'ACM'), i * 20);
  });
}

function acordeMenor() {
  const base = 261.63;
  [base, base * 1.189, base * 1.5].forEach((f, i) => {
    setTimeout(() => tocar(f, 'ACm'), i * 20);
  });
}

function arpegio() {
  const escala = [261.63, 293.66, 329.63, 392.00, 440.00, 523.25];
  escala.forEach((f, i) => {
    setTimeout(() => tocar(f, 'ARP'), i * 120);
  });
}

function barrido() {
  if (!audioCtx) { initAudio().then(barrido); return; }
  if (audioCtx.state === 'suspended') audioCtx.resume();
  const osc  = audioCtx.createOscillator();
  const gain = audioCtx.createGain();
  osc.type = state.wave;
  osc.frequency.setValueAtTime(80, audioCtx.currentTime);
  osc.frequency.exponentialRampToValueAtTime(2000, audioCtx.currentTime + 1.5);
  gain.gain.setValueAtTime(state.volume * 0.6, audioCtx.currentTime);
  gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 1.5);
  osc.connect(gain);
  gain.connect(masterGain);
  osc.start();
  osc.stop(audioCtx.currentTime + 1.6);
  log('〰 BARRIDO FRECUENCIAL 80Hz→2kHz', 'log-warn');
}

// ══════════════════════════════════════════
//  SISTEMA JACK TRRS — ENTRADA / SALIDA
// ══════════════════════════════════════════

let jackState = {
  salidaActiva: true,
  entradaActiva: false,
  thruActivo: false,
  simulActivo: false,
  volOut: 0.7,
  gainIn: 1.0,
  thruVol: 0.5
};

let micStream = null;
let micGainNode = null;
let thruGainNode = null;
let micAnalyzerNode = null;
let meterAnimFrame = null;

// ── TOGGLE SALIDA ──
function toggleSalida() {
  jackState.salidaActiva = !jackState.salidaActiva;
  const btn = document.getElementById('btn-out');
  const blk = document.getElementById('blk-out');
  if (jackState.salidaActiva) {
    if (masterGain) masterGain.gain.value = jackState.volOut;
    btn.textContent = '● ACTIVO';
    btn.classList.remove('off');
    blk.classList.add('active-block');
    document.getElementById('dot-out-l').setAttribute('fill', '#00ffcc');
    document.getElementById('dot-out-r').setAttribute('fill', '#00ffcc');
    log('📤 SALIDA AURICULARES: ON', 'log-ok');
  } else {
    if (masterGain) masterGain.gain.value = 0;
    btn.textContent = '○ SILENCIADO';
    btn.classList.add('off');
    blk.classList.remove('active-block');
    document.getElementById('dot-out-l').setAttribute('fill', '#1a1a1a');
    document.getElementById('dot-out-r').setAttribute('fill', '#1a1a1a');
    log('📤 SALIDA AURICULARES: SILENCIADA', 'log-warn');
  }
}

// ── TOGGLE ENTRADA MIC/JACK ──
async function toggleEntrada() {
  await initAudio();
  if (audioCtx.state === 'suspended') audioCtx.resume();

  if (jackState.entradaActiva) {
    // Desactivar
    if (micStream) { micStream.getTracks().forEach(t => t.stop()); micStream = null; }
    if (micSource) { try { micSource.disconnect(); } catch(e){} micSource = null; }
    jackState.entradaActiva = false;
    document.getElementById('btn-mic').textContent = '○ INACTIVO';
    document.getElementById('btn-mic').classList.add('off');
    document.getElementById('blk-in').classList.remove('active-block');
    document.getElementById('dot-mic').setAttribute('fill', '#1a1a1a');
    document.getElementById('st-mic').textContent = 'OFF';
    document.getElementById('meter-in').style.width = '0%';
    log('📥 ENTRADA JACK: DESCONECTADA', 'log-warn');
  } else {
    // Activar
    try {
      // Preferir dispositivo jack/auricular si está disponible
      const devices = await navigator.mediaDevices.enumerateDevices();
      const audioIn = devices.filter(d => d.kind === 'audioinput');
      // Intentar seleccionar el micro del jack (suele ser el primero no por defecto)
      let deviceId = undefined;
      const jackDev = audioIn.find(d =>
        d.label.toLowerCase().includes('headset') ||
        d.label.toLowerCase().includes('jack') ||
        d.label.toLowerCase().includes('wired') ||
        d.label.toLowerCase().includes('auricular')
      );
      if (jackDev) deviceId = jackDev.deviceId;

      micStream = await navigator.mediaDevices.getUserMedia({
        audio: deviceId
          ? { deviceId: { exact: deviceId }, echoCancellation: false, noiseSuppression: false, autoGainControl: false }
          : { echoCancellation: false, noiseSuppression: false, autoGainControl: false }
      });

      micSource    = audioCtx.createMediaStreamSource(micStream);
      micGainNode  = audioCtx.createGain();
      micGainNode.gain.value = jackState.gainIn;

      // Analyzer exclusivo para la entrada
      micAnalyzerNode = audioCtx.createAnalyser();
      micAnalyzerNode.fftSize = 1024;

      micSource.connect(micGainNode);
      micGainNode.connect(micAnalyzerNode);
      micGainNode.connect(analyzerNode); // visible en osciloscopio

      // Thru: si está activo, conectar también a la salida
      if (jackState.thruActivo && thruGainNode) {
        micGainNode.connect(thruGainNode);
      }

      jackState.entradaActiva = true;
      document.getElementById('btn-mic').textContent = '● ESCUCHANDO';
      document.getElementById('btn-mic').classList.remove('off');
      document.getElementById('blk-in').classList.add('active-block');
      document.getElementById('dot-mic').setAttribute('fill', '#ff3300');
      document.getElementById('st-mic').textContent = jackDev ? 'JACK' : 'MIC';
      log(`📥 ENTRADA JACK ACTIVA${jackDev ? ' — DISPOSITIVO: ' + jackDev.label.substring(0,30) : ' — MIC INTERNO'}`, 'log-ok');
      iniciarMedidorEntrada();
    } catch (err) {
      log('❌ ERROR: PERMISO DE AUDIO DENEGADO — ' + err.message, 'log-err');
    }
  }
}

// ── TOGGLE MONITOR THRU (escucha lo que entra, en tiempo real) ──
async function toggleThru() {
  await initAudio();
  jackState.thruActivo = !jackState.thruActivo;
  const btn = document.getElementById('btn-thru');

  if (jackState.thruActivo) {
    thruGainNode = audioCtx.createGain();
    thruGainNode.gain.value = jackState.thruVol;
    thruGainNode.connect(masterGain);
    if (micGainNode) micGainNode.connect(thruGainNode);
    btn.textContent = '● MONITOR THRU';
    btn.classList.remove('off');
    log('🔁 MONITOR THRU: ON — entrada enrutada a salida', 'log-ok');
  } else {
    if (thruGainNode) { try { thruGainNode.disconnect(); } catch(e){} thruGainNode = null; }
    btn.textContent = '○ MONITOR THRU';
    btn.classList.add('off');
    log('🔁 MONITOR THRU: OFF', 'log-warn');
  }
}

// ── TOGGLE MODO SIMULTÁNEO ──
async function toggleSimultaneo() {
  jackState.simulActivo = !jackState.simulActivo;
  const btn    = document.getElementById('btn-simul');
  const status = document.getElementById('simul-status');

  if (jackState.simulActivo) {
    // Activar salida + entrada juntas
    if (!jackState.salidaActiva) toggleSalida();
    if (!jackState.entradaActiva) await toggleEntrada();
    if (!jackState.thruActivo) await toggleThru();

    btn.textContent = '● SIMULTÁNEO ACTIVO';
    btn.classList.remove('off');
    document.getElementById('blk-simul').classList.add('active-block');
    status.style.color = '#00ffcc';
    status.textContent = '⚡ JACK: EMITIENDO Y ESCUCHANDO — TRRS DUAL MODE';
    log('⚡ MODO SIMULTÁNEO JACK: ACTIVO — TX + RX por TRRS', 'log-hi');
  } else {
    btn.textContent = '○ DESACTIVADO';
    btn.classList.add('off');
    document.getElementById('blk-simul').classList.remove('active-block');
    status.style.color = '#333';
    status.textContent = '— ESPERANDO ACTIVACIÓN —';
    log('⚡ MODO SIMULTÁNEO: OFF', 'log-warn');
  }
}

// ── CONTROLES DE VOLUMEN / GAIN ──
function setVolOut(v) {
  jackState.volOut = v / 100;
  document.getElementById('jack-vol-out-val').textContent = v + '%';
  if (masterGain && jackState.salidaActiva) masterGain.gain.value = jackState.volOut;
}
function setGainIn(v) {
  jackState.gainIn = v / 100;
  document.getElementById('jack-gain-in-val').textContent = v + '%';
  if (micGainNode) micGainNode.gain.value = jackState.gainIn;
}
function setThruVol(v) {
  jackState.thruVol = v / 100;
  document.getElementById('jack-thru-val').textContent = v + '%';
  if (thruGainNode) thruGainNode.gain.value = jackState.thruVol;
}

// ── MEDIDOR VU DE ENTRADA ──
function iniciarMedidorEntrada() {
  if (meterAnimFrame) cancelAnimationFrame(meterAnimFrame);
  const meterIn = document.getElementById('meter-in');
  const buf = new Uint8Array(micAnalyzerNode.frequencyBinCount);
  function tick() {
    if (!jackState.entradaActiva) { meterIn.style.width = '0%'; return; }
    micAnalyzerNode.getByteFrequencyData(buf);
    const avg = buf.reduce((a,b) => a+b, 0) / buf.length;
    const pct = Math.min(100, (avg / 128) * 100);
    meterIn.style.width = pct + '%';
    meterIn.style.background = pct > 80 ? '#ff3300' : pct > 60 ? '#ffcc00' : '#00ffcc';
    meterAnimFrame = requestAnimationFrame(tick);
  }
  tick();
}

// ── MEDIDORES VU DE SALIDA (desde analyzerNode) ──
function actualizarMetrosOut() {
  requestAnimationFrame(actualizarMetrosOut);
  if (!analyzerNode || !jackState.salidaActiva) {
    document.getElementById('meter-out-l').style.width = '0%';
    document.getElementById('meter-out-r').style.width = '0%';
    return;
  }
  const buf = new Uint8Array(analyzerNode.frequencyBinCount);
  analyzerNode.getByteFrequencyData(buf);
  const half = buf.length / 2;
  const avgL = buf.slice(0, half).reduce((a,b)=>a+b,0) / half;
  const avgR = buf.slice(half).reduce((a,b)=>a+b,0) / half;
  document.getElementById('meter-out-l').style.width = Math.min(100,(avgL/128)*120) + '%';
  document.getElementById('meter-out-r').style.width = Math.min(100,(avgR/128)*120) + '%';
}
// Iniciar medidores de salida al cargar
setTimeout(() => { if (analyzerNode) actualizarMetrosOut(); }, 500);

// ── SELECTOR FORMA DE ONDA ──
document.querySelectorAll('.wave-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.wave-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    state.wave = btn.dataset.wave;
    document.getElementById('st-wave').textContent = btn.dataset.wave.toUpperCase();
    log(`ONDA: ${btn.dataset.wave.toUpperCase()}`, 'log-ok');
  });
});

// ── EFECTOS ──
const fxMap = {
  'fx-reverb':  'reverb',
  'fx-delay':   'delay',
  'fx-distort': 'distort',
  'fx-flanger': 'flanger',
  'fx-lpf':     'lpf',
  'fx-hpf':     'hpf',
};
Object.entries(fxMap).forEach(([id, key]) => {
  document.getElementById(id).addEventListener('click', function() {
    if (!audioCtx) { initAudio(); }
    state.fx[key] = !state.fx[key];
    this.classList.toggle('active', state.fx[key]);
    const activos = Object.entries(state.fx).filter(([,v]) => v).map(([k]) => k.toUpperCase()).join('+') || 'NINGUNO';
    document.getElementById('st-fx').textContent = activos;
    log(`FX ${key.toUpperCase()}: ${state.fx[key] ? 'ON' : 'OFF'}`, 'log-warn');
  });
});

// ══════════════════════════════════════════
//  CONTROL DE FRECUENCIA DIRECTA (Hz)
// ══════════════════════════════════════════

let hzBase    = 440;
let hzFine    = 0;
let hzContOsc = null;
let hzContGain= null;

function getHzTotal() { return Math.max(1, hzBase + hzFine); }

function onHzSlider(v) {
  hzBase = parseFloat(v);
  updateHzDisplay();
  if (hzContOsc) hzContOsc.frequency.value = getHzTotal();
}

function onHzFine(v) {
  hzFine = parseFloat(v);
  document.getElementById('hz-fine-val').textContent = (hzFine >= 0 ? '+' : '') + hzFine.toFixed(1) + ' Hz';
  updateHzDisplay();
  if (hzContOsc) hzContOsc.frequency.value = getHzTotal();
}

function resetHzFine() {
  hzFine = 0;
  document.getElementById('slider-hz-fine').value = 0;
  document.getElementById('hz-fine-val').textContent = '±0 Hz';
  if (hzContOsc) hzContOsc.frequency.value = getHzTotal();
}

function setHz(val) {
  hzBase = val;
  document.getElementById('slider-hz').value = val;
  updateHzDisplay();
  if (hzContOsc) hzContOsc.frequency.value = getHzTotal();
  else tocarHz(); // preview rápido
}

function updateHzDisplay() {
  const total = getHzTotal();
  const el = document.getElementById('hz-val-big');
  const unit = document.getElementById('hz-unit');
  const zone = document.getElementById('hz-zone-label');

  if (total >= 1000) {
    el.textContent = (total / 1000).toFixed(total < 10000 ? 2 : 1);
    unit.textContent = 'kHz';
  } else {
    el.textContent = Math.round(total);
    unit.textContent = 'Hz';
  }

  // Zona y color
  if (total < 20) {
    zone.textContent = 'INFRA'; zone.style.color = '#555'; el.style.color = '#555';
  } else if (total < 300) {
    zone.textContent = 'GRAVES'; zone.style.color = '#00ffcc'; el.style.color = '#00ffcc';
  } else if (total < 4000) {
    zone.textContent = 'MEDIOS'; zone.style.color = '#0088ff'; el.style.color = '#0088ff';
  } else if (total < 12000) {
    zone.textContent = 'AGUDOS'; zone.style.color = '#cc00ff'; el.style.color = '#cc00ff';
  } else if (total < 20000) {
    zone.textContent = 'MUY AGUDO'; zone.style.color = '#ffcc00'; el.style.color = '#ffcc00';
  } else {
    zone.textContent = '⚠ ULTRA'; zone.style.color = '#ff3300'; el.style.color = '#ff3300';
  }
}

function tocarHz() {
  if (!audioCtx) { initAudio().then(tocarHz); return; }
  if (audioCtx.state === 'suspended') audioCtx.resume();
  const total = getHzTotal();
  const osc  = audioCtx.createOscillator();
  const gain = audioCtx.createGain();
  osc.type = state.wave;
  osc.frequency.value = total;
  gain.gain.setValueAtTime(state.volume * 0.5, audioCtx.currentTime);
  gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 0.4);
  osc.connect(gain);
  gain.connect(masterGain);
  osc.start();
  osc.stop(audioCtx.currentTime + 0.4);
}

function toggleHzContinuo() {
  if (!audioCtx) { initAudio().then(toggleHzContinuo); return; }
  if (audioCtx.state === 'suspended') audioCtx.resume();
  const btn = document.getElementById('hz-play-btn');

  if (hzContOsc) {
    // Parar
    try { hzContGain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + 0.05);
          hzContOsc.stop(audioCtx.currentTime + 0.06); } catch(e){}
    hzContOsc = null; hzContGain = null;
    btn.textContent = '▶ EMIT';
    btn.classList.remove('active');
    log('■ EMISIÓN Hz CONTINUA PARADA', 'log-warn');
  } else {
    // Emitir continuo
    hzContOsc  = audioCtx.createOscillator();
    hzContGain = audioCtx.createGain();
    hzContOsc.type = state.wave;
    hzContOsc.frequency.value = getHzTotal();
    hzContGain.gain.setValueAtTime(state.volume * 0.5, audioCtx.currentTime);
    hzContOsc.connect(hzContGain);
    hzContGain.connect(masterGain);
    hzContOsc.start();
    btn.textContent = '■ STOP';
    btn.classList.add('active');
    log(`▶ EMISIÓN CONTINUA: ${Math.round(getHzTotal())} Hz`, 'log-hi');
    // Auto-parar cuando la onda cambia para reconectar
    hzContOsc.onended = () => { hzContOsc = null; hzContGain = null; btn.textContent = '▶ EMIT'; btn.classList.remove('active'); };
  }
}

// Actualizar frecuencia continua si cambia la onda
document.querySelectorAll('.wave-btn').forEach(b => {
  b.addEventListener('click', () => {
    if (hzContOsc) hzContOsc.type = b.dataset.wave;
  });
});

// ══════════════════════════════════════════
//  PANEL DE ACORDES
// ══════════════════════════════════════════

const CHORD_ROOTS = ['C','C#','D','D#','E','F','F#','G','G#','A','A#','B'];
const CHORD_ROOT_HZ = [261.63,277.18,293.66,311.13,329.63,349.23,369.99,392.00,415.30,440.00,466.16,493.88];
const CHORD_TYPES = {
  'MAY':    [0,4,7],
  'MEN':    [0,3,7],
  'MAY7':   [0,4,7,11],
  'MEN7':   [0,3,7,10],
  'DOM7':   [0,4,7,10],
  'DIM':    [0,3,6],
  'AUM':    [0,4,8],
  'SUS2':   [0,2,7],
  'SUS4':   [0,5,7],
  'ADD9':   [0,4,7,14],
  '9':      [0,4,7,10,14],
  'MAJ9':   [0,4,7,11,14],
  'MEN9':   [0,3,7,10,14],
  'DIM7':   [0,3,6,9],
  '11':     [0,4,7,10,14,17],
  'POWER':  [0,7],
};

let chordRootIdx = 9;  // LA por defecto
let chordTypeKey = 'MAY';

function buildChordPanel() {
  // Raíces
  const rootsEl = document.getElementById('chord-roots');
  CHORD_ROOTS.forEach((name, i) => {
    const btn = document.createElement('button');
    const isSharpNote = name.includes('#');
    btn.className = 'chord-root-btn' + (isSharpNote ? ' sharp' : '') + (i === chordRootIdx ? ' active' : '');
    btn.textContent = name;
    btn.onclick = () => {
      document.querySelectorAll('.chord-root-btn').forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      chordRootIdx = i;
      updateChordDisplay();
    };
    rootsEl.appendChild(btn);
  });

  // Tipos
  const typesEl = document.getElementById('chord-types');
  Object.keys(CHORD_TYPES).forEach(key => {
    const btn = document.createElement('button');
    btn.className = 'chord-type-btn' + (key === chordTypeKey ? ' active' : '');
    btn.textContent = key;
    btn.onclick = () => {
      document.querySelectorAll('.chord-type-btn').forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      chordTypeKey = key;
      updateChordDisplay();
    };
    typesEl.appendChild(btn);
  });

  updateChordDisplay();
}

function getChordFreqs() {
  const oct     = parseInt(document.getElementById('chord-oct').value);
  const octMult = Math.pow(2, oct - 4);
  const root    = CHORD_ROOT_HZ[chordRootIdx] * octMult;
  return CHORD_TYPES[chordTypeKey].map(semi => root * Math.pow(2, semi / 12));
}

function updateChordDisplay() {
  const freqs = getChordFreqs();
  const names = CHORD_TYPES[chordTypeKey].map(semi => {
    const noteIdx = (chordRootIdx + semi) % 12;
    return CHORD_ROOTS[noteIdx];
  });
  document.getElementById('chord-display').textContent =
    `${CHORD_ROOTS[chordRootIdx]} ${chordTypeKey}  →  ${names.join(' - ')}  [${freqs.map(f=>Math.round(f)+'Hz').join(', ')}]`;
}

function tocarAcorde() {
  if (!audioCtx) { initAudio().then(tocarAcorde); return; }
  if (audioCtx.state === 'suspended') audioCtx.resume();
  const freqs = getChordFreqs();
  freqs.forEach(f => {
    const osc  = audioCtx.createOscillator();
    const gain = audioCtx.createGain();
    osc.type = state.wave;
    osc.frequency.value = f;
    gain.gain.setValueAtTime(0, audioCtx.currentTime);
    gain.gain.linearRampToValueAtTime(state.volume * 0.4, audioCtx.currentTime + state.attack);
    gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + state.duration);
    osc.connect(gain); gain.connect(masterGain);
    osc.start(); osc.stop(audioCtx.currentTime + state.duration + 0.05);
  });
  pulsarCore(CHORD_ROOT_HZ[chordRootIdx]);
  log(`🎸 ACORDE: ${CHORD_ROOTS[chordRootIdx]} ${chordTypeKey}`, 'log-hi');
}

function tocarAcordeArpegio() {
  if (!audioCtx) { initAudio().then(tocarAcordeArpegio); return; }
  const freqs = getChordFreqs();
  freqs.forEach((f, i) => setTimeout(() => tocar(f, CHORD_ROOTS[(chordRootIdx + CHORD_TYPES[chordTypeKey][i]) % 12]), i * 130));
}

function tocarAcordeInversion() {
  if (!audioCtx) { initAudio().then(tocarAcordeInversion); return; }
  // Primera inversión: primera nota sube una octava
  const freqs = getChordFreqs();
  freqs[0] *= 2;
  freqs.forEach(f => {
    const osc  = audioCtx.createOscillator();
    const gain = audioCtx.createGain();
    osc.type = state.wave;
    osc.frequency.value = f;
    gain.gain.setValueAtTime(0, audioCtx.currentTime);
    gain.gain.linearRampToValueAtTime(state.volume * 0.4, audioCtx.currentTime + state.attack);
    gain.gain.exponentialRampToValueAtTime(0.001, audioCtx.currentTime + state.duration);
    osc.connect(gain); gain.connect(masterGain);
    osc.start(); osc.stop(audioCtx.currentTime + state.duration + 0.05);
  });
  log(`🎸 INVERSIÓN: ${CHORD_ROOTS[chordRootIdx]} ${chordTypeKey} (1ª inv)`, 'log-hi');
}

// Inicializar panel de acordes
buildChordPanel();

// ── SLIDERS ──
document.getElementById('slider-vol').addEventListener('input', function() {
  state.volume = this.value / 100;
  document.getElementById('vol-val').textContent = this.value;
  if (masterGain) masterGain.gain.value = state.volume;
});
document.getElementById('slider-dur').addEventListener('input', function() {
  state.duration = this.value / 10;
  document.getElementById('dur-val').textContent = state.duration.toFixed(1);
});
document.getElementById('slider-atk').addEventListener('input', function() {
  state.attack = this.value / 1000;
  document.getElementById('atk-val').textContent = state.attack.toFixed(3);
});
document.getElementById('slider-oct').addEventListener('input', function() {
  state.octave = parseInt(this.value);
  document.getElementById('oct-val').textContent = this.value;
  log(`OCTAVA: ${this.value}`, 'log-ok');
});

// ══════════════════════════════════════════
//  SECUENCIADOR MELÓDICO
// ══════════════════════════════════════════

// Escalas: intervalos en semitonos desde la raíz
const ESCALAS = {
  'cromática':   [0,1,2,3,4,5,6,7,8,9,10,11],
  'mayor':       [0,2,4,5,7,9,11],
  'menor':       [0,2,3,5,7,8,10],
  'pentatonica': [0,2,4,7,9],
  'blues':       [0,3,5,6,7,10],
  'dórica':      [0,2,3,5,7,9,10],
  'frigia':      [0,1,3,5,7,8,10],
};

// Notas cromáticas base (Hz) desde C0
const BASE_C0 = 16.3516;
const SHARP_IDX = [1,3,6,8,10]; // C#,D#,F#,G#,A#
const NOTE_NAMES_ALL = ['C','C#','D','D#','E','F','F#','G','G#','A','A#','B'];

// Estado del secuenciador melódico
// seqData[paso] = { active: bool, semitone: int (índice absoluto desde C0) }
const SEQ_STEPS = 16;
let seqData = Array.from({length: SEQ_STEPS}, () => ({ active: false, semitone: 48 })); // 48 = C4
let seqScaleNotes = []; // notas disponibles según escala seleccionada
const PIANO_ROWS = 14; // filas visibles en el piano roll (notas en el rango)

function semitonToHz(semitone) {
  return BASE_C0 * Math.pow(2, semitone / 12);
}
function semitoneName(semitone) {
  const oct  = Math.floor(semitone / 12);
  const note = semitone % 12;
  return NOTE_NAMES_ALL[note] + oct;
}
function isSharp(semitone) {
  return SHARP_IDX.includes(semitone % 12);
}

// ── Calcular notas de la escala seleccionada ──
function calcularEscala() {
  const escala   = document.getElementById('seq-scale').value;
  const root     = parseInt(document.getElementById('seq-root').value);
  const octBase  = parseInt(document.getElementById('seq-oct-base').value);
  const intervalos = ESCALAS[escala];
  const baseSemi = octBase * 12 + root; // C=0,C#=1,...
  // 2 octavas de la escala
  seqScaleNotes = [];
  for (let oct = 0; oct <= 2; oct++) {
    intervalos.forEach(iv => {
      seqScaleNotes.push(baseSemi + oct * 12 + iv);
    });
  }
  seqScaleNotes = [...new Set(seqScaleNotes)].sort((a,b)=>b-a); // orden descendente (arriba = agudo)
  return seqScaleNotes;
}

// ── Construir el piano roll ──
function buildPianoRoll() {
  calcularEscala();

  const noteRow   = document.getElementById('seq-note-row');
  const rollEl    = document.getElementById('seq-piano-roll');
  const activeRow = document.getElementById('seq-active-row');

  noteRow.innerHTML   = '';
  rollEl.innerHTML    = '';
  activeRow.innerHTML = '';

  // Crear columnas (una por paso)
  for (let step = 0; step < SEQ_STEPS; step++) {
    // ── Label superior (nota asignada) ──
    const label = document.createElement('div');
    label.className = 'seq-note-label';
    label.id = `seq-label-${step}`;
    label.textContent = seqData[step].active ? semitoneName(seqData[step].semitone) : '—';
    if (seqData[step].active) label.classList.add('has-note');
    noteRow.appendChild(label);

    // ── Columna del piano roll ──
    const col = document.createElement('div');
    col.className = 'seq-pitch-col';

    seqScaleNotes.forEach((semi, row) => {
      const cell = document.createElement('div');
      cell.className = 'seq-pitch-cell' + (isSharp(semi) ? ' is-sharp' : '');
      cell.dataset.step = step;
      cell.dataset.semi = semi;
      // Marcar si este paso tiene esta nota seleccionada
      if (seqData[step].active && seqData[step].semitone === semi) {
        cell.classList.add('selected');
      }
      cell.addEventListener('click', () => seleccionarNota(step, semi, cell));
      col.appendChild(cell);
    });

    rollEl.appendChild(col);

    // ── Botón activo/inactivo (fila inferior) ──
    const ab = document.createElement('div');
    ab.className = 'seq-active-btn' + (seqData[step].active ? ' on' : '');
    ab.id = `seq-active-${step}`;
    ab.dataset.step = step;
    ab.innerHTML = `<span class="step-num">${step + 1}</span>`;
    ab.addEventListener('click', () => toggleStepActive(step));
    activeRow.appendChild(ab);
  }
}

// ── Seleccionar nota para un paso ──
function seleccionarNota(step, semi, cell) {
  // Desmarcar celda anterior en esta columna
  document.querySelectorAll(`[data-step="${step}"].seq-pitch-cell`).forEach(c => {
    c.classList.remove('selected', 'playing-cell');
  });
  seqData[step].semitone = semi;
  seqData[step].active   = true;
  cell.classList.add('selected');
  // Actualizar label
  const label = document.getElementById(`seq-label-${step}`);
  label.textContent = semitoneName(semi);
  label.classList.add('has-note');
  // Activar el paso
  const ab = document.getElementById(`seq-active-${step}`);
  ab.classList.add('on');
  // Preview sonido
  tocar(semitonToHz(semi), semitoneName(semi));
}

// ── Activar/desactivar paso ──
function toggleStepActive(step) {
  seqData[step].active = !seqData[step].active;
  const ab    = document.getElementById(`seq-active-${step}`);
  const label = document.getElementById(`seq-label-${step}`);
  if (seqData[step].active) {
    ab.classList.add('on');
    label.textContent = semitoneName(seqData[step].semitone);
    label.classList.add('has-note');
  } else {
    ab.classList.remove('on');
    label.textContent = '—';
    label.classList.remove('has-note');
  }
}

// ── Aplicar escala nueva (reconstruir roll) ──
function aplicarEscala() {
  buildPianoRoll();
  log(`ESCALA: ${document.getElementById('seq-scale').value.toUpperCase()} — RAÍZ: ${NOTE_NAMES_ALL[parseInt(document.getElementById('seq-root').value)]}`, 'log-ok');
}

// ── Melodía aleatoria ──
function randomizeMelody() {
  calcularEscala();
  const steps = parseInt(document.getElementById('seq-steps').value);
  for (let s = 0; s < SEQ_STEPS; s++) {
    if (s < steps) {
      seqData[s].active   = Math.random() > 0.3;
      seqData[s].semitone = seqScaleNotes[Math.floor(Math.random() * seqScaleNotes.length)];
    } else {
      seqData[s].active = false;
    }
  }
  buildPianoRoll();
  log('🎲 MELODÍA ALEATORIA GENERADA', 'log-ok');
}

// ── BPM y pasos ──
document.getElementById('seq-bpm').addEventListener('input', function() {
  document.getElementById('seq-bpm-val').textContent = this.value + ' BPM';
  if (seqRunning) { clearInterval(seqInterval); startSeq(); }
});
document.getElementById('seq-steps').addEventListener('input', function() {
  document.getElementById('seq-steps-val').textContent = this.value;
});

// ── Play/Stop ──
function toggleSequencer() {
  if (!audioCtx) { initAudio().then(toggleSequencer); return; }
  if (seqRunning) {
    clearInterval(seqInterval);
    seqRunning = false;
    document.getElementById('seq-play-btn').textContent = '▶ PLAY';
    document.getElementById('st-seq').textContent = 'PARADO';
    // Limpiar highlights
    document.querySelectorAll('.seq-pitch-cell').forEach(c => c.classList.remove('playing-cell'));
    document.querySelectorAll('.seq-active-btn').forEach(c => c.classList.remove('playing'));
    log('■ SECUENCIADOR PARADO', 'log-warn');
  } else {
    startSeq();
    document.getElementById('seq-play-btn').textContent = '■ STOP';
    document.getElementById('st-seq').textContent = 'RUNNING';
    log('▶ SECUENCIADOR MELÓDICO INICIADO', 'log-ok');
  }
}

function startSeq() {
  seqRunning = true;
  const bpm   = parseInt(document.getElementById('seq-bpm').value);
  const steps = parseInt(document.getElementById('seq-steps').value);
  const ms    = (60000 / bpm) / 4;
  seqStep = 0;

  seqInterval = setInterval(() => {
    // Limpiar visual paso anterior
    document.querySelectorAll('.seq-pitch-cell').forEach(c => c.classList.remove('playing-cell'));
    document.querySelectorAll('.seq-active-btn').forEach(c => c.classList.remove('playing'));

    const currentStep = seqStep % steps;
    const data = seqData[currentStep];

    // Marcar paso actual
    document.getElementById(`seq-active-${currentStep}`)?.classList.add('playing');

    if (data.active) {
      const freq = semitonToHz(data.semitone);
      tocar(freq, semitoneName(data.semitone));
      // Marcar celda activa en el roll
      document.querySelectorAll(`[data-step="${currentStep}"][data-semi="${data.semitone}"]`)
        .forEach(c => c.classList.add('playing-cell'));
    }

    seqStep = (seqStep + 1) % steps;
  }, ms);
}

function clearSeq() {
  seqData = Array.from({length: SEQ_STEPS}, () => ({ active: false, semitone: 48 }));
  buildPianoRoll();
  log('SECUENCIADOR LIMPIADO', 'log-warn');
}

// ── INIT del piano roll al cargar ──
buildPianoRoll();

// ── DRAW LOOP ──
const oscCanvas  = document.getElementById('osciloscopio');
const specCanvas = document.getElementById('spectrum');
const octx = oscCanvas.getContext('2d');
const sctx = specCanvas.getContext('2d');

function drawLoop() {
  requestAnimationFrame(drawLoop);
  if (!analyzerNode) return;

  // Osciloscopio
  analyzerNode.getByteTimeDomainData(dataArray);
  octx.fillStyle = '#000';
  octx.fillRect(0, 0, oscCanvas.width, oscCanvas.height);
  octx.lineWidth = 1.5;
  octx.strokeStyle = '#00ffcc';
  octx.beginPath();
  const sw = oscCanvas.width / analyzerNode.frequencyBinCount;
  let x = 0;
  for (let i = 0; i < analyzerNode.frequencyBinCount; i++) {
    const v = dataArray[i] / 128.0;
    const y = v * oscCanvas.height / 2;
    i === 0 ? octx.moveTo(x, y) : octx.lineTo(x, y);
    x += sw;
  }
  octx.lineTo(oscCanvas.width, oscCanvas.height / 2);
  octx.stroke();

  // Espectro
  analyzerNode.getByteFrequencyData(freqArray);
  sctx.fillStyle = '#000';
  sctx.fillRect(0, 0, specCanvas.width, specCanvas.height);
  const bw = specCanvas.width / freqArray.length;
  for (let i = 0; i < freqArray.length; i++) {
    const h = (freqArray[i] / 255) * specCanvas.height;
    const hue = (i / freqArray.length) * 180;
    sctx.fillStyle = `hsl(${180 - hue}, 100%, 50%)`;
    sctx.fillRect(i * bw, specCanvas.height - h, bw, h);
  }
}

// ── CREAR ANILLOS ──
const cont = document.getElementById('agarius-container');
for (let i = 1; i <= 9; i++) {
  const r = document.createElement('div');
  r.className = 'anillo';
  const s = 50 + i * 40;
  r.style.width  = s + 'px';
  r.style.height = s + 'px';
  cont.appendChild(r);
}

// ── LOG ──
const monitorEl = document.getElementById('monitor-raid');
function log(msg, clase = 'log-ok') {
  const d = document.createElement('div');
  d.className = clase;
  const ts = new Date().toLocaleTimeString('es', { hour12: false });
  d.textContent = `[${ts}] > ${msg}`;
  monitorEl.prepend(d);
  if (monitorEl.childNodes.length > 30) monitorEl.lastChild.remove();
}

// ── TECLADO FÍSICO ──
const keyMap = {
  'a':'C','w':'C#','s':'D','e':'D#','d':'E','f':'F',
  't':'F#','g':'G','y':'G#','h':'A','u':'A#','j':'B',
  'k':'C2','l':'D2'
};
document.addEventListener('keydown', (ev) => {
  if (ev.repeat) return;
  const nota = keyMap[ev.key.toLowerCase()];
  if (nota) {
    const found = NOTAS.find(n => n.name === nota);
    if (found) tocar(found.freq, found.name);
  }
});

// ── INIT AL CLICK ──
document.body.addEventListener('click', () => { if (!audioCtx) initAudio(); }, { once: true });

// ── TECLADO HINT ──
log('TECLADO: A=C  W=C#  S=D  E=D#  D=E  F=FA  T=F#  G=SOL  Y=G#  H=LA  J=SI', 'log-warn');
</script>
</body>
</html>
