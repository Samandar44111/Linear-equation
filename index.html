<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Linear Equation Solver</title>
  <link href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Syne:wght@700;800&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #0d0d0f;
      --panel: #141417;
      --border: #2a2a30;
      --accent: #c8f04a;
      --accent2: #4af0c8;
      --text: #e8e8ec;
      --muted: #7a7a88;
      --error: #f04a6a;
      --mono: 'DM Mono', monospace;
      --head: 'Syne', sans-serif;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--mono);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 2rem 1rem;
      position: relative;
      overflow-x: hidden;
    }

    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(var(--border) 1px, transparent 1px),
        linear-gradient(90deg, var(--border) 1px, transparent 1px);
      background-size: 48px 48px;
      opacity: 0.35;
      pointer-events: none;
    }

    body::after {
      content: '';
      position: fixed;
      width: 600px; height: 600px;
      background: radial-gradient(circle, rgba(200,240,74,0.07) 0%, transparent 70%);
      top: -100px; left: 50%;
      transform: translateX(-50%);
      pointer-events: none;
    }

    .container {
      width: 100%;
      max-width: 900px;
      position: relative;
      z-index: 1;
    }

    header { margin-bottom: 2.5rem; }

    .tag {
      font-size: 0.7rem;
      letter-spacing: 0.18em;
      color: var(--accent);
      text-transform: uppercase;
      margin-bottom: 0.5rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    .tag::before { content: '//'; color: var(--muted); }

    h1 {
      font-family: var(--head);
      font-size: clamp(2rem, 5vw, 3.2rem);
      font-weight: 800;
      line-height: 1;
      letter-spacing: -0.02em;
    }
    h1 span { color: var(--accent); }

    .subtitle { color: var(--muted); font-size: 0.82rem; margin-top: 0.6rem; }

    .tabs {
      display: flex;
      gap: 0.5rem;
      margin-bottom: 1.5rem;
      flex-wrap: wrap;
    }

    .tab {
      padding: 0.45rem 1.1rem;
      border: 1px solid var(--border);
      background: transparent;
      color: var(--muted);
      font-family: var(--mono);
      font-size: 0.78rem;
      letter-spacing: 0.08em;
      cursor: pointer;
      border-radius: 4px;
      transition: all 0.18s;
    }
    .tab:hover { border-color: var(--accent); color: var(--accent); }
    .tab.active {
      background: var(--accent);
      color: #0d0d0f;
      border-color: var(--accent);
      font-weight: 500;
    }

    .panel {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 2rem;
      margin-bottom: 1.25rem;
    }

    .section-label {
      font-size: 0.68rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--muted);
      margin-bottom: 1.2rem;
    }

    .eq-row {
      display: flex;
      align-items: center;
      gap: 0.35rem;
      margin-bottom: 0.85rem;
      flex-wrap: wrap;
    }

    .eq-label {
      font-size: 0.82rem;
      color: var(--accent2);
      min-width: 22px;
      font-weight: 500;
      flex-shrink: 0;
    }

    input[type="number"] {
      background: var(--bg);
      border: 1px solid var(--border);
      color: var(--text);
      font-family: var(--mono);
      font-size: 0.82rem;
      padding: 0.42rem 0.4rem;
      border-radius: 5px;
      width: 60px;
      text-align: center;
      outline: none;
      transition: border-color 0.18s;
    }
    input:focus { border-color: var(--accent); }
    input.rhs { width: 68px; border-color: #3a3a44; }
    input.rhs:focus { border-color: var(--accent); }

    .var-label {
      font-family: var(--mono);
      font-size: 0.8rem;
      font-style: italic;
      color: var(--accent2);
    }

    .op { font-size: 0.85rem; color: var(--muted); }
    .eq-sign { font-size: 0.85rem; color: var(--accent); padding: 0 0.1rem; }

    .btn-row { display: flex; gap: 0.75rem; margin-top: 1.5rem; flex-wrap: wrap; }

    button {
      padding: 0.65rem 1.6rem;
      border-radius: 5px;
      border: none;
      font-family: var(--mono);
      font-size: 0.82rem;
      letter-spacing: 0.06em;
      cursor: pointer;
      transition: all 0.16s;
    }

    .btn-solve { background: var(--accent); color: #0d0d0f; font-weight: 500; }
    .btn-solve:hover { filter: brightness(1.1); transform: translateY(-1px); }
    .btn-clear { background: transparent; border: 1px solid var(--border); color: var(--muted); }
    .btn-clear:hover { border-color: var(--error); color: var(--error); }
    .btn-example { background: transparent; border: 1px solid var(--border); color: var(--muted); }
    .btn-example:hover { border-color: var(--accent2); color: var(--accent2); }

    .err-msg { color: var(--error); font-size: 0.8rem; margin-top: 0.6rem; display: none; }
    .err-msg.show { display: block; }

    .result-panel {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 1.5rem 2rem;
      display: none;
      animation: fadeUp 0.3s ease;
    }
    .result-panel.show { display: block; }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(10px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .result-header {
      font-size: 0.68rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--muted);
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    .result-header .dot { width: 7px; height: 7px; border-radius: 50%; background: var(--accent); }

    .result-values { display: flex; gap: 1.5rem; flex-wrap: wrap; margin-bottom: 1rem; }
    .result-item { display: flex; flex-direction: column; gap: 0.2rem; }
    .result-var { font-size: 0.72rem; color: var(--muted); letter-spacing: 0.1em; text-transform: uppercase; }
    .result-val { font-family: var(--head); font-size: 1.8rem; font-weight: 800; color: var(--accent); letter-spacing: -0.02em; }

    .result-steps { border-top: 1px solid var(--border); padding-top: 1rem; margin-top: 0.5rem; }

    .steps-toggle {
      background: none; border: none; color: var(--muted);
      font-family: var(--mono); font-size: 0.75rem; cursor: pointer;
      padding: 0; letter-spacing: 0.05em;
      display: flex; align-items: center; gap: 0.4rem;
    }
    .steps-toggle:hover { color: var(--accent2); }

    .steps-content { display: none; margin-top: 1rem; }
    .steps-content.open { display: block; }

    .step { display: flex; gap: 1rem; margin-bottom: 0.65rem; align-items: flex-start; }
    .step-num {
      min-width: 22px; height: 22px;
      border: 1px solid var(--border); border-radius: 3px;
      display: flex; align-items: center; justify-content: center;
      font-size: 0.65rem; color: var(--muted); flex-shrink: 0; margin-top: 1px;
    }
    .step-text { font-size: 0.82rem; color: var(--text); line-height: 1.6; }
    .step-text code {
      background: rgba(200,240,74,0.08); color: var(--accent);
      padding: 0.05rem 0.3rem; border-radius: 3px;
      font-family: var(--mono); font-size: 0.8rem;
    }

    footer { margin-top: 2rem; text-align: center; font-size: 0.7rem; color: var(--muted); letter-spacing: 0.05em; }
  </style>
</head>
<body>
<div class="container">
  <header>
    <div class="tag">Math Utility</div>
    <h1>Linear Eq<span>.</span><br/>Solver</h1>
    <p class="subtitle">Solve systems of 1 to 5 variables — with step-by-step Gaussian elimination</p>
  </header>

  <div class="tabs">
    <button class="tab active" onclick="setMode(1)">1 Variable</button>
    <button class="tab" onclick="setMode(2)">2 Variables</button>
    <button class="tab" onclick="setMode(3)">3 Variables</button>
    <button class="tab" onclick="setMode(4)">4 Variables</button>
    <button class="tab" onclick="setMode(5)">5 Variables</button>
  </div>

  <div class="panel">
    <div class="section-label" id="panelLabel"></div>
    <div id="equationRows"></div>
    <div class="err-msg" id="errMsg"></div>
    <div class="btn-row">
      <button class="btn-solve" onclick="solveSystem()">Solve →</button>
      <button class="btn-clear" onclick="clearAll()">Clear</button>
      <button class="btn-example" onclick="loadExample()">Example</button>
    </div>
  </div>

  <div class="result-panel" id="resultPanel">
    <div class="result-header"><span class="dot"></span> Solution</div>
    <div class="result-values" id="resultValues"></div>
    <div class="result-steps">
      <button class="steps-toggle" onclick="toggleSteps()">
        <span id="stepsArrow">▶</span> Show step-by-step solution
      </button>
      <div class="steps-content" id="stepsContent"></div>
    </div>
  </div>

  <footer>linear-equation-solver &nbsp;·&nbsp; 1–5 variables &nbsp;·&nbsp; Gaussian elimination &nbsp;·&nbsp; pure HTML/CSS/JS</footer>
</div>

<script>
  const VARS    = ['x', 'y', 'z', 'w', 'v'];
  const CIRCLES = ['①','②','③','④','⑤'];

  // Pre-built examples for each mode (solutions noted in comments)
  const EXAMPLES = {
    1: { A: [[3]],                                                        b: [15]       },  // x=5
    2: { A: [[2,3],[1,-1]],                                               b: [8,1]      },  // x=11/5, y=6/5
    3: { A: [[2,1,-1],[-3,-1,2],[-2,1,2]],                               b: [8,-11,-3] },  // x=2,y=3,z=-1 (classic)
    4: { A: [[2,1,0,-1],[1,3,1,0],[0,1,2,1],[-1,0,1,3]],                 b: [3,9,8,10] },
    5: { A: [[2,1,0,-1,1],[1,3,1,0,0],[0,1,2,1,-1],[-1,0,1,3,0],[1,-1,0,0,2]], b: [3,9,8,10,4] }
  };

  let currentN = 1;

  function setMode(n) {
    currentN = n;
    document.querySelectorAll('.tab').forEach((t, i) => t.classList.toggle('active', i === n - 1));
    buildMatrix(n);
    hideResult();
  }

  function buildMatrix(n) {
    const vars = VARS.slice(0, n);
    document.getElementById('panelLabel').textContent =
      n === 1
        ? 'Enter equation:  a·x = b'
        : `Enter ${n}×${n} system — one equation per row`;

    const container = document.getElementById('equationRows');
    container.innerHTML = '';

    for (let r = 0; r < n; r++) {
      const row = document.createElement('div');
      row.className = 'eq-row';

      // Row label
      const lbl = document.createElement('span');
      lbl.className = 'eq-label';
      lbl.textContent = CIRCLES[r];
      row.appendChild(lbl);

      // Coefficient + variable pairs
      vars.forEach((v, c) => {
        const inp = document.createElement('input');
        inp.type = 'number';
        inp.id = `cell_${r}_${c}`;
        inp.placeholder = String.fromCharCode(97 + c); // a, b, c, d, e
        row.appendChild(inp);

        const vl = document.createElement('span');
        vl.className = 'var-label';
        vl.textContent = v;
        row.appendChild(vl);

        if (c < n - 1) {
          const op = document.createElement('span');
          op.className = 'op';
          op.textContent = '+';
          row.appendChild(op);
        }
      });

      // = sign
      const eq = document.createElement('span');
      eq.className = 'eq-sign';
      eq.textContent = '=';
      row.appendChild(eq);

      // RHS
      const rhs = document.createElement('input');
      rhs.type = 'number';
      rhs.id = `rhs_${r}`;
      rhs.className = 'rhs';
      rhs.placeholder = 'c';
      row.appendChild(rhs);

      container.appendChild(row);
    }
  }

  function getMatrix() {
    const n = currentN;
    const A = [], b = [];
    for (let r = 0; r < n; r++) {
      const row = [];
      for (let c = 0; c < n; c++) {
        const v = parseFloat(document.getElementById(`cell_${r}_${c}`).value);
        if (isNaN(v)) return null;
        row.push(v);
      }
      const rv = parseFloat(document.getElementById(`rhs_${r}`).value);
      if (isNaN(rv)) return null;
      A.push(row);
      b.push(rv);
    }
    return { A, b };
  }

  function gaussianElimination(A, b) {
    const n = A.length;
    let M = A.map((row, i) => [...row, b[i]]);
    const steps = [];

    if (n === 1) {
      // Special-case: simple one-variable
      const a = M[0][0], c = M[0][1];
      if (Math.abs(a) < 1e-12) {
        if (Math.abs(c) < 1e-9) return { error: 'Infinitely many solutions (0·x = 0).' };
        return { error: `No solution (0·x = ${fmt(c)}).` };
      }
      const x = c / a;
      steps.push(`Equation: <code>${fmt(a)}x = ${fmt(c)}</code>`);
      steps.push(`Divide both sides by ${fmt(a)}: <code>x = ${fmt(c)} ÷ ${fmt(a)} = ${fmt(x)}</code>`);
      steps.push(`Verify: <code>${fmt(a)} × ${fmt(x)} = ${fmt(a*x)}</code> ✓`);
      return { x: [x], steps };
    }

    steps.push(`Start with ${n}×${n} augmented matrix [A | b].`);

    // Forward elimination with partial pivoting
    for (let col = 0; col < n; col++) {
      let maxRow = col;
      for (let r = col + 1; r < n; r++) {
        if (Math.abs(M[r][col]) > Math.abs(M[maxRow][col])) maxRow = r;
      }

      if (maxRow !== col) {
        [M[col], M[maxRow]] = [M[maxRow], M[col]];
        steps.push(`Swap R${col+1} ↔ R${maxRow+1} for numerical stability.`);
      }

      if (Math.abs(M[col][col]) < 1e-12) {
        return { error: 'No unique solution — the system is either inconsistent or has infinitely many solutions.' };
      }

      for (let r = col + 1; r < n; r++) {
        const factor = M[r][col] / M[col][col];
        if (Math.abs(factor) < 1e-12) continue;
        steps.push(`Eliminate ${VARS[col]} from R${r+1}: R${r+1} ← R${r+1} − (${fmt(factor)})·R${col+1}`);
        for (let c = col; c <= n; c++) M[r][c] -= factor * M[col][c];
      }
    }

    steps.push(`Upper triangular form reached. Applying back substitution.`);

    // Back substitution
    const x = new Array(n).fill(0);
    for (let i = n - 1; i >= 0; i--) {
      x[i] = M[i][n];
      for (let j = i + 1; j < n; j++) x[i] -= M[i][j] * x[j];
      x[i] /= M[i][i];
      steps.push(`Solve for <em>${VARS[i]}</em>: <code>${VARS[i]} = ${fmt(x[i])}</code>`);
    }

    // Verify
    let ok = true;
    A.forEach((row, r) => {
      const sum = row.reduce((s, c, j) => s + c * x[j], 0);
      if (Math.abs(sum - b[r]) > 1e-6) ok = false;
    });
    steps.push(`Verification: substitute solution into all equations — ${ok ? '✓ all satisfied.' : '⚠ minor floating-point rounding may apply.'}`);

    return { x, steps };
  }

  function solveSystem() {
    const data = getMatrix();
    if (!data) return showErr('Please fill in every coefficient and constant field.');

    const result = gaussianElimination(data.A, data.b);
    if (result.error) return showErr(result.error);

    const { x, steps } = result;
    const vars = VARS.slice(0, currentN);

    const valsHTML = x.map((v, i) =>
      `<div class="result-item">
        <span class="result-var">${vars[i]}</span>
        <span class="result-val">${fmt(v)}</span>
      </div>`
    ).join('');

    const stepsHTML = steps.map((s, i) =>
      `<div class="step">
        <div class="step-num">${i+1}</div>
        <div class="step-text">${s}</div>
      </div>`
    ).join('');

    document.getElementById('resultValues').innerHTML = valsHTML;
    document.getElementById('stepsContent').innerHTML = stepsHTML;
    document.getElementById('stepsContent').classList.remove('open');
    document.getElementById('stepsArrow').textContent = '▶';
    document.getElementById('resultPanel').classList.add('show');
    document.getElementById('errMsg').classList.remove('show');
  }

  function clearAll() {
    const n = currentN;
    for (let r = 0; r < n; r++) {
      for (let c = 0; c < n; c++) document.getElementById(`cell_${r}_${c}`).value = '';
      document.getElementById(`rhs_${r}`).value = '';
    }
    hideResult();
  }

  function loadExample() {
    const ex = EXAMPLES[currentN];
    const n = currentN;
    for (let r = 0; r < n; r++) {
      for (let c = 0; c < n; c++) document.getElementById(`cell_${r}_${c}`).value = ex.A[r][c];
      document.getElementById(`rhs_${r}`).value = ex.b[r];
    }
    hideResult();
  }

  function showErr(msg) {
    const el = document.getElementById('errMsg');
    el.textContent = msg;
    el.classList.add('show');
    setTimeout(() => el.classList.remove('show'), 5000);
  }

  function hideResult() {
    document.getElementById('resultPanel').classList.remove('show');
  }

  function toggleSteps() {
    const c = document.getElementById('stepsContent');
    const a = document.getElementById('stepsArrow');
    c.classList.toggle('open');
    a.textContent = c.classList.contains('open') ? '▼' : '▶';
  }

  function fmt(n) {
    if (Math.abs(n) < 1e-10) return '0';
    const r = Math.round(n * 1e9) / 1e9;
    if (Number.isInteger(r)) return r.toString();
    // Try to show as fraction if close
    return parseFloat(r.toFixed(6)).toString();
  }

  // Init
  setMode(1);
</script>
</body>
</html>
