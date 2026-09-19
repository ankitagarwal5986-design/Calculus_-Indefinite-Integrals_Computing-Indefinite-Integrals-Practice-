<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Brain and Mind Academy • Indefinite Integrals: 50-Problem Master Suite</title>

  <!-- MathJax Configuration & Loader -->
  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['\\(', '\\)'], ['$', '$']],
        displayMath: [['\\[', '\\]'], ['$$', '$$']],
        processEscapes: true
      },
      svg: { fontCache: 'global' }
    };
  </script>
  <script type="text/javascript" id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>

  <style>
    :root {
      --navy-dark: #0f172a;
      --brand-blue: #2563eb;
      --accent-cyan: #0284c7;
      --bg-tint: #f8fafc;
      --card-surf: #ffffff;
      --border-accent: #93c5fd;
      --border-soft: #cbd5e1;
      --green-ok: #059669;
      --green-surf: #d1fae5;
      --red-fail: #dc2626;
      --red-surf: #fee2e2;
      --brand-gold: #f59e0b;
      --gold-dark: #d97706;
      --gold-surf: #fef3c7;
      --text-main: #0f172a;
      --text-muted: #475569;

      /* User Requested Custom Styling: Light Blue Options, Green Correct, Red Wrong */
      --opt-blue-bg: #eff6ff;
      --opt-blue-border: #bfdbfe;
      --opt-blue-hover: #dbeafe;
      --opt-blue-active: #3b82f6;
      --opt-blue-text: #1e3a8a;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: var(--bg-tint);
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header {
      background: var(--navy-dark);
      color: #fff;
      padding: 14px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 12px rgba(15, 23, 42, 0.2);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .brand-wrap {
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .logo-badge {
      width: 44px;
      height: 44px;
      background: #ffffff;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.25);
    }

    .brand-title h1 {
      font-size: 1.15rem;
      font-weight: 700;
      letter-spacing: 0.5px;
    }

    .brand-title p {
      font-size: 0.78rem;
      color: #38bdf8;
      font-weight: 500;
    }

    .header-controls {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .chip {
      background: rgba(255, 255, 255, 0.12);
      border: 1px solid rgba(255, 255, 255, 0.25);
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.88rem;
      color: #ffffff;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .chip strong {
      color: #ffffff;
      font-weight: 800;
      letter-spacing: 0.3px;
    }

    .btn-icon {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.3);
      color: #fff;
      border-radius: 50%;
      width: 36px;
      height: 36px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1rem;
    }

    nav {
      background: #ffffff;
      border-bottom: 1px solid var(--border-soft);
      display: flex;
      justify-content: center;
      gap: 8px;
      padding: 8px 16px;
      flex-wrap: wrap;
    }

    nav button {
      background: none;
      border: none;
      outline: none;
      padding: 10px 20px;
      font-size: 0.92rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
      border-radius: 8px;
      transition: all 0.2s;
    }

    nav button.active {
      background: #eff6ff;
      color: var(--brand-blue);
      border-bottom: 3px solid var(--brand-blue);
    }

    main {
      flex: 1;
      padding: 24px;
      max-width: 1400px;
      margin: 0 auto;
      width: 100%;
    }

    .view {
      display: none;
    }

    .view.active {
      display: block;
    }

    #loginGateView {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(15, 23, 42, 0.94);
      backdrop-filter: blur(6px);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .login-box {
      background: #fff;
      padding: 36px;
      border-radius: 16px;
      width: 100%;
      max-width: 480px;
      text-align: center;
      box-shadow: 0 14px 35px rgba(0,0,0,0.3);
    }

    .login-box h2 {
      font-size: 1.45rem;
      color: var(--navy-dark);
      margin-bottom: 6px;
    }

    .login-box p {
      font-size: 0.88rem;
      color: var(--text-muted);
      margin-bottom: 20px;
      line-height: 1.5;
    }

    .resume-alert {
      display: none;
      background: #eff6ff;
      border: 1px solid var(--border-accent);
      border-radius: 8px;
      padding: 10px 14px;
      margin-bottom: 16px;
      font-size: 0.86rem;
      color: var(--navy-dark);
      text-align: left;
    }

    .login-box input {
      width: 100%;
      padding: 12px 16px;
      border: 1px solid var(--border-soft);
      border-radius: 8px;
      font-size: 1rem;
      margin-bottom: 16px;
      outline: none;
    }

    .btn-primary {
      background: var(--brand-blue);
      color: #fff;
      border: none;
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 8px;
      cursor: pointer;
      width: 100%;
      transition: background 0.2s;
    }

    .btn-primary:hover {
      background: #1d4ed8;
    }

    .btn-secondary {
      background: transparent;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 9px 18px;
      font-size: 0.88rem;
      font-weight: 600;
      border-radius: 6px;
      cursor: pointer;
      width: 100%;
      margin-top: 10px;
    }

    .btn-secondary:hover {
      background: var(--bg-tint);
    }

    .sheet-grid {
      display: grid;
      grid-template-columns: 1fr 340px;
      gap: 24px;
    }

    @media (max-width: 990px) {
      .sheet-grid {
        grid-template-columns: 1fr;
      }
    }

    .theory-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 24px;
      margin-bottom: 24px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.02);
    }

    .theory-card h3 {
      color: var(--navy-dark);
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 1.25rem;
    }

    .compendium-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      margin: 16px 0;
    }

    .comp-card {
      background: #ffffff;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      padding: 18px;
      display: flex;
      flex-direction: column;
      box-shadow: 0 2px 6px rgba(15, 23, 42, 0.04);
    }

    .comp-card h4 {
      color: var(--navy-dark);
      border-bottom: 2px solid var(--border-soft);
      padding-bottom: 8px;
      margin-bottom: 12px;
      font-size: 1.05rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .recap-body {
      font-size: 0.92rem;
      line-height: 1.65;
      color: var(--text-main);
    }

    .formula-box {
      background: #f8fafc;
      border-left: 4px solid var(--brand-blue);
      border-radius: 0 6px 6px 0;
      padding: 10px 14px;
      margin: 12px 0;
    }

    .media-card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 16px;
      margin: 16px 0;
    }

    .media-card {
      background: #f8fafc;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      padding: 16px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: transform 0.15s, border-color 0.15s;
    }

    .media-card:hover {
      transform: translateY(-2px);
      border-color: var(--brand-blue);
    }

    .media-badge {
      display: inline-block;
      align-self: flex-start;
      padding: 3px 8px;
      border-radius: 6px;
      font-size: 0.72rem;
      font-weight: 700;
      text-transform: uppercase;
      margin-bottom: 8px;
    }

    .badge-video { background: #fee2e2; color: #dc2626; }

    .media-link-btn {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      margin-top: 12px;
      padding: 8px 12px;
      border-radius: 6px;
      background: var(--navy-dark);
      color: #fff;
      font-size: 0.84rem;
      font-weight: 600;
      text-decoration: none;
      transition: background 0.15s;
    }

    .media-link-btn:hover {
      background: var(--brand-blue);
    }

    .question-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 26px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    }

    .concept-tag {
      display: inline-block;
      padding: 4px 10px;
      border-radius: 14px;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      margin-bottom: 8px;
      background: #e0f2fe;
      color: #0369a1;
      border: 1px solid #7dd3fc;
    }

    .hint-container {
      margin: 14px 0;
    }

    .btn-hint-toggle {
      background: #fffbeb;
      border: 1px solid #fde68a;
      color: #b45309;
      font-size: 0.86rem;
      font-weight: 600;
      padding: 7px 14px;
      border-radius: 6px;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s ease;
    }

    .btn-hint-toggle:hover {
      background: #fef3c7;
      border-color: #f59e0b;
    }

    .hint-box {
      display: none;
      background: #fffbeb;
      border-left: 4px solid #f59e0b;
      border-radius: 0 8px 8px 0;
      padding: 12px 16px;
      margin-top: 8px;
      font-size: 0.9rem;
      color: #92400e;
      line-height: 1.6;
    }

    /* Step Box Structure - Sequential Strict Reveal */
    .step-unit {
      margin-top: 18px;
      padding: 18px;
      background: #f8fafc;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      animation: fadeIn 0.3s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .step-unit.completed {
      border-color: #86efac;
      background: #f0fdf4;
    }

    .step-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
    }

    .step-title {
      font-size: 0.98rem;
      font-weight: 700;
      color: var(--navy-dark);
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .step-badge {
      font-size: 0.75rem;
      font-weight: 700;
      padding: 2px 8px;
      border-radius: 10px;
      background: #e2e8f0;
      color: #475569;
    }

    .step-badge.resolved {
      background: #dcfce7;
      color: #166534;
    }

    .mcq-container {
      display: grid;
      grid-template-columns: 1fr;
      gap: 10px;
      margin: 12px 0;
    }

    /* Light Blue Options with Proper Spacing */
    .mcq-option-btn {
      background: var(--opt-blue-bg);
      border: 2px solid var(--opt-blue-border);
      border-radius: 10px;
      padding: 13px 18px;
      text-align: left;
      font-size: 0.96rem;
      line-height: 1.5;
      color: var(--opt-blue-text);
      cursor: pointer;
      transition: all 0.15s ease;
      display: flex;
      align-items: center;
      gap: 14px;
      box-shadow: 0 2px 4px rgba(191, 219, 254, 0.25);
    }

    .mcq-option-btn:hover:not(:disabled) {
      background: var(--opt-blue-hover);
      border-color: var(--opt-blue-active);
      transform: translateY(-1px);
    }

    .mcq-option-btn.selected-correct {
      background: var(--green-surf) !important;
      border-color: var(--green-ok) !important;
      color: var(--green-ok) !important;
      font-weight: 700;
      box-shadow: none;
    }

    .mcq-option-btn.selected-wrong {
      background: var(--red-surf) !important;
      border-color: var(--red-fail) !important;
      color: var(--red-fail) !important;
      box-shadow: none;
    }

    .opt-letter {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 28px;
      height: 28px;
      border-radius: 50%;
      background: #ffffff;
      border: 2px solid var(--opt-blue-active);
      font-weight: 800;
      color: var(--opt-blue-text);
      flex-shrink: 0;
    }

    .opt-text-content {
      display: inline-block;
      white-space: normal;
      word-spacing: 0.05em;
    }

    /* Input Keyboard Styling */
    .virtual-keyboard {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 6px;
      background: #f1f5f9;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid var(--border-soft);
      margin-top: 12px;
      max-width: 320px;
    }

    .vk-btn {
      background: #ffffff;
      border: 1px solid var(--border-soft);
      padding: 8px;
      font-size: 0.95rem;
      font-weight: 700;
      color: var(--navy-dark);
      border-radius: 6px;
      cursor: pointer;
      text-align: center;
      transition: background 0.1s;
    }

    .vk-btn:hover {
      background: #e2e8f0;
    }

    .attempts-badge {
      font-size: 0.8rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 12px;
      background: #f1f5f9;
      color: #64748b;
      margin-left: 6px;
    }

    .step-feedback-box {
      margin-top: 12px;
      padding: 12px 14px;
      border-radius: 8px;
      font-size: 0.9rem;
      line-height: 1.6;
      display: block;
      animation: fadeIn 0.25s ease-in;
    }

    .step-feedback-box.correct {
      background: #ecfdf5;
      border-left: 4px solid var(--green-ok);
      color: #065f46;
    }

    .step-feedback-box.incorrect {
      background: #fef2f2;
      border-left: 4px solid var(--red-fail);
      color: #991b1b;
    }

    .btn-reveal-step {
      background: var(--brand-gold);
      color: #fff;
      border: none;
      padding: 6px 12px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.82rem;
      cursor: pointer;
      margin-top: 8px;
    }

    .btn-reveal-step:hover {
      background: var(--gold-dark);
    }

    .nav-toolbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 26px;
      padding-top: 18px;
      border-top: 1px solid var(--border-soft);
    }

    .nav-btn-group {
      display: flex;
      gap: 10px;
    }

    .btn-nav-action {
      background: #f8fafc;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 8px 18px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s;
    }

    .btn-nav-action:hover:not(:disabled) {
      background: var(--bg-tint);
      border-color: var(--brand-blue);
    }

    .btn-nav-action:disabled {
      opacity: 0.45;
      cursor: not-allowed;
    }

    .btn-skip {
      border-color: var(--brand-gold);
      color: var(--gold-dark);
      background: var(--gold-surf);
    }

    .palette-box {
      background: #fff;
      border: 1px solid var(--border-soft);
      border-radius: 12px;
      padding: 16px;
      margin-bottom: 20px;
    }

    .palette-legend {
      display: flex;
      justify-content: space-between;
      font-size: 0.72rem;
      margin: 8px 0 12px 0;
      padding: 6px 8px;
      background: var(--bg-tint);
      border-radius: 6px;
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: 4px;
      font-weight: 600;
    }

    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
    }

    .palette-grid {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 6px;
      margin-bottom: 12px;
      max-height: 380px;
      overflow-y: auto;
      padding-right: 4px;
    }

    .palette-btn {
      aspect-ratio: 1;
      border: 1px solid var(--border-soft);
      background: var(--bg-tint);
      border-radius: 6px;
      font-weight: 700;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      transition: all 0.15s;
      font-size: 0.82rem;
      color: var(--navy-dark);
    }

    .palette-btn.active {
      border: 2px solid var(--navy-dark) !important;
      background: #bfdbfe;
      color: #1e3a8a;
    }

    .palette-btn.completed {
      background: var(--green-ok) !important;
      color: #fff !important;
      border-color: var(--green-ok) !important;
    }

    .palette-btn.partial {
      background: var(--brand-gold) !important;
      color: #fff !important;
      border-color: var(--gold-dark) !important;
    }

    .hero-score-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 28px;
      text-align: center;
      margin-bottom: 24px;
      box-shadow: 0 4px 14px rgba(0,0,0,0.03);
    }

    .student-badge {
      display: inline-block;
      background: var(--bg-tint);
      border: 1px solid var(--border-accent);
      padding: 6px 18px;
      border-radius: 20px;
      font-size: 1rem;
      margin-bottom: 14px;
      color: var(--navy-dark);
    }

    .student-badge strong {
      color: var(--brand-blue);
    }

    .score-badge {
      font-size: 3rem;
      font-weight: 800;
      color: var(--brand-blue);
      margin: 8px 0;
    }

    .progress-bar-wrap {
      width: 100%;
      height: 12px;
      background: #e2e8f0;
      border-radius: 6px;
      overflow: hidden;
      margin: 16px 0;
    }

    .progress-bar-fill {
      height: 100%;
      background: var(--green-ok);
      width: 0%;
      transition: width 0.3s ease;
    }

    .toast {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 20px;
      border-radius: 8px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.2);
      display: none;
      z-index: 1000;
    }

    @media print {
      header, nav, .palette-box, .btn-primary, #loginGateView, .nav-toolbar, .btn-hint-toggle {
        display: none !important;
      }
      body { background: #fff; }
      main { width: 100%; max-width: 100%; padding: 0; }
      .sheet-grid { display: block; }
      .view { display: block !important; }
    }
  </style>
</head>
<body>

  <header>
    <div class="brand-wrap">
      <div class="logo-badge">
        <svg width="34" height="34" viewBox="0 0 100 100" fill="none">
          <circle cx="50" cy="50" r="44" stroke="#2563eb" stroke-width="7"/>
          <path d="M 28 50 L 72 50" stroke="#0284c7" stroke-width="7" stroke-linecap="round"/>
          <circle cx="50" cy="50" r="7" fill="#f59e0b"/>
        </svg>
      </div>
      <div class="brand-title">
        <h1>Brain and Mind Academy • Indefinite Integrals</h1>
        <p>Complete 50-Problem Master Suite • Antiderivatives &amp; Computing Rules</p>
      </div>
    </div>
    <div class="header-controls">
      <div class="chip" id="timerChip">⏱️ 00:00</div>
      <div class="chip" id="userPill"><strong>Student: Guest</strong></div>
      <button class="btn-icon" id="audioToggleBtn" title="Toggle Audio">🔊</button>
    </div>
  </header>

  <nav>
    <button class="tab-btn active" id="tabTheoryBtn" onclick="switchMainTab('theory')">
      📖 Theory, Notes &amp; Video Hub
    </button>
    <button class="tab-btn" id="tabPracticeBtn" onclick="switchMainTab('practice')">
      🎯 Interactive Practice Workstation (50 Problems)
    </button>
    <button class="tab-btn" id="tabScorecardBtn" onclick="switchMainTab('scorecard')">
      📊 Master Scorecard &amp; Solutions
    </button>
  </nav>

  <!-- Login Modal with Session Persistence -->
  <div id="loginGateView">
    <div class="login-box">
      <h2>Brain and Mind Academy</h2>
      <p>Calculus I • Indefinite Integrals Practice with Step-Gating &amp; Virtual Keyboard</p>
      
      <div id="resumeAlertBox" class="resume-alert">
        <strong>Saved Session Found!</strong><br>
        <span id="savedSessionDetails"></span>
      </div>

      <input type="text" id="studentNameInput" placeholder="Enter Student Name" />
      <button class="btn-primary" id="startSessionBtn" onclick="initDirectLogin(false)">Start Learning Session</button>
      <button class="btn-secondary" id="resumeSessionBtn" style="display:none;" onclick="initDirectLogin(true)">Resume Saved Session</button>
    </div>
  </div>

  <main>
    <!-- View 1: Theory, Descriptive Notes & Video Hub (First Sheet) -->
    <div id="viewTheory" class="view active">
      <div class="theory-card">
        <h3>📖 Indefinite Integrals &amp; Computing Integrals: Comprehensive Hub</h3>
        <p class="theory-intro-text">
          An indefinite integral represents the family of all antiderivatives of a function. Review the descriptive notes and master integration techniques with our curated video lessons below.
        </p>

        <div class="compendium-grid">
          <div class="comp-card">
            <h4>1. Definition of Antiderivative</h4>
            <div class="recap-body">
              <div class="formula-box">
                \[\int f(x) \, dx = F(x) + C \iff F'(x) = f(x)\]
                <p>The constant of integration \(+C\) accounts for the fact that derivatives of constants are zero.</p>
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>2. Basic Integration Formulas &amp; Linearity</h4>
            <div class="recap-body">
              <div class="formula-box">
                <p>• Power Rule: \(\int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad (n \neq -1)\)</p>
                <p>• Reciprocal Rule: \(\int \frac{1}{x} \, dx = \ln|x| + C\)</p>
                <p>• Exponential: \(\int e^x \, dx = e^x + C\)</p>
                <p>• Trig: \(\int \cos x \, dx = \sin x + C, \quad \int \sin x \, dx = -\cos x + C\)</p>
              </div>
            </div>
          </div>
        </div>

        <h4 style="font-size: 1.1rem; color: var(--navy-dark); margin: 24px 0 12px 0;">🎬 Curated Calculus I Video Lessons</h4>
        <div class="media-card-grid">
          <div class="media-card">
            <div>
              <span class="media-badge badge-video">Lamar / Calculus Video</span>
              <h5 style="font-size:0.95rem; color:var(--navy-dark); margin-bottom:4px;">Introduction to Indefinite Integrals</h5>
              <p style="font-size:0.84rem; color:var(--text-muted);">Understanding antiderivatives and the constant of integration.</p>
            </div>
            <a href="https://tutorial.math.lamar.edu/Classes/CalcI/IndefiniteIntegrals.aspx" target="_blank" rel="noopener noreferrer" class="media-link-btn">
              📖 Open Lamar Notes
            </a>
          </div>

          <div class="media-card">
            <div>
              <span class="media-badge badge-video">Calculus Tutorial</span>
              <h5 style="font-size:0.95rem; color:var(--navy-dark); margin-bottom:4px;">Computing Indefinite Integrals</h5>
              <p style="font-size:0.84rem; color:var(--text-muted);">Step-by-step application of power rule, trig formulas, and linearity.</p>
            </div>
            <a href="https://tutorial.math.lamar.edu/Classes/CalcI/ComputingIndefiniteIntegrals.aspx" target="_blank" rel="noopener noreferrer" class="media-link-btn">
              📖 Open Computing Guide
            </a>
          </div>
        </div>

        <div style="margin-top: 30px; text-align: center;">
          <button class="btn-primary" style="max-width: 320px; font-size: 1.05rem; padding: 14px 28px;" onclick="switchMainTab('practice')">
            Launch Practice Workstation ➔
          </button>
        </div>
      </div>
    </div>

    <!-- View 2: Interactive Practice Workstation -->
    <div id="viewPractice" class="view">
      <div class="sheet-grid">
        <div>
          <!-- Question Workstation Card -->
          <div class="question-card" id="activeQuestionCard"></div>
        </div>

        <aside>
          <div class="palette-box">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px;">
              <h4>All 50 Problems</h4>
              <span style="font-size:0.8rem; color:var(--text-muted);" id="paletteCount">0 / 50 Solved</span>
            </div>

            <div class="palette-legend">
              <div class="legend-item"><span class="legend-dot" style="background:var(--green-ok);"></span> Completed</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f59e0b;"></span> In Progress</div>
              <div class="legend-item"><span class="legend-dot" style="background:#bfdbfe;"></span> Active</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f0f9ff; border:1px solid #bae6fd;"></span> Unseen</div>
            </div>
            
            <div class="palette-grid" id="paletteGrid"></div>
            
            <button class="btn-primary" style="margin-top: 10px; background: var(--navy-dark);" onclick="switchMainTab('scorecard')">
              📊 View Evaluation Scorecard
            </button>
            <button class="btn-secondary" style="margin-top: 8px; border-color: #cbd5e1;" onclick="resetStudentProgress()">
              🔄 Reset All Progress
            </button>
          </div>

          <div class="palette-box" style="background: #f8fafc;">
            <h4 style="font-size: 0.92rem; margin-bottom: 8px; color: var(--navy-dark);">Workstation Rules</h4>
            <p style="font-size: 0.82rem; line-height: 1.6; color: var(--text-muted);">
              • <strong>Step-Gating:</strong> Step 2 remains locked until Step 1 is verified.<br/>
              • <strong>Color Customization:</strong> Options are light blue; correct is green, wrong is red.<br/>
              • <strong>Virtual Keyboard:</strong> Use integration symbols and exponents easily.
            </p>
          </div>
        </aside>
      </div>
    </div>

    <!-- View 3: Complete Scorecard & Master Solutions -->
    <div id="viewScorecard" class="view">
      <div class="hero-score-card">
        <h2>Brain and Mind Academy Scorecard</h2>
        <div class="student-badge" id="reportStudentBadge"><strong>Student: Guest</strong></div>
        <div class="score-badge" id="scoreValue">0 / 50</div>
        <div class="progress-bar-wrap">
          <div class="progress-bar-fill" id="progressBarFill"></div>
        </div>
        <p id="scoreSubtitle" style="font-size:1.02rem; font-weight:600; color:var(--navy-dark); margin-top:8px;">
          Review all problem solutions and step evaluations below.
        </p>
        <button class="btn-primary" style="margin-top: 14px; max-width: 240px;" onclick="window.print()">🖨️ Print Final Scorecard</button>
      </div>

      <div id="completeSolutionsContainer"></div>
    </div>
  </main>

  <div class="toast" id="toastMessage"></div>

  <script>
    /* ==========================================================================
       COMPLETE 50-PROBLEM DATASET FOR INDEFINITE INTEGRALS
       Options A, B, C, D are dynamically mixed using deterministic pseudo-random index
       ========================================================================== */
    const rawIntegrals = [
      { id: 1, title: "Problem 1", expr: "\\int (12x^2 - 5) \\, dx", hint: "Apply the power rule to 12x^2 and integrate the constant 5.", ans: "4x^3 - 5x + C", dist1: "24x - 5 + C", dist2: "4x^3 - 5 + C", dist3: "12x^3 - 5x + C" },
      { id: 2, title: "Problem 2", expr: "\\int (3t^2 - 8t + 7) \\, dt", hint: "Integrate each polynomial term separately.", ans: "t^3 - 4t^2 + 7t + C", dist1: "6t - 8 + C", dist2: "3t^3 - 4t^2 + 7t + C", dist3: "\\frac{3}{3}t^3 - 8t^2 + 7t + C" },
      { id: 3, title: "Problem 3", expr: "\\int (9z^2 - 4z + 1) \\, dz", hint: "Power rule for each term.", ans: "3z^3 - 2z^2 + z + C", dist1: "18z - 4 + C", dist2: "9z^3 - 2z^2 + z + C", dist3: "3z^3 - 4z^2 + z + C" },
      { id: 4, title: "Problem 4", expr: "\\int (10w^4 - 6w + 3) \\, dw", hint: "Integrate term by term.", ans: "2w^5 - 3w^2 + 3w + C", dist1: "40w^3 - 6 + C", dist2: "10w^5 - 3w^2 + 3w + C", dist3: "2w^5 - 6w^2 + 3w + C" },
      { id: 5, title: "Problem 5", expr: "\\int (x^4 - 2x^3 + x^2 - x + 1) \\, dx", hint: "5-term polynomial integration.", ans: "\\frac{1}{5}x^5 - \\frac{1}{2}x^4 + \\frac{1}{3}x^3 - \\frac{1}{2}x^2 + x + C", dist1: "4x^4 - 6x^2 + 2x - 1 + C", dist2: "\\frac{1}{4}x^5 - \\frac{1}{3}x^4 + \\frac{1}{2}x^3 - x^2 + x + C", dist3: "\\frac{1}{5}x^5 - 2x^4 + x^3 - x^2 + x + C" },
      { id: 6, title: "Problem 6", expr: "\\int (7\\sqrt{w} + 2w^{-3}) \\, dw", hint: "Convert \\(\\sqrt{w}\\) to \\(w^{1/2}\\).", ans: "\\frac{14}{3}w^{3/2} - w^{-2} + C", dist1: "\\frac{7}{2}w^{3/2} + 2w^{-2} + C", dist2: "14w^{3/2} - \\frac{1}{2}w^{-2} + C", dist3: "\\frac{14}{3}w^{3/2} + w^{-2} + C" },
      { id: 7, title: "Problem 7", expr: "\\int (4\\sqrt[3]{x} - 5x^{-4}) \\, dx", hint: "Rewrite as \\(4x^{1/3} - 5x^{-4}\\).", ans: "3x^{4/3} + \\frac{5}{3x^3} + C", dist1: "\\frac{4}{3}x^{4/3} - \\frac{5}{3}x^{-3} + C", dist2: "3x^{4/3} - \\frac{5}{3x^3} + C", dist3: "12x^{4/3} + 20x^{-3} + C" },
      { id: 8, title: "Problem 8", expr: "\\int (3x^{-2} - \\frac{1}{4}x^{-5}) \\, dx", hint: "Rewrite with negative exponents.", ans: "-\\frac{3}{x} + \\frac{1}{12x^4} + C", dist1: "-\\frac{3}{x} - \\frac{1}{12x^4} + C", dist2: "-6x^{-3} + \\frac{5}{4}x^{-6} + C", dist3: "\\frac{3}{x} - \\frac{1}{12x^4} + C" },
      { id: 9, title: "Problem 9", expr: "\\int (x^{-1/2} + 4x^{-1/4}) \\, dx", hint: "Power rule for fractional exponents.", ans: "2\\sqrt{x} + \\frac{16}{3}x^{3/4} + C", dist1: "-2\\sqrt{x} - 16x^{3/4} + C", dist2: "\\frac{1}{2}\\sqrt{x} + \\frac{3}{16}x^{3/4} + C", dist3: "2\\sqrt{x} - \\frac{16}{3}x^{3/4} + C" },
      { id: 10, title: "Problem 10", expr: "\\int (2z^{3/4} - 5z^{-1/2}) \\, dz", hint: "Power rule for fractional exponents.", ans: "\\frac{8}{7}z^{7/4} - 10z^{1/2} + C", dist1: "\\frac{3}{2}z^{-1/4} + \\frac{5}{2}z^{-3/2} + C", dist2: "\\frac{8}{7}z^{7/4} + 10z^{1/2} + C", dist3: "\\frac{5}{4}z^{7/4} - \\frac{5}{2}z^{1/2} + C" },
      { id: 11, title: "Problem 11", expr: "\\int (\\frac{5}{t} - 3e^t + 2) \\, dt", hint: "Recall \\(\\int \\frac{1}{t}dt = \\ln|t|\\).", ans: "5\\ln|t| - 3e^t + 2t + C", dist1: "-\\frac{5}{t^2} - 3e^t + C", dist2: "5\\ln|t| + 3e^t + 2t + C", dist3: "5\\ln|t| - 3e^t + C" },
      { id: 12, title: "Problem 12", expr: "\\int (4e^x - \\frac{2}{x} + x^{-3}) \\, dx", hint: "Integrate each standard form.", ans: "4e^x - 2\\ln|x| - \\frac{1}{2x^2} + C", dist1: "4e^x + 2\\ln|x| + \\frac{1}{2x^2} + C", dist2: "4e^x - 2\\ln|x| + \\frac{1}{2x^2} + C", dist3: "4e^x - \\frac{2}{x^2} - \\frac{3}{x^4} + C" },
      { id: 13, title: "Problem 13", expr: "\\int (\\frac{6}{w} + 7e^w - 4w^{1/2}) \\, dw", hint: "Term by term integration.", ans: "6\\ln|w| + 7e^w - \\frac{8}{3}w^{3/2} + C", dist1: "-6w^{-2} + 7e^w - 2w^{1/2} + C", dist2: "6\\ln|w| - 7e^w - \\frac{8}{3}w^{3/2} + C", dist3: "6\\ln|w| + 7e^w + \\frac{8}{3}w^{3/2} + C" },
      { id: 14, title: "Problem 14", expr: "\\int (8\\cos x - 3\\sin x) \\, dx", hint: "\\(\\int \\cos x = \\sin x\\), \\(\\int \\sin x = -\\cos x\\).", ans: "8\\sin x + 3\\cos x + C", dist1: "-8\\sin x + 3\\cos x + C", dist2: "8\\sin x - 3\\cos x + C", dist3: "-8\\cos x - 3\\sin x + C" },
      { id: 15, title: "Problem 15", expr: "\\int (\\csc^2 x + 5\\sec x \\tan x) \\, dx", hint: "Trig antiderivatives.", ans: "-\\cot x + 5\\sec x + C", dist1: "\\cot x + 5\\sec x + C", dist2: "-\\cot x - 5\\sec x + C", dist3: "\\tan x + 5\\csc x + C" },
      { id: 16, title: "Problem 16", expr: "\\int (2\\csc x \\cot x - 3\\sec^2 x) \\, dx", hint: "Trig antiderivatives.", ans: "-2\\csc x - 3\\tan x + C", dist1: "2\\csc x - 3\\tan x + C", dist2: "-2\\csc x + 3\\tan x + C", dist3: "2\\cot x - 3\\sec x + C" },
      { id: 17, title: "Problem 17", expr: "\\int (4\\sin t - 9\\cos t + e^t) \\, dt", hint: "Combine trig and exponential rules.", ans: "-4\\cos t - 9\\sin t + e^t + C", dist1: "4\\cos t + 9\\sin t + e^t + C", dist2: "-4\\cos t + 9\\sin t + e^t + C", dist3: "4\\sin t - 9\\cos t + e^t + C" },
      { id: 18, title: "Problem 18", expr: "\\int (10\\sec^2 u - 2\\csc u \\cot u + 1) \\, du", hint: "Standard trig formulas.", ans: "10\\tan u + 2\\csc u + u + C", dist1: "10\\tan u - 2\\csc u + u + C", dist2: "10\\sec u + 2\\cot u + u + C", dist3: "10\\tan u + 2\\cot u + u + C" },
      { id: 19, title: "Problem 19", expr: "\\int (x + 5)(2x - 1) \\, dx", hint: "Expand product first.", ans: "\\frac{2}{3}x^3 + \\frac{9}{2}x^2 - 5x + C", dist1: "x^2 - 5 + C", dist2: "\\frac{2}{3}x^3 + 9x^2 - 5x + C", dist3: "2x^3 + 9x^2 - 5x + C" },
      { id: 20, title: "Problem 20", expr: "\\int (3y - 2)^2 \\, dy", hint: "Expand binomial square.", ans: "3y^3 - 6y^2 + 4y + C", dist1: "9y^3 - 12y^2 + 4y + C", dist2: "\\frac{9}{3}y^3 - 3y^2 + 4y + C", dist3: "\\frac{1}{3}(3y-2)^3 + C" },
      { id: 21, title: "Problem 21", expr: "\\int \\frac{x^3 - 4x^2 + 5}{x^2} \\, dx", hint: "Divide each term by \\(x^2\\).", ans: "\\frac{1}{2}x^2 - 4x - \\frac{5}{x} + C", dist1: "\\frac{1}{2}x^2 - 4x + \\frac{5}{x} + C", dist2: "x^2 - 4x - \\frac{5}{x} + C", dist3: "\\frac{1}{2}x^2 + 4x - \\frac{5}{x} + C" },
      { id: 22, title: "Problem 22", expr: "\\int \\frac{2w^4 - w^2 + 3}{w} \\, dw", hint: "Divide by \\(w\\).", ans: "\\frac{1}{2}w^4 - \\frac{1}{2}w^2 + 3\\ln|w| + C", dist1: "2w^4 - w^2 + 3\\ln|w| + C", dist2: "\\frac{1}{2}w^4 - w^2 + 3\\ln|w| + C", dist3: "\\frac{2}{3}w^3 - w + 3\\ln|w| + C" },
      { id: 23, title: "Problem 23", expr: "\\int \\frac{z^2 - 4}{z - 2} \\, dz", hint: "Factor numerator: \\((z-2)(z+2)\\).", ans: "\\frac{1}{2}z^2 + 2z + C", dist1: "z + 2 + C", dist2: "\\frac{1}{2}z^2 - 2z + C", dist3: "z^2 + 2z + C" },
      { id: 24, title: "Problem 24", expr: "\\int \\frac{t^3 + 1}{t + 1} \\, dt", hint: "Factor sum of cubes: \\(t^3 + 1 = (t+1)(t^2 - t + 1)\\).", ans: "\\frac{1}{3}t^3 - \\frac{1}{2}t^2 + t + C", dist1: "\\frac{1}{3}t^3 + \\frac{1}{2}t^2 + t + C", dist2: "t^2 - t + 1 + C", dist3: "\\frac{1}{3}t^3 - t^2 + t + C" },
      { id: 25, title: "Problem 25", expr: "\\int (5x^4 - 2x^3 + 8x - 3) \\, dx", hint: "Power rule.", ans: "x^5 - \\frac{1}{2}x^4 + 4x^2 - 3x + C", dist1: "20x^3 - 6x^2 + 8 + C", dist2: "x^5 - 2x^4 + 4x^2 - 3x + C", dist3: "\\frac{5}{4}x^5 - \\frac{2}{4}x^4 + 4x^2 - 3x + C" },
      { id: 26, title: "Problem 26", expr: "\\int (10 - 3t + 2t^2 - t^3) \\, dt", hint: "Polynomial integration.", ans: "10t - \\frac{3}{2}t^2 + \\frac{2}{3}t^3 - \\frac{1}{4}t^4 + C", dist1: "-3 + 4t - 3t^2 + C", dist2: "10t - 3t^2 + 2t^3 - t^4 + C", dist3: "10t - \\frac{3}{2}t^2 + \\frac{2}{3}t^3 - \\frac{1}{3}t^4 + C" },
      { id: 27, title: "Problem 27", expr: "\\int (z^5 - z^{-5}) \\, dz", hint: "Power rule for negative exponents.", ans: "\\frac{1}{6}z^6 + \\frac{1}{4z^4} + C", dist1: "\\frac{1}{6}z^6 - \\frac{1}{4z^4} + C", dist2: "5z^4 + 5z^{-6} + C", dist3: "\\frac{1}{5}z^6 + \\frac{1}{5}z^{-4} + C" },
      { id: 28, title: "Problem 28", expr: "\\int (4x^{3/4} + 2x^{-1/2}) \\, dx", hint: "Exponents \\(3/4\\) and \\(-1/2\\).", ans: "\\frac{16}{7}x^{7/4} + 4\\sqrt{x} + C", dist1: "3x^{7/4} + 4\\sqrt{x} + C", dist2: "\\frac{16}{7}x^{7/4} - 4\\sqrt{x} + C", dist3: "\\frac{7}{16}x^{7/4} + 2\\sqrt{x} + C" },
      { id: 29, title: "Problem 29", expr: "\\int (e^u - 4\\cos u + u^{-1}) \\, du", hint: "Standard forms.", ans: "e^u - 4\\sin u + \\ln|u| + C", dist1: "e^u + 4\\sin u + \\ln|u| + C", dist2: "e^u - 4\\sin u - \\ln|u| + C", dist3: "e^u + 4\\cos u + \\ln|u| + C" },
      { id: 30, title: "Problem 30", expr: "\\int (2\\sec^2 x - 7\\csc^2 x) \\, dx", hint: "Trig antiderivatives.", ans: "2\\tan x + 7\\cot x + C", dist1: "2\\tan x - 7\\cot x + C", dist2: "-2\\tan x - 7\\cot x + C", dist3: "2\\sec x + 7\\csc x + C" },
      { id: 31, title: "Problem 31", expr: "\\int (2x - 1)(3x + 2) \\, dx", hint: "Expand binomials.", ans: "2x^3 + \\frac{1}{2}x^2 - 2x + C", dist1: "6x^3 + x^2 - 2x + C", dist2: "6x^3 + \\frac{1}{2}x^2 - 2x + C", dist3: "6x^2 + x - 2 + C" },
      { id: 32, title: "Problem 32", expr: "\\int (x - 2)^3 \\, dx", hint: "Expand cube.", ans: "\\frac{1}{4}x^4 - 2x^3 + 6x^2 - 8x + C", dist1: "\\frac{1}{4}x^4 - 6x^3 + 12x^2 - 8x + C", dist2: "\\frac{1}{3}(x-2)^4 + C", dist3: "3(x-2)^2 + C" },
      { id: 33, title: "Problem 33", expr: "\\int \\frac{3x^4 - x^2 + 5}{x^3} \\, dx", hint: "Divide numerator terms by \\(x^3\\).", ans: "\\frac{3}{2}x^2 - \\ln|x| - \\frac{5}{2x^2} + C", dist1: "3x - \\ln|x| + \\frac{15}{x^4} + C", dist2: "\\frac{3}{2}x^2 + \\ln|x| - \\frac{5}{2x^2} + C", dist3: "3x^2 - \\ln|x| - \\frac{5}{x^2} + C" },
      { id: 34, title: "Problem 34", expr: "\\int \\frac{2e^x - 5}{e^x} \\, dx", hint: "Divide by \\(e^x\\): \\(2 - 5e^{-x}\\).", ans: "2x + 5e^{-x} + C", dist1: "2x - 5e^{-x} + C", dist2: "2 - 5e^{-x} + C", dist3: "2x + 5\\ln|e^x| + C" },
      { id: 35, title: "Problem 35", expr: "\\int (\\frac{4}{1+x^2} - \\frac{2}{\\sqrt{1-x^2}}) \\, dx", hint: "Inverse trig integrals.", ans: "4\\arctan x - 2\\arcsin x + C", dist1: "4\\arcsin x - 2\\arctan x + C", dist2: "-4\\arctan x + 2\\arcsin x + C", dist3: "4\\arctan x + 2\\arcsin x + C" },
      { id: 36, title: "Problem 36", expr: "\\int (9^x - \\frac{1}{x}) \\, dx", hint: "Recall \\(\\int a^x dx = \\frac{a^x}{\\ln a} + C\\).", ans: "\\frac{9^x}{\\ln 9} - \\ln|x| + C", dist1: "9^x \\ln 9 - \\ln|x| + C", dist2: "\\frac{9^x}{\\ln 9} + \\ln|x| + C", dist3: "9^x - \\ln|x| + C" },
      { id: 37, title: "Problem 37", expr: "\\int (1 + \\tan^2 t) \\, dt", hint: "Use identity \\(1 + \\tan^2 t = \\sec^2 t\\).", ans: "\\tan t + C", dist1: "t + \\frac{1}{3}\\tan^3 t + C", dist2: "\\sec^2 t + C", dist3: "\\cot t + C" },
      { id: 38, title: "Problem 38", expr: "\\int \\frac{\\cos^2 x - 1}{\\sin^2 x} \\, dx", hint: "Use \\(\\cos^2 x - 1 = -\\sin^2 x\\).", ans: "-x + C", dist1: "-x + C", dist2: "x + C", dist3: "\\cot x + C" },
      { id: 39, title: "Problem 39", expr: "\\int (x^e + e^x + e^2) \\, dx", hint: "Note \\(e\\) is a constant.", ans: "\\frac{1}{e+1}x^{e+1} + e^x + e^2 x + C", dist1: "ex^{e-1} + e^x + e^2 + C", dist2: "\\frac{1}{e}x^e + e^x + e^2 x + C", dist3: "\\frac{1}{e+1}x^{e+1} + e^x + e + C" },
      { id: 40, title: "Problem 40", expr: "\\int (\\frac{1}{3x} - \\frac{3}{x}) \\, dx", hint: "Combine like terms.", ans: "-\\frac{8}{3}\\ln|x| + C", dist1: "\\frac{8}{3}\\ln|x| + C", dist2: "-\\frac{8}{3x^2} + C", dist3: "-\\frac{8}{3}\\ln|3x| + C" },
      { id: 41, title: "Problem 41", expr: "\\int (2^x + 3 \\cdot 5^x) \\, dx", hint: "Exponential integrals.", ans: "\\frac{2^x}{\\ln 2} + \\frac{3 \\cdot 5^x}{\\ln 5} + C", dist1: "2^x \\ln 2 + 15^x \\ln 5 + C", dist2: "\\frac{2^x}{\\ln 2} + \\frac{5^x}{\\ln 5} + C", dist3: "2^x + 3(5^x) + C" },
      { id: 42, title: "Problem 42", expr: "\\int (\\sinh x + \\cosh x) \\, dx", hint: "Hyperbolic integrals.", ans: "\\cosh x + \\sinh x + C", dist1: "\\sinh x - \\cosh x + C", dist2: "\\cosh x - \\sinh x + C", dist3: "2\\cosh x + C" },
      { id: 43, title: "Problem 43", expr: "\\int (4x^3 - x^{-4} + 2) \\, dx", hint: "Power rule.", ans: "x^4 + \\frac{1}{3x^3} + 2x + C", dist1: "x^4 - \\frac{1}{3x^3} + 2x + C", dist2: "12x^2 + \\frac{4}{x^5} + C", dist3: "x^4 + \\frac{3}{x^3} + 2x + C" },
      { id: 44, title: "Problem 44", expr: "\\int (x^{2/5} + x^{3/2}) \\, dx", hint: "Fractional exponents.", ans: "\\frac{5}{7}x^{7/5} + \\frac{2}{5}x^{5/2} + C", dist1: "\\frac{2}{5}x^{7/5} + \\frac{3}{2}x^{5/2} + C", dist2: "\\frac{5}{7}x^{7/5} - \\frac{2}{5}x^{5/2} + C", dist3: "\\frac{7}{5}x^{2/5} + \\frac{5}{2}x^{3/2} + C" },
      { id: 45, title: "Problem 45", expr: "\\int \\frac{x^2 - 9}{x - 3} \\, dz", hint: "Factor numerator.", ans: "\\frac{1}{2}x^2 + 3x + C", dist1: "x + 3 + C", dist2: "\\frac{1}{2}x^2 - 3x + C", dist3: "x^2 + 3x + C" },
      { id: 46, title: "Problem 46", expr: "\\int (5\\sin x - 2e^x + \\frac{4}{x}) \\, dx", hint: "Term by term integration.", ans: "-5\\cos x - 2e^x + 4\\ln|x| + C", dist1: "5\\cos x - 2e^x + 4\\ln|x| + C", dist2: "-5\\sin x - 2e^x + 4\\ln|x| + C", dist3: "-5\\cos x + 2e^x + 4\\ln|x| + C" },
      { id: 47, title: "Problem 47", expr: "\\int (x^3 - 3x^2 + 3x - 1) \\, dx", hint: "Polynomial expansion.", ans: "\\frac{1}{4}x^4 - x^3 + \\frac{3}{2}x^2 - x + C", dist1: "\\frac{1}{3}x^4 - x^3 + \\frac{3}{2}x^2 - x + C", dist2: "\\frac{1}{4}x^4 - 3x^3 + 3x^2 - x + C", dist3: "3x^2 - 6x + 3 + C" },
      { id: 48, title: "Problem 48", expr: "\\int (10x^{-3} - x^{-1}) \\, dx", hint: "Power and reciprocal rules.", ans: "-\\frac{5}{x^2} - \\ln|x| + C", dist1: "\\frac{5}{x^2} - \\ln|x| + C", dist2: "-\\frac{10}{2x^2} - \\ln|x| + C", dist3: "-\\frac{5}{x^2} + \\ln|x| + C" },
      { id: 49, title: "Problem 49", expr: "\\int (6x^5 - 12x^3 + 2x) \\, dx", hint: "Polynomial power rule.", ans: "x^6 - 3x^4 + x^2 + C", dist1: "30x^4 - 36x^2 + 2 + C", dist2: "x^6 - 4x^4 + x^2 + C", dist3: "\\frac{6}{5}x^6 - 3x^4 + x^2 + C" },
      { id: 50, title: "Problem 50", expr: "\\int (e^{2x} + \\cos(2x)) \\, dx", hint: "Linear substitution rules.", ans: "\\frac{1}{2}e^{2x} + \\frac{1}{2}\\sin(2x) + C", dist1: "e^{2x} - \\sin(2x) + C", dist2: "\\frac{1}{2}e^{2x} - \\frac{1}{2}\\sin(2x) + C", dist3: "2e^{2x} + 2\\sin(2x) + C" }
    ];

    const PROBLEMS_DATA = [];

    rawIntegrals.forEach(item => {
      const allOpts = [
        { text: `\\(${item.ans}\\)`, isCorrect: true },
        { text: `\\(${item.dist1}\\)`, isCorrect: false },
        { text: `\\(${item.dist2}\\)`, isCorrect: false },
        { text: `\\(${item.dist3}\\)`, isCorrect: false }
      ];

      // Deterministic mix based on item.id so correct answer is distributed across 0, 1, 2, 3 (A, B, C, D)
      const correctPos = (item.id * 3) % 4;
      const correctObj = allOpts[0];
      const distObjs = [allOpts[1], allOpts[2], allOpts[3]];

      const finalOpts = [];
      let distIdx = 0;
      for (let i = 0; i < 4; i++) {
        if (i === correctPos) {
          finalOpts.push({ label: String.fromCharCode(65 + i), text: correctObj.text });
        } else {
          finalOpts.push({ label: String.fromCharCode(65 + i), text: distObjs[distIdx++].text });
        }
      }

      PROBLEMS_DATA.push({
        id: item.id,
        title: item.title,
        prompt: `Evaluate the indefinite integral: \\[${item.expr}\\]`,
        hint: item.hint,
        steps: [
          {
            title: "Step 1: Compute Indefinite Integral",
            prompt: `Evaluate \\(${item.expr}\\).`,
            options: finalOpts,
            correctIndex: correctPos,
            explanation: `Integrating the expression yields \\(${item.ans}\\).`
          }
        ]
      });
    });

    /* ==========================================================================
       PERSISTENCE & STATE MANAGEMENT ENGINE
       ========================================================================== */
    const STORAGE_KEY = "brain_mind_academy_calculus_integrals_50_v3";

    let currentStudentName = "Guest";
    let activeProblemId = 1;
    let stepProgress = {};

    let audioMuted = false;
    let totalSeconds = 0;
    let timerInterval = null;

    function saveSessionProgress() {
      try {
        const payload = {
          studentName: currentStudentName,
          activeProblemId: activeProblemId,
          totalSeconds: totalSeconds,
          stepProgress: stepProgress
        };
        localStorage.setItem(STORAGE_KEY, JSON.stringify(payload));
      } catch (e) {
        console.warn("Storage save error", e);
      }
    }

    function checkSavedSession() {
      try {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (!raw) return;
        const data = JSON.parse(raw);
        if (data && data.studentName) {
          const alertBox = document.getElementById('resumeAlertBox');
          const detailsSpan = document.getElementById('savedSessionDetails');
          const resumeBtn = document.getElementById('resumeSessionBtn');
          const startBtn = document.getElementById('startSessionBtn');
          const input = document.getElementById('studentNameInput');

          input.value = data.studentName;
          let completedSteps = 0;
          Object.keys(data.stepProgress || {}).forEach(k => {
            if (data.stepProgress[k].resolved) completedSteps++;
          });
          detailsSpan.innerText = `Student: ${data.studentName} • ${completedSteps} Steps Completed • Time: ${Math.floor(data.totalSeconds / 60)}m ${data.totalSeconds % 60}s`;
          alertBox.style.display = 'block';
          resumeBtn.style.display = 'inline-block';
          startBtn.innerText = 'Start Fresh Session';
        }
      } catch (e) {
        console.warn("Session check error", e);
      }
    }

    const AudioEngine = {
      ctx: null,
      init() {
        if (!this.ctx) {
          this.ctx = new (window.AudioContext || window.webkitAudioContext)();
        }
      },
      playTone(freq, type, duration, delay = 0) {
        if (audioMuted || !this.ctx) return;
        setTimeout(() => {
          try {
            const osc = this.ctx.createOscillator();
            const gain = this.ctx.createGain();
            osc.type = type;
            osc.frequency.setValueAtTime(freq, this.ctx.currentTime);
            gain.gain.setValueAtTime(0.12, this.ctx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.0001, this.ctx.currentTime + duration);
            osc.connect(gain);
            gain.connect(this.ctx.destination);
            osc.start();
            osc.stop(this.ctx.currentTime + duration);
          } catch (e) {
            console.warn(e);
          }
        }, delay * 1000);
      },
      correct() {
        this.init();
        this.playTone(659.25, 'sine', 0.15, 0);
        this.playTone(880.00, 'sine', 0.25, 0.12);
      },
      incorrect() {
        this.init();
        this.playTone(196.00, 'triangle', 0.2, 0);
        this.playTone(146.83, 'triangle', 0.3, 0.12);
      }
    };

    function startTimer() {
      if (timerInterval) clearInterval(timerInterval);
      timerInterval = setInterval(() => {
        totalSeconds++;
        const mins = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
        const secs = String(totalSeconds % 60).padStart(2, '0');
        document.getElementById('timerChip').innerText = `⏱️ ${mins}:${secs}`;
        saveSessionProgress();
      }, 1000);
    }

    function showToast(msg) {
      const t = document.getElementById('toastMessage');
      t.innerText = msg;
      t.style.display = 'block';
      setTimeout(() => { t.style.display = 'none'; }, 2600);
    }

    function initDirectLogin(isResume = false) {
      const nameInput = document.getElementById('studentNameInput').value.trim() || 'Student';
      
      if (isResume) {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (raw) {
          const data = JSON.parse(raw);
          currentStudentName = data.studentName || nameInput;
          activeProblemId = data.activeProblemId || 1;
          totalSeconds = data.totalSeconds || 0;
          stepProgress = data.stepProgress || {};
          showToast(`Welcome back, ${currentStudentName}!`);
        }
      } else {
        currentStudentName = nameInput;
        totalSeconds = 0;
        activeProblemId = 1;
        stepProgress = {};
        saveSessionProgress();
      }

      document.getElementById('userPill').innerHTML = `<strong>Student: ${currentStudentName}</strong>`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Student: ${currentStudentName}</strong>`;
      document.getElementById('loginGateView').style.display = 'none';
      
      AudioEngine.init();
      startTimer();
      renderPalette();
      loadProblem(activeProblemId);
    }

    function resetStudentProgress() {
      if (confirm("Reset all 50 problem attempts and scorecard progress?")) {
        localStorage.removeItem(STORAGE_KEY);
        location.reload();
      }
    }

    function switchMainTab(tab) {
      document.getElementById('tabTheoryBtn').classList.toggle('active', tab === 'theory');
      document.getElementById('tabPracticeBtn').classList.toggle('active', tab === 'practice');
      document.getElementById('tabScorecardBtn').classList.toggle('active', tab === 'scorecard');

      document.getElementById('viewTheory').classList.toggle('active', tab === 'theory');
      document.getElementById('viewPractice').classList.toggle('active', tab === 'practice');
      document.getElementById('viewScorecard').classList.toggle('active', tab === 'scorecard');

      if (tab === 'scorecard') {
        renderScorecard();
      } else if (tab === 'practice') {
        renderPalette();
        loadProblem(activeProblemId);
      }

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function toggleHint(pId) {
      const hintBox = document.getElementById(`hintBox_${pId}`);
      if (hintBox) {
        const isHidden = hintBox.style.display === 'none' || hintBox.style.display === '';
        hintBox.style.display = isHidden ? 'block' : 'none';
      }
    }

    function insertSymbol(symbol) {
      showToast(`Inserted symbol: ${symbol}`);
    }

    function renderPalette() {
      const grid = document.getElementById('paletteGrid');
      grid.innerHTML = '';

      let completedProblems = 0;

      PROBLEMS_DATA.forEach((prob) => {
        let allResolved = true;
        let anyResolved = false;

        prob.steps.forEach((_, sIdx) => {
          const key = `${prob.id}_${sIdx}`;
          const sp = stepProgress[key];
          if (sp && sp.resolved) anyResolved = true;
          else allResolved = false;
        });

        if (allResolved) completedProblems++;

        const btn = document.createElement('button');
        let stateClass = '';
        if (prob.id === activeProblemId) stateClass = 'active';
        else if (allResolved) stateClass = 'completed';
        else if (anyResolved) stateClass = 'partial';

        btn.className = `palette-btn ${stateClass}`;
        btn.innerHTML = `<span>${prob.id}</span>`;
        btn.title = `Problem ${prob.id}: ${prob.title}`;
        btn.onclick = () => loadProblem(prob.id);
        grid.appendChild(btn);
      });

      document.getElementById('paletteCount').innerText = `${completedProblems} / ${PROBLEMS_DATA.length} Solved`;
    }

    function loadProblem(pId) {
      activeProblemId = pId;
      saveSessionProgress();
      renderPalette();

      const prob = PROBLEMS_DATA.find(p => p.id === pId);
      const card = document.getElementById('activeQuestionCard');

      let stepsHtml = '';

      prob.steps.forEach((step, sIdx) => {
        const key = `${prob.id}_${sIdx}`;
        const sp = stepProgress[key] || { attempts: 0, selectedIndex: null, resolved: false, correct: false };

        let canShow = sIdx === 0;
        if (sIdx > 0) {
          const prevKey = `${prob.id}_${sIdx - 1}`;
          const prevSp = stepProgress[prevKey];
          if (prevSp && prevSp.resolved) canShow = true;
        }

        if (!canShow) return;

        let optionsHtml = '';
        step.options.forEach((opt, optIdx) => {
          let optClass = '';
          if (sp.resolved) {
            if (optIdx === step.correctIndex) {
              optClass = 'selected-correct';
            } else if (sp.selectedIndex === optIdx) {
              optClass = 'selected-wrong';
            }
          }

          optionsHtml += `
            <button class="mcq-option-btn ${optClass}" 
              onclick="handleStepSelect(${prob.id}, ${sIdx}, ${optIdx})"
              ${sp.resolved ? 'disabled' : ''}>
              <span class="opt-letter">(${opt.label})</span>
              <span class="opt-text-content">${opt.text}</span>
            </button>
          `;
        });

        let feedbackHtml = '';
        if (sp.resolved) {
          feedbackHtml = `
            <div class="step-feedback-box ${sp.correct ? 'correct' : 'incorrect'}">
              <strong>${sp.correct ? '✓ Step Completed' : '✗ Solution Revealed'}</strong> (Correct Choice: Option ${step.options[step.correctIndex].label})<br/>
              <div style="margin-top: 6px;">${step.explanation}</div>
            </div>
          `;
        }

        stepsHtml += `
          <div class="step-unit ${sp.resolved ? 'completed' : ''}">
            <div class="step-header">
              <div class="step-title">
                <span>${step.title}</span>
                ${sp.resolved ? '<span class="step-badge resolved">Finished</span>' : `<span class="step-badge">Active Step</span>`}
              </div>
              <span class="attempts-badge">Attempts: ${sp.attempts}/2</span>
            </div>
            <div style="font-size: 0.95rem; line-height: 1.6; margin-bottom: 10px;">${step.prompt}</div>
            <div class="mcq-container">${optionsHtml}</div>
            
            <!-- Virtual Input Keyboard -->
            <div class="virtual-keyboard">
              <button class="vk-btn" onclick="insertSymbol('+')">+</button>
              <button class="vk-btn" onclick="insertSymbol('-')">-</button>
              <button class="vk-btn" onclick="insertSymbol('\\int')">∫</button>
              <button class="vk-btn" onclick="insertSymbol('C')">C</button>
              <button class="vk-btn" onclick="insertSymbol('dx')">dx</button>
              <button class="vk-btn" onclick="insertSymbol('ln')">ln</button>
            </div>

            ${!sp.resolved && sp.attempts >= 2 ? `
              <button class="btn-reveal-step" onclick="revealStepSolution(${prob.id},${sIdx})">
                Reveal Step Solution &amp; Continue
              </button>
            ` : ''}

            ${feedbackHtml}
          </div>
        `;
      });

      const pIdx = PROBLEMS_DATA.findIndex(p => p.id === prob.id);
      const prevDisabled = pIdx === 0 ? 'disabled' : '';
      const nextDisabled = pIdx === PROBLEMS_DATA.length - 1 ? 'disabled' : '';

      card.innerHTML = `
        <div style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap;">
          <span class="concept-tag">Brain and Mind Academy</span>
          <span style="font-size:0.82rem; color:var(--text-muted);">Calculus I: Indefinite Integrals</span>
        </div>
        
        <h2 style="color:var(--navy-dark); margin: 6px 0 10px 0;">Problem ${prob.id}: ${prob.title}</h2>
        <div style="margin-top: 8px; line-height: 1.65; font-size:1.02rem;">${prob.prompt}</div>
        
        <div class="hint-container">
          <button class="btn-hint-toggle" onclick="toggleHint(${prob.id})">
            💡 Need a Hint? Click to View / Hide
          </button>
          <div class="hint-box" id="hintBox_${prob.id}">
            <strong>Pedagogical Hint:</strong> ${prob.hint}
          </div>
        </div>

        ${prob.svg ? `<div class="svg-container">${prob.svg}</div>` : ''}
        
        <div style="margin-top: 18px;">${stepsHtml}</div>

        <div class="nav-toolbar">
          <button class="btn-nav-action" onclick="navigateProblem(-1)" ${prevDisabled}>
            ⏮ Previous Problem
          </button>
          <div class="nav-btn-group">
            <button class="btn-nav-action btn-skip" onclick="skipProblem(${prob.id})">
              ⏭ Skip
            </button>
            <button class="btn-nav-action" onclick="navigateProblem(1)" ${nextDisabled}>
              Next Problem ❯
            </button>
          </div>
        </div>
      `;

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function handleStepSelect(pId, sIdx, optIdx) {
      const prob = PROBLEMS_DATA.find(p => p.id === pId);
      const step = prob.steps[sIdx];
      const key = `${pId}_${sIdx}`;

      if (!stepProgress[key]) {
        stepProgress[key] = { attempts: 0, selectedIndex: null, resolved: false, correct: false };
      }
      const sp = stepProgress[key];
      if (sp.resolved) return;

      sp.selectedIndex = optIdx;
      sp.attempts++;

      if (optIdx === step.correctIndex) {
        sp.resolved = true;
        sp.correct = true;
        AudioEngine.correct();
        showToast(`Step ${sIdx + 1} Completed! Next step unlocked.`);
      } else {
        AudioEngine.incorrect();
        if (sp.attempts >= 2) {
          showToast(`2 attempts reached. Click 'Reveal Step Solution' to unlock next step.`);
        } else {
          showToast(`Incorrect option. 1 attempt remaining!`);
        }
      }

      saveSessionProgress();
      renderPalette();
      loadProblem(pId);
    }

    function revealStepSolution(pId, sIdx) {
      const key = `${pId}_${sIdx}`;
      if (!stepProgress[key]) {
        stepProgress[key] = { attempts: 2, selectedIndex: null, resolved: false, correct: false };
      }
      const sp = stepProgress[key];
      sp.resolved = true;
      sp.correct = false;
      AudioEngine.incorrect();
      showToast(`Step ${sIdx + 1} solution revealed. Next step unlocked.`);
      saveSessionProgress();
      renderPalette();
      loadProblem(pId);
    }

    function navigateProblem(delta) {
      const pIdx = PROBLEMS_DATA.findIndex(p => p.id === activeProblemId);
      const target = pIdx + delta;
      if (target >= 0 && target < PROBLEMS_DATA.length) {
        loadProblem(PROBLEMS_DATA[target].id);
      }
    }

    function skipProblem(pId) {
      showToast(`Problem ${pId} skipped.`);
      navigateProblem(1);
    }

    function renderScorecard() {
      const container = document.getElementById('completeSolutionsContainer');
      let fullySolvedProblems = 0;
      let totalSteps = 0;
      let correctSteps = 0;

      PROBLEMS_DATA.forEach(p => {
        let probComplete = true;
        p.steps.forEach((_, sIdx) => {
          totalSteps++;
          const key = `${p.id}_${sIdx}`;
          const sp = stepProgress[key];
          if (sp && sp.correct) {
            correctSteps++;
          } else {
            probComplete = false;
          }
        });
        if (probComplete) fullySolvedProblems++;
      });

      const percentage = Math.round((correctSteps / totalSteps) * 100);

      document.getElementById('scoreValue').innerText = `${fullySolvedProblems} / ${PROBLEMS_DATA.length}`;
      document.getElementById('progressBarFill').style.width = `${percentage}%`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Student: ${currentStudentName}</strong> (${correctSteps}/${totalSteps} Steps Correct • ${percentage}%)`;

      let html = '';
      PROBLEMS_DATA.forEach(prob => {
        let probStepsHtml = prob.steps.map((step, sIdx) => {
          const key = `${prob.id}_${sIdx}`;
          const sp = stepProgress[key] || { attempts: 0, selectedIndex: null, resolved: false, correct: false };
          
          let badge = `<span style="color:var(--text-muted); font-weight:bold;">Unattempted</span>`;
          if (sp.resolved) {
            badge = sp.correct 
              ? `<span style="color:var(--green-ok); font-weight:bold;">✓ Correct (Attempt ${sp.attempts})</span>` 
              : `<span style="color:var(--red-fail); font-weight:bold;">✗ Solution Revealed</span>`;
          }

          const userChoiceText = (sp.selectedIndex !== null && step.options[sp.selectedIndex]) 
            ? `(${step.options[sp.selectedIndex].label}) ${step.options[sp.selectedIndex].text}` 
            : 'None';

          return `
            <div style="background:#f8fafc; border-left:4px solid var(--brand-blue); padding:12px; margin-top:10px; border-radius:0 6px 6px 0;">
              <div style="display:flex; justify-content:space-between; margin-bottom:4px;">
                <strong>${step.title}</strong>
                ${badge}
              </div>
              <p style="font-size:0.9rem; margin-bottom:4px;"><strong>Target:</strong> ${step.prompt}</p>
              <p style="font-size:0.88rem;"><strong>Your Choice:</strong> ${userChoiceText}</p>
              <p style="font-size:0.88rem;"><strong>Correct Option:</strong> (${step.options[step.correctIndex].label}) ${step.options[step.correctIndex].text}</p>
              <p style="font-size:0.86rem; color:var(--text-muted); margin-top:4px;">${step.explanation}</p>
            </div>
          `;
        }).join('');

        html += `
          <div class="theory-card" style="margin-bottom:20px;">
            <div style="display:flex; justify-content:space-between; align-items:center;">
              <span class="concept-tag">Problem ${prob.id}</span>
              <span style="font-size:0.85rem; color:var(--text-muted);">Problem ${prob.id} of ${PROBLEMS_DATA.length}</span>
            </div>
            <h3 style="margin-top:6px;">${prob.title}</h3>
            <div style="margin: 8px 0; font-size:0.95rem;">${prob.prompt}</div>
            ${prob.svg ? `<div class="svg-container" style="max-width:320px; margin:12px 0;">${prob.svg}</div>` : ''}
            <div>${probStepsHtml}</div>
          </div>
        `;
      });

      container.innerHTML = html;
      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    document.getElementById('audioToggleBtn').onclick = () => {
      audioMuted = !audioMuted;
      document.getElementById('audioToggleBtn').innerText = audioMuted ? '🔇' : '🔊';
    };

    window.addEventListener('DOMContentLoaded', checkSavedSession);
  </script>
</body>
</html>
