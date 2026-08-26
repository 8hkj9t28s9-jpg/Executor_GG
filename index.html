<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover" />
  <title>JS Mobile Game & App Studio</title>
  
  <!-- CodeMirror 5 Syntax Highlighting -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/codemirror.min.css" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/theme/material-darker.min.css" />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/codemirror.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.65.16/mode/javascript/javascript.min.js"></script>

  <style>
    :root {
      --bg-main: #07090e;
      --bg-panel: #11141c;
      --accent: #38bdf8;
      --accent-green: #10b981;
      --accent-red: #ef4444;
      --accent-purple: #a855f7;
      --accent-orange: #f97316;
      --border: #1e2433;
      --text: #e2e8f0;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      -webkit-tap-highlight-color: transparent;
      user-select: none;
    }

    body {
      background: var(--bg-main);
      color: var(--text);
      display: flex;
      flex-direction: column;
      height: 100dvh;
      overflow: hidden;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    }

    /* Top Navigation */
    header {
      background: var(--bg-panel);
      padding: 6px 10px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid var(--border);
      z-index: 10;
    }

    .brand-wrap {
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .brand {
      font-weight: 900;
      font-size: 0.95rem;
      letter-spacing: 0.5px;
      color: var(--accent);
    }

    .header-actions {
      display: flex;
      gap: 4px;
      align-items: center;
    }

    select, button {
      outline: none;
      border: 1px solid transparent;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.75rem;
      padding: 6px 8px;
      cursor: pointer;
    }

    select {
      background: #181d28;
      color: var(--text);
      border-color: var(--border);
      max-width: 100px;
    }

    .btn-run { background: var(--accent-green); color: #fff; }
    .btn-stop { background: var(--accent-red); color: #fff; }
    .btn-pad { background: #1e293b; color: #94a3b8; }
    .btn-pad.active { background: var(--accent-purple); color: #fff; }
    .btn-export { background: var(--accent-orange); color: #fff; }

    /* Tab Controls */
    .tabs {
      display: flex;
      background: var(--bg-panel);
      border-bottom: 1px solid var(--border);
    }

    .tab {
      flex: 1;
      text-align: center;
      padding: 8px 0;
      font-size: 0.78rem;
      font-weight: 700;
      color: #64748b;
      cursor: pointer;
      border-bottom: 2px solid transparent;
      transition: all 0.2s;
    }

    .tab.active {
      color: var(--accent);
      border-bottom-color: var(--accent);
      background: rgba(56, 189, 248, 0.05);
    }

    /* Views */
    .viewport {
      flex: 1;
      position: relative;
      overflow: hidden;
    }

    .view {
      position: absolute;
      inset: 0;
      display: none;
      flex-direction: column;
    }

    .view.active {
      display: flex;
    }

    /* Code Editor */
    .CodeMirror {
      height: 100% !important;
      font-family: "Fira Code", monospace;
      font-size: 0.85rem;
      line-height: 1.45;
      background: #05070a !important;
      user-select: auto;
    }

    .CodeMirror-gutters {
      background: #0a0e17 !important;
      border-right: 1px solid var(--border) !important;
    }

    /* Sandbox Container */
    iframe {
      width: 100%;
      height: 100%;
      border: none;
      background: #000;
    }

    /* Console View */
    #consoleLog {
      flex: 1;
      background: #05070a;
      padding: 8px;
      overflow-y: auto;
      font-family: monospace;
      font-size: 0.78rem;
      user-select: text;
    }

    .log-item {
      padding: 3px 6px;
      border-bottom: 1px solid #121824;
      display: flex;
      gap: 6px;
      word-break: break-all;
    }

    .log-time { color: #475569; }
    .log-info { color: var(--accent); }
    .log-warn { color: #fbbf24; background: rgba(251, 191, 36, 0.05); }
    .log-error { color: var(--accent-red); background: rgba(239, 68, 68, 0.05); }

    /* On-Screen D-Pad & Controller Overlay */
    #gamepadOverlay {
      position: absolute;
      inset: 0;
      pointer-events: none;
      display: none;
      z-index: 50;
    }

    .dpad-container {
      position: absolute;
      bottom: 24px;
      left: 20px;
      width: 120px;
      height: 120px;
      pointer-events: auto;
    }

    .dpad-btn {
      position: absolute;
      background: rgba(255, 255, 255, 0.12);
      border: 1px solid rgba(255, 255, 255, 0.25);
      border-radius: 8px;
      color: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 1.1rem;
      backdrop-filter: blur(4px);
    }

    .dpad-btn:active, .dpad-btn.pressed {
      background: rgba(56, 189, 248, 0.5);
    }

    .dpad-up { top: 0; left: 40px; width: 40px; height: 40px; }
    .dpad-down { bottom: 0; left: 40px; width: 40px; height: 40px; }
    .dpad-left { top: 40px; left: 0; width: 40px; height: 40px; }
    .dpad-right { top: 40px; right: 0; width: 40px; height: 40px; }

    .action-container {
      position: absolute;
      bottom: 30px;
      right: 20px;
      display: flex;
      gap: 15px;
      pointer-events: auto;
    }

    .action-btn {
      width: 52px;
      height: 52px;
      border-radius: 50%;
      background: rgba(239, 68, 68, 0.25);
      border: 1px solid rgba(239, 68, 68, 0.6);
      color: #fff;
      font-weight: 800;
      font-size: 1.1rem;
      display: flex;
      align-items: center;
      justify-content: center;
      backdrop-filter: blur(4px);
    }

    .action-btn.btn-b {
      background: rgba(56, 189, 248, 0.25);
      border-color: rgba(56, 189, 248, 0.6);
      transform: translateY(-12px);
    }

    .action-btn:active, .action-btn.pressed {
      background: rgba(255, 255, 255, 0.6);
      color: #000;
    }

    /* Floating Exit/Editor Switch Button */
    #floatingBtn {
      position: fixed;
      top: 12px;
      right: 12px;
      width: 36px;
      height: 36px;
      border-radius: 50%;
      background: rgba(0, 0, 0, 0.65);
      border: 1px solid rgba(255, 255, 255, 0.3);
      color: #fff;
      display: none;
      align-items: center;
      justify-content: center;
      font-size: 1.1rem;
      font-weight: bold;
      z-index: 100;
      cursor: pointer;
    }

    /* Project Manager Modal */
    #projectModal {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.85);
      display: none;
      flex-direction: column;
      padding: 20px;
      z-index: 200;
    }

    .modal-content {
      background: var(--bg-panel);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 16px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      max-height: 80vh;
      overflow-y: auto;
    }

    .project-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #181d28;
      padding: 10px;
      border-radius: 6px;
    }
  </style>
</head>
<body>

  <header>
    <div class="brand-wrap">
      <div class="brand">STUDIO</div>
      <button onclick="openProjects()" style="background:#1e293b; color:#38bdf8;">📁 Files</button>
    </div>
    <div class="header-actions">
      <button id="padToggleBtn" class="btn-pad active" onclick="toggleGamepad()">🎮 Pad</button>
      <select id="scriptPresets" onchange="loadPreset(this.value)">
        <option value="" disabled selected>Presets...</option>
        <option value="raycaster">3D Raycaster</option>
        <option value="shooter">Space Shooter</option>
        <option value="platformer">Platformer</option>
        <option value="snake">2D Snake</option>
        <option value="particles">Particles</option>
      </select>
      <button class="btn-export" onclick="exportToHTML()">Export</button>
      <button class="btn-stop" onclick="stopExecution()">Stop</button>
      <button class="btn-run" onclick="executeCode()">▶ Run</button>
    </div>
  </header>

  <div class="tabs">
    <div class="tab active" onclick="switchTab('editor')">Code</div>
    <div class="tab" onclick="switchTab('preview')">Preview</div>
    <div class="tab" onclick="switchTab('console')">Console (<span id="logCount">0</span>)</div>
  </div>

  <div class="viewport">
    <div id="editorView" class="view active">
      <textarea id="codeEditor"></textarea>
    </div>

    <div id="previewView" class="view">
      <iframe id="sandboxFrame" sandbox="allow-scripts allow-modals"></iframe>
      
      <!-- Virtual Gamepad Overlay -->
      <div id="gamepadOverlay">
        <div class="dpad-container">
          <div class="dpad-btn dpad-up" data-key="up">▲</div>
          <div class="dpad-btn dpad-left" data-key="left">◀</div>
          <div class="dpad-btn dpad-right" data-key="right">▶</div>
          <div class="dpad-btn dpad-down" data-key="down">▼</div>
        </div>
        <div class="action-container">
          <div class="action-btn btn-b" data-key="b">B</div>
          <div class="action-btn btn-a" data-key="a">A</div>
        </div>
      </div>
    </div>

    <div id="consoleView" class="view">
      <div id="consoleLog"></div>
    </div>
  </div>

  <div id="floatingBtn" onclick="switchTab('editor')">✕</div>

  <!-- Project Manager Modal -->
  <div id="projectModal">
    <div class="modal-content">
      <div style="display:flex; justify-content:space-between; align-items:center;">
        <h3 style="color:#38bdf8;">Saved Projects</h3>
        <button onclick="closeProjects()" style="background:#ef4444; color:#fff;">Close</button>
      </div>
      <div style="display:flex; gap:8px;">
        <input type="text" id="newProjectName" placeholder="New project name..." style="flex:1; padding:8px; background:#07090e; color:#fff; border:1px solid #1e2433; border-radius:4px;" />
        <button onclick="saveNewProject()" style="background:#10b981; color:#fff;">Save Current</button>
      </div>
      <div id="projectList" style="display:flex; flex-direction:column; gap:8px;"></div>
    </div>
  </div>

  <script>
    let gamepadEnabled = true;
    const inputState = { up: false, down: false, left: false, right: false, a: false, b: false };

    // --- PRESETS ---
    const PRESETS = {
      raycaster: `// Pseudo-3D Raycaster Engine (Wolfenstein 3D Style)
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
document.body.appendChild(canvas);

function resize() {
  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;
}
window.addEventListener('resize', resize);
resize();

const MAP = [
  [1,1,1,1,1,1,1,1],
  [1,0,0,0,0,0,0,1],
  [1,0,1,0,1,1,0,1],
  [1,0,1,0,0,1,0,1],
  [1,0,0,0,0,0,0,1],
  [1,0,1,1,0,1,0,1],
  [1,0,0,0,0,0,0,1],
  [1,1,1,1,1,1,1,1]
];
const MAP_SIZE = 8, TILE_SIZE = 64;

let player = { x: 96, y: 96, angle: 0, fov: Math.PI / 3 };

console.log("3D Raycaster Loaded. Use D-Pad Left/Right to turn, Up/Down to move, [A] to buzz.");

function castRays() {
  const numRays = Math.floor(canvas.width / 4);
  const halfFov = player.fov / 2;

  ctx.fillStyle = '#1e293b';
  ctx.fillRect(0, 0, canvas.width, canvas.height / 2); // Ceiling
  ctx.fillStyle = '#0f172a';
  ctx.fillRect(0, canvas.height / 2, canvas.width, canvas.height / 2); // Floor

  for (let i = 0; i < numRays; i++) {
    const rayAngle = player.angle - halfFov + (i / numRays) * player.fov;
    let dist = 0, hit = false;
    const sin = Math.sin(rayAngle), cos = Math.cos(rayAngle);

    while (!hit && dist < 500) {
      dist += 2;
      let checkX = Math.floor((player.x + cos * dist) / TILE_SIZE);
      let checkY = Math.floor((player.y + sin * dist) / TILE_SIZE);

      if (checkX >= 0 && checkX < MAP_SIZE && checkY >= 0 && checkY < MAP_SIZE) {
        if (MAP[checkY][checkX] > 0) hit = true;
      }
    }

    // Fix fisheye distortion
    const correctedDist = dist * Math.cos(rayAngle - player.angle);
    const wallHeight = (TILE_SIZE * 350) / (correctedDist || 1);

    const shade = Math.max(20, Math.min(255, 255 - dist * 0.5));
    ctx.fillStyle = 'rgb(0, ' + Math.floor(shade * 0.7) + ', ' + shade + ')';
    ctx.fillRect(i * 4, (canvas.height - wallHeight) / 2, 4, wallHeight);
  }
}

function loop() {
  if (window.Input) {
    if (window.Input.left) player.angle -= 0.04;
    if (window.Input.right) player.angle += 0.04;
    
    let moveStep = 0;
    if (window.Input.up) moveStep = 3;
    if (window.Input.down) moveStep = -3;

    if (moveStep !== 0) {
      let newX = player.x + Math.cos(player.angle) * moveStep;
      let newY = player.y + Math.sin(player.angle) * moveStep;
      if (MAP[Math.floor(newY / TILE_SIZE)][Math.floor(newX / TILE_SIZE)] === 0) {
        player.x = newX;
        player.y = newY;
      }
    }

    if (window.Input.a) {
      window.Sound.play('laser');
      window.Haptics.buzz(30);
    }
  }

  castRays();
  requestAnimationFrame(loop);
}
loop();`,

      shooter: `// Retro Space Bullet Hell
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
document.body.appendChild(canvas);
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let player = { x: canvas.width / 2, y: canvas.height - 80, r: 16, speed: 5 };
let bullets = [], enemies = [], score = 0;

function spawnEnemy() {
  if (Math.random() < 0.04) {
    enemies.push({ x: Math.random() * (canvas.width - 30) + 15, y: -20, r: 14, dy: 2 + Math.random() * 2 });
  }
}

function loop() {
  ctx.fillStyle = '#05070a';
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  if (window.Input) {
    if (window.Input.left && player.x > player.r) player.x -= player.speed;
    if (window.Input.right && player.x < canvas.width - player.r) player.x += player.speed;
    if (window.Input.up && player.y > player.r) player.y -= player.speed;
    if (window.Input.down && player.y < canvas.height - player.r) player.y += player.speed;

    if (window.Input.a && Math.random() < 0.25) {
      bullets.push({ x: player.x, y: player.y - 10, dy: -9 });
      window.Sound.play('laser');
    }
  }

  spawnEnemy();

  // Bullets
  ctx.fillStyle = '#38bdf8';
  bullets.forEach((b, bi) => {
    b.y += b.dy;
    ctx.fillRect(b.x - 2, b.y - 6, 4, 12);
    if (b.y < 0) bullets.splice(bi, 1);
  });

  // Enemies
  enemies.forEach((e, ei) => {
    e.y += e.dy;
    ctx.fillStyle = '#ef4444';
    ctx.beginPath();
    ctx.arc(e.x, e.y, e.r, 0, Math.PI * 2);
    ctx.fill();

    // Bullet-Enemy Collisions
    bullets.forEach((b, bi) => {
      if (Math.hypot(b.x - e.x, b.y - e.y) < e.r) {
        enemies.splice(ei, 1);
        bullets.splice(bi, 1);
        score += 100;
        window.Sound.play('explosion');
        window.Haptics.buzz(40);
      }
    });

    if (e.y > canvas.height + 20) enemies.splice(ei, 1);
  });

  // Draw Player
  ctx.fillStyle = '#10b981';
  ctx.beginPath();
  ctx.arc(player.x, player.y, player.r, 0, Math.PI * 2);
  ctx.fill();

  ctx.fillStyle = '#fff';
  ctx.font = '16px monospace';
  ctx.fillText('Score: ' + score, 20, 30);

  requestAnimationFrame(loop);
}
loop();`,

      platformer: `// 2D Platformer Jumper
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
document.body.appendChild(canvas);
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let p = { x: 50, y: 100, vx: 0, vy: 0, size: 24, grounded: false };
const gravity = 0.5;

function loop() {
  ctx.fillStyle = '#0f172a';
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  if (window.Input) {
    if (window.Input.left) p.vx = -4;
    else if (window.Input.right) p.vx = 4;
    else p.vx = 0;

    if (window.Input.a && p.grounded) {
      p.vy = -12;
      p.grounded = false;
      window.Sound.play('jump');
      window.Haptics.buzz(20);
    }
  }

  p.vy += gravity;
  p.x += p.vx;
  p.y += p.vy;

  // Floor collision
  if (p.y + p.size >= canvas.height - 40) {
    p.y = canvas.height - 40 - p.size;
    p.vy = 0;
    p.grounded = true;
  }

  // Draw Floor
  ctx.fillStyle = '#334155';
  ctx.fillRect(0, canvas.height - 40, canvas.width, 40);

  // Draw Player
  ctx.fillStyle = '#38bdf8';
  ctx.fillRect(p.x, p.y, p.size, p.size);

  requestAnimationFrame(loop);
}
loop();`,

      snake: `// 2D D-Pad Snake
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
document.body.appendChild(canvas);
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const grid = 20;
let snake = [{x: 160, y: 160}];
let dx = grid, dy = 0, food = {x: 80, y: 80}, count = 0;

function loop() {
  requestAnimationFrame(loop);
  if (++count < 6) return;
  count = 0;

  if (window.Input) {
    if (window.Input.left && dx === 0) { dx = -grid; dy = 0; }
    if (window.Input.right && dx === 0) { dx = grid; dy = 0; }
    if (window.Input.up && dy === 0) { dy = -grid; dx = 0; }
    if (window.Input.down && dy === 0) { dy = grid; dx = 0; }
  }

  ctx.fillStyle = '#05070a';
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  let head = {x: snake[0].x + dx, y: snake[0].y + dy};
  snake.unshift(head);

  if (Math.abs(head.x - food.x) < grid && Math.abs(head.y - food.y) < grid) {
    food.x = Math.floor(Math.random() * (canvas.width / grid)) * grid;
    food.y = Math.floor(Math.random() * (canvas.height / grid)) * grid;
    window.Sound.play('coin');
    window.Haptics.buzz(25);
  } else {
    snake.pop();
  }

  ctx.fillStyle = '#ef4444';
  ctx.fillRect(food.x, food.y, grid - 2, grid - 2);

  ctx.fillStyle = '#38bdf8';
  snake.forEach(cell => ctx.fillRect(cell.x, cell.y, grid - 2, grid - 2));
}
loop();`,

      particles: `// Multi-touch Particle FX
const canvas = document.createElement('canvas');
const ctx = canvas.getContext('2d');
document.body.appendChild(canvas);
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let particles = [];
window.addEventListener('pointermove', e => {
  for(let i = 0; i < 4; i++) {
    particles.push({
      x: e.clientX, y: e.clientY,
      dx: (Math.random() - 0.5) * 6,
      dy: (Math.random() - 0.5) * 6,
      size: Math.random() * 8 + 2,
      color: 'hsl(' + (Date.now() / 10 % 360) + ', 100%, 60%)'
    });
  }
});

function animate() {
  ctx.fillStyle = 'rgba(0, 0, 0, 0.15)';
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  particles.forEach((p, idx) => {
    p.x += p.dx;
    p.y += p.dy;
    p.size *= 0.95;
    ctx.fillStyle = p.color;
    ctx.beginPath();
    ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
    ctx.fill();
    if (p.size < 0.5) particles.splice(idx, 1);
  });
  requestAnimationFrame(animate);
}
animate();`
    };

    // Initialize CodeMirror Editor
    const editor = CodeMirror.fromTextArea(document.getElementById('codeEditor'), {
      mode: 'javascript',
      theme: 'material-darker',
      lineNumbers: true,
      lineWrapping: true,
      indentUnit: 2,
      tabSize: 2
    });

    editor.setValue(localStorage.getItem('exec_studio_code') || PRESETS.raycaster);
    editor.on('change', () => {
      localStorage.setItem('exec_studio_code', editor.getValue());
    });

    let logCounter = 0;

    function switchTab(name) {
      document.querySelectorAll('.tab').forEach((t, i) => {
        t.classList.toggle('active', 
          (name === 'editor' && i === 0) || 
          (name === 'preview' && i === 1) || 
          (name === 'console' && i === 2)
        );
      });

      document.getElementById('editorView').classList.toggle('active', name === 'editor');
      document.getElementById('previewView').classList.toggle('active', name === 'preview');
      document.getElementById('consoleView').classList.toggle('active', name === 'console');

      const floatingBtn = document.getElementById('floatingBtn');
      const padOverlay = document.getElementById('gamepadOverlay');

      floatingBtn.style.display = (name === 'preview') ? 'flex' : 'none';
      padOverlay.style.display = (name === 'preview' && gamepadEnabled) ? 'block' : 'none';

      if (name === 'editor') editor.refresh();
    }

    function toggleGamepad() {
      gamepadEnabled = !gamepadEnabled;
      const btn = document.getElementById('padToggleBtn');
      btn.innerText = gamepadEnabled ? '🎮 Pad' : '🚫 Pad';
      btn.classList.toggle('active', gamepadEnabled);

      if (document.getElementById('previewView').classList.contains('active')) {
        document.getElementById('gamepadOverlay').style.display = gamepadEnabled ? 'block' : 'none';
      }
    }

    function logToUI(msg, level = 'info') {
      logCounter++;
      document.getElementById('logCount').innerText = logCounter;
      const el = document.createElement('div');
      el.className = `log-item log-${level}`;
      el.innerHTML = `<span class="log-time">${new Date().toLocaleTimeString().split(' ')[0]}</span> <span>${msg}</span>`;
      const container = document.getElementById('consoleLog');
      container.appendChild(el);
      container.scrollTop = container.scrollHeight;
    }

    window.addEventListener('message', e => {
      if (e.data && e.data.type === 'exec_log') {
        logToUI(e.data.message, e.data.level);
      }
    });

    // Touch D-Pad Handling
    function bindGamepadEvents() {
      const buttons = document.querySelectorAll('.dpad-btn, .action-btn');
      buttons.forEach(btn => {
        const key = btn.dataset.key;
        const press = (e) => {
          e.preventDefault();
          inputState[key] = true;
          btn.classList.add('pressed');
          syncInputToSandbox();
        };
        const release = (e) => {
          e.preventDefault();
          inputState[key] = false;
          btn.classList.remove('pressed');
          syncInputToSandbox();
        };
        btn.addEventListener('pointerdown', press);
        btn.addEventListener('pointerup', release);
        btn.addEventListener('pointercancel', release);
      });
    }
    bindGamepadEvents();

    function syncInputToSandbox() {
      const frame = document.getElementById('sandboxFrame');
      if (frame && frame.contentWindow) {
        frame.contentWindow.postMessage({ type: 'input_sync', state: inputState }, '*');
      }
    }

    function buildSandboxPayload(code) {
      return `<!DOCTYPE html>
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <style>
    * { margin:0; padding:0; box-sizing:border-box; }
    body { background:#000; overflow:hidden; width:100vw; height:100vh; }
  </style>
</head>
<body>
  <script>
    // Input Bridge
    window.Input = { up: false, down: false, left: false, right: false, a: false, b: false };
    window.addEventListener('message', (e) => {
      if (e.data && e.data.type === 'input_sync') {
        Object.assign(window.Input, e.data.state);
      }
    });

    // Sound Synthesizer API
    const AudioCtx = window.AudioContext || window.webkitAudioContext;
    const actx = AudioCtx ? new AudioCtx() : null;
    window.Sound = {
      play: (type) => {
        if (!actx) return;
        if (actx.state === 'suspended') actx.resume();
        const osc = actx.createOscillator();
        const gain = actx.createGain();
        osc.connect(gain);
        gain.connect(actx.destination);
        const t = actx.currentTime;

        if (type === 'laser') {
          osc.type = 'sawtooth';
          osc.frequency.setValueAtTime(880, t);
          osc.frequency.exponentialRampToValueAtTime(110, t + 0.15);
          gain.gain.setValueAtTime(0.3, t);
          gain.gain.linearRampToValueAtTime(0.01, t + 0.15);
          osc.start(t);
          osc.stop(t + 0.15);
        } else if (type === 'jump') {
          osc.type = 'square';
          osc.frequency.setValueAtTime(150, t);
          osc.frequency.exponentialRampToValueAtTime(450, t + 0.12);
          gain.gain.setValueAtTime(0.2, t);
          gain.gain.linearRampToValueAtTime(0.01, t + 0.12);
          osc.start(t);
          osc.stop(t + 0.12);
        } else if (type === 'coin') {
          osc.type = 'sine';
          osc.frequency.setValueAtTime(987, t);
          osc.frequency.setValueAtTime(1318, t + 0.08);
          gain.gain.setValueAtTime(0.25, t);
          gain.gain.linearRampToValueAtTime(0.01, t + 0.25);
          osc.start(t);
          osc.stop(t + 0.25);
        } else if (type === 'explosion') {
          osc.type = 'triangle';
          osc.frequency.setValueAtTime(100, t);
          osc.frequency.exponentialRampToValueAtTime(30, t + 0.3);
          gain.gain.setValueAtTime(0.4, t);
          gain.gain.linearRampToValueAtTime(0.01, t + 0.3);
          osc.start(t);
          osc.stop(t + 0.3);
        }
      }
    };

    // Haptics API
    window.Haptics = {
      buzz: (ms = 30) => { if (navigator.vibrate) navigator.vibrate(ms); }
    };

    // Logging Bridge
    ['log', 'warn', 'error'].forEach(lvl => {
      const fn = console[lvl];
      console[lvl] = (...args) => {
        fn.apply(console, args);
        parent.postMessage({
          type: 'exec_log',
          level: lvl,
          message: args.map(a => typeof a === 'object' ? JSON.stringify(a) : a).join(' ')
        }, '*');
      };
    });

    window.onerror = (m, u, l) => parent.postMessage({ type: 'exec_log', level: 'error', message: 'Line ' + l + ': ' + m }, '*');

    try {
      ${code}
    } catch(err) {
      console.error(err.message);
    }
  <\/script>
</body>
</html>`;
    }

    function executeCode() {
      const code = editor.getValue();
      const frame = document.getElementById('sandboxFrame');
      frame.srcdoc = buildSandboxPayload(code);
      switchTab('preview');
      setTimeout(syncInputToSandbox, 100);
    }

    function stopExecution() {
      document.getElementById('sandboxFrame').srcdoc = '';
      logToUI("Script stopped.", "warn");
    }

    function loadPreset(key) {
      if (PRESETS[key]) {
        editor.setValue(PRESETS[key]);
        logToUI(`Loaded preset: ${key}`, 'info');
      }
    }

    // --- PROJECT MANAGER ---
    function openProjects() {
      renderProjects();
      document.getElementById('projectModal').style.display = 'flex';
    }

    function closeProjects() {
      document.getElementById('projectModal').style.display = 'none';
    }

    function getSavedProjects() {
      return JSON.parse(localStorage.getItem('exec_projects') || '{}');
    }

    function renderProjects() {
      const projects = getSavedProjects();
      const list = document.getElementById('projectList');
      list.innerHTML = '';

      Object.keys(projects).forEach(name => {
        const item = document.createElement('div');
        item.className = 'project-item';
        item.innerHTML = `
          <span style="font-weight:600; color:#fff;">${name}</span>
          <div style="display:flex; gap:6px;">
            <button onclick="loadProject('${name}')" style="background:#38bdf8; color:#000;">Load</button>
            <button onclick="deleteProject('${name}')" style="background:#ef4444; color:#fff;">Delete</button>
          </div>
        `;
        list.appendChild(item);
      });
    }

    function saveNewProject() {
      const name = document.getElementById('newProjectName').value.trim();
      if (!name) return;
      const projects = getSavedProjects();
      projects[name] = editor.getValue();
      localStorage.setItem('exec_projects', JSON.stringify(projects));
      document.getElementById('newProjectName').value = '';
      renderProjects();
      logToUI(`Project saved: ${name}`, 'info');
    }

    function loadProject(name) {
      const projects = getSavedProjects();
      if (projects[name]) {
        editor.setValue(projects[name]);
        closeProjects();
        logToUI(`Loaded project: ${name}`, 'info');
      }
    }

    function deleteProject(name) {
      const projects = getSavedProjects();
      delete projects[name];
      localStorage.setItem('exec_projects', JSON.stringify(projects));
      renderProjects();
      logToUI(`Deleted project: ${name}`, 'warn');
    }

    // --- STANDALONE HTML EXPORTER ---
    function exportToHTML() {
      const code = editor.getValue();
      const fullHtml = buildSandboxPayload(code);
      const blob = new Blob([fullHtml], { type: 'text/html' });
      const a = document.createElement('a');
      a.href = URL.createObjectURL(blob);
      a.download = 'my-game.html';
      a.click();
      logToUI("Game exported as 'my-game.html'.", 'info');
    }
  </script>
</body>
</html>
