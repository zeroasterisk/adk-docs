---
hide:
  - toc
  - navigation
---
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@splidejs/splide@4.1.4/dist/css/splide.min.css">
<script src="https://cdn.jsdelivr.net/npm/@splidejs/splide@4.1.4/dist/js/splide.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/asciinema-player@3.9.0/dist/bundle/asciinema-player.css" />
<script src="https://cdn.jsdelivr.net/npm/asciinema-player@3.9.0/dist/bundle/asciinema-player.min.js"></script>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<script>document.body.classList.add('adk-landing-page');</script>
<style>
  body.adk-landing-page { overflow-x: hidden !important; }
  body.adk-landing-page .md-grid { max-width: 100% !important; width: 100% !important; }
  body.adk-landing-page .md-sidebar { display: none !important; }
  body.adk-landing-page .md-main__inner { max-width: none !important; margin: 0 !important; padding: 0 !important; }
  body.adk-landing-page .md-content { max-width: none !important; margin: 0 !important; flex-grow: 1 !important; }
  body.adk-landing-page .md-content__inner { max-width: 1280px !important; margin: 0 auto !important; padding: 0 clamp(16px, 4vw, 48px) !important; box-sizing: border-box !important; overflow-x: hidden !important; }
  body.adk-landing-page .md-footer { display: none !important; }
  body.adk-landing-page .md-header__inner { max-width: 100% !important; overflow-x: hidden !important; padding-right: 20px !important; }
  /* Responsive header repo links — full text → icons only (≤1200px) → hidden (≤900px) */
  .md-header__title { flex-shrink: 1 !important; min-width: 120px !important; overflow: hidden !important; }
  .md-header__source { flex-shrink: 0 !important; display: flex !important; gap: 2px !important; flex-wrap: nowrap !important; max-width: none !important; width: auto !important; }
  body.adk-landing-page .md-header__inner { padding-right: 12px !important; }
  .md-header .md-source { min-width: auto !important; width: auto !important; margin-right: 2px !important; }
  .md-header .md-source__repository { font-size: 0.65rem; white-space: nowrap; }
  .md-header .md-source__icon svg { width: 1rem !important; height: 1rem !important; }
  @media (max-width: 1200px) {
    .md-header .md-source__repository { display: none !important; }
    .md-header .md-source { margin-right: 4px !important; position: relative; }
    .md-header .md-source::after {
      content: ''; display: inline-block; width: 16px; height: 16px;
      background-size: contain; background-repeat: no-repeat; background-position: center;
      position: absolute; right: 4px; top: 50%; transform: translateY(-50%);
    }
    .md-header .md-source { padding-right: 22px !important; min-width: 0 !important; width: auto !important; }
    .md-header .md-source[href*="adk-python"]::after { background-image: url('https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg'); }
    .md-header .md-source[href*="adk-js"]::after { background-image: url('https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg'); }
    .md-header .md-source[href*="adk-go"]::after { background-image: url('https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/go/go-original.svg'); }
    .md-header .md-source[href*="adk-java"]::after { background-image: url('https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg'); }
  }
  @media (max-width: 900px) {
    .md-header .md-source { display: none !important; }
  }
</style>

<div class="adk-landing">

<!-- Ambient Glows -->
<div class="glow glow-tl"></div>
<div class="glow glow-tr"></div>
<div class="glow glow-mr"></div>

<!-- Hero Section -->
<div class="hero-grid">
  <div class="hero-content">
    <h1>SOTA Production AI Agents, <span class="hero-dim">not Prototypes.</span></h1>
    <p>Start in seconds, stay in control while you hill climb, and scale up to enterprise-level deployments. Batteries included, any model, any tools, any deployment, opinionated but fully customizable, P0 Google code and <strong>fully open source</strong>.</p>
    <div class="hero-actions">
      <a href="get-started/quickstart/" class="btn btn-primary">Get Started</a>
    </div>
  </div>
  <div class="hero-visual">
    <!-- Tabbed Code Window -->
    <div class="tabbed-area" id="tabbed-area">
      <div class="mac-window">
        <div class="iterm-tab-bar">
          <div class="iterm-tab active" data-lang="python"><img class="lang-icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" alt="Python"> Python</div>
          <div class="iterm-tab" data-lang="go"><img class="lang-icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/go/go-original.svg" alt="Go"> Go</div>
          <div class="iterm-tab" data-lang="java"><img class="lang-icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/java/java-original.svg" alt="Java"> Java</div>
          <div class="iterm-tab" data-lang="typescript"><img class="lang-icon" src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg" alt="TypeScript"> TypeScript</div>
        </div>
        <div class="code-content" id="code-python"><pre><span class="kw">from</span> google.adk <span class="kw">import</span> <span class="fn">Agent</span>
<span class="kw">from</span> google.adk.tools <span class="kw">import</span> google_search

agent = <span class="fn">Agent</span>(
    name=<span class="str">"researcher"</span>,
    model=<span class="str">"gemini-2.5-flash"</span>,
    instruction=<span class="str">"You help users research topics thoroughly."</span>,
    tools=[google_search],
)</pre></div>
        <div class="code-content" id="code-go" style="display:none"><pre><span class="kw">import</span> <span class="str">"google.golang.org/adk/agent"</span>

a := agent.<span class="fn">New</span>(<span class="str">"researcher"</span>,
    agent.<span class="fn">WithModel</span>(<span class="str">"gemini-2.5-flash"</span>),
    agent.<span class="fn">WithInstruction</span>(<span class="str">"You help users research topics thoroughly."</span>),
    agent.<span class="fn">WithTools</span>(googleSearch),
)</pre></div>
        <div class="code-content" id="code-java" style="display:none"><pre><span class="kw">import</span> com.google.adk.agents.<span class="fn">LlmAgent</span>;
<span class="kw">import</span> com.google.adk.tools.<span class="fn">GoogleSearchTool</span>;

<span class="fn">LlmAgent</span> agent = <span class="fn">LlmAgent</span>.builder()
    .name(<span class="str">"researcher"</span>)
    .model(<span class="str">"gemini-2.5-flash"</span>)
    .instruction(<span class="str">"You help users research topics thoroughly."</span>)
    .tools(<span class="fn">GoogleSearchTool</span>.create())
    .build();</pre></div>
        <div class="code-content" id="code-typescript" style="display:none"><pre><span class="kw">import</span> { <span class="fn">Agent</span> } <span class="kw">from</span> <span class="str">'@google/adk'</span>;
<span class="kw">import</span> { googleSearch } <span class="kw">from</span> <span class="str">'@google/adk/tools'</span>;

<span class="kw">const</span> agent = <span class="kw">new</span> <span class="fn">Agent</span>({
  name: <span class="str">'researcher'</span>,
  model: <span class="str">'gemini-2.5-flash'</span>,
  instruction: <span class="str">'You help users research topics thoroughly.'</span>,
  tools: [googleSearch],
});</pre></div>
      </div>
      <!-- Install info synced with tabs -->
      <div class="install-info" id="install-python">
        <div class="install-cmd"><code>pip install google-adk</code></div>
        <div class="install-badges">
          <span class="badge badge-version">v1.26.0</span>
          <span class="badge badge-stars">⭐ 18,189</span>
          <span class="badge badge-downloads">📦 3.7M+/mo</span>
        </div>
        <a href="https://github.com/google/adk-python" class="github-link" target="_blank">
          <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
          adk-python
        </a>
      </div>
      <div class="install-info" id="install-go" style="display:none">
        <div class="install-cmd"><code>go get google.golang.org/adk</code></div>
        <div class="install-badges">
          <span class="badge badge-version">v0.5.0</span>
          <span class="badge badge-stars">⭐ 7,088</span>
        </div>
        <a href="https://github.com/google/adk-go" class="github-link" target="_blank">
          <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
          adk-go
        </a>
      </div>
      <div class="install-info" id="install-java" style="display:none">
        <div class="install-cmd"><code>com.google.adk:google-adk:0.2.0</code></div>
        <div class="install-badges">
          <span class="badge badge-version">v0.2.0</span>
          <span class="badge badge-stars">⭐ 1,327</span>
        </div>
        <a href="https://github.com/google/adk-java" class="github-link" target="_blank">
          <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
          adk-java
        </a>
      </div>
      <div class="install-info" id="install-typescript" style="display:none">
        <div class="install-cmd"><code>npm install @google/adk</code></div>
        <div class="install-badges">
          <span class="badge badge-version">v0.4.0</span>
          <span class="badge badge-stars">⭐ 868</span>
          <span class="badge badge-downloads">📦 95K+/mo</span>
        </div>
        <a href="https://github.com/google/adk-js" class="github-link" target="_blank">
          <svg viewBox="0 0 16 16"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
          adk-js
        </a>
      </div>
    </div>
  </div>
</div>

<!-- Developer Tools -->
<div class="feature-split">
  <div class="feature-text">
    <span class="feature-badge">Developer Tools</span>
    <h2>Build agents <i>with</i> agents.</h2>
    <p>ADK is designed to be written by both humans and AI. Hook up your favorite coding assistant to our MCP Server and let it generate robust, tool-bound agents in seconds.</p>
    <p>Define your skills, bind your tools, and let your IDE do the heavy lifting.</p>
  </div>
  <div class="feature-visual">
    <div id="asciinema-demo"></div>
  </div>
</div>

<!-- Dev UI Section -->
<div class="feature-split reverse">
  <div class="feature-text">
    <span class="feature-badge">Observability</span>
    <h2>Visual Debugging &amp; Tracing</h2>
    <p>Stop printing to stdout. ADK includes a powerful interactive web UI for testing, debugging, and tracing agent behavior locally.</p>
    <p>Inspect tool calls, modify context windows on the fly, and visualize multi-agent graph executions with zero configuration.</p>
  </div>
  <div class="feature-visual">
    <div class="ui-wrapper">
      <img src="assets/adk-web-dev-ui-chat.png" alt="ADK Web Dev UI" class="devui-img">
    </div>
  </div>
</div>

<!-- Eval Section -->
<div class="feature-split">
  <div class="feature-text">
    <span class="feature-badge">Built-in Evaluation</span>
    <h2>Go beyond vibes. Evaluate everything.</h2>
    <p>Testing agents is notoriously hard. ADK's built-in evaluation framework lets you systematically test not just the final text response, but the <strong>entire execution trajectory</strong>.</p>
    <p>Assert that specific tools were called, check the exact sequence of graph nodes, and ground outputs against real data.</p>
  </div>
  <div class="feature-visual">
    <div class="eval-grid">
      <div class="eval-card pass">
        <div class="eval-title"><span>test_weather_trajectory</span><span class="eval-status pass">✓ PASS</span></div>
        <div class="eval-desc">Verified tool sequence: [get_location → get_weather]</div>
      </div>
      <div class="eval-card pass">
        <div class="eval-title"><span>test_response_groundedness</span><span class="eval-status pass">✓ PASS</span></div>
        <div class="eval-desc">Response perfectly matches tool output constraints.</div>
      </div>
      <div class="eval-card fail">
        <div class="eval-title"><span>test_prm_safety_filter</span><span class="eval-status fail">✗ FAIL</span></div>
        <div class="eval-desc">Agent bypassed safety node in graph path.</div>
      </div>
      <div class="eval-card pass">
        <div class="eval-title"><span>test_latency_budget</span><span class="eval-status pass">✓ PASS</span></div>
        <div class="eval-desc">Execution completed in 842ms (Budget: 1500ms).</div>
      </div>
    </div>

    <!-- Metrics Chart -->
    <div class="metrics-dashboard">
      <div class="metrics-chart">
        <div class="metrics-chart-label">Agent v2.1 vs v2.0 — Response Quality</div>
        <svg viewBox="0 0 400 160" class="metrics-svg">
          <line x1="40" y1="20" x2="40" y2="130" stroke-width="1"/>
          <line x1="40" y1="130" x2="380" y2="130" stroke-width="1"/>
          <line x1="40" y1="75" x2="380" y2="75" stroke-width="0.5" stroke-dasharray="4"/>
          <line x1="40" y1="45" x2="380" y2="45" stroke-width="0.5" stroke-dasharray="4"/>
          <polyline points="40,95 90,93 140,96 190,94 240,95 290,93 340,94 380,95" fill="none" stroke="#6b7280" stroke-width="2" opacity="0.7"/>
          <polyline points="40,92 90,85 140,78 190,68 240,58 290,50 340,42 380,35" fill="none" stroke="#3b82f6" stroke-width="2.5"/>
          <polyline points="40,92 90,85 140,78 190,68 240,58 290,50 340,42 380,35 380,130 40,130" fill="url(#blueGrad)" opacity="0.15"/>
          <defs><linearGradient id="blueGrad" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#3b82f6"/><stop offset="100%" stop-color="transparent"/></linearGradient></defs>
          <text x="385" y="98" fill="#6b7280" font-size="10" font-family="Inter">v2.0</text>
          <text x="385" y="38" fill="#3b82f6" font-size="10" font-family="Inter">v2.1</text>
          <text x="40" y="148" fill="#71717a" font-size="9" font-family="Inter">Day 1</text>
          <text x="360" y="148" fill="#71717a" font-size="9" font-family="Inter">Day 7</text>
        </svg>
      </div>
      <div class="metrics-table-wrap">
        <table class="metrics-table">
          <thead><tr><th>Metric</th><th>v2.0</th><th>v2.1</th><th>Δ</th></tr></thead>
          <tbody>
            <tr class="metric-green"><td>Groundedness</td><td>76%</td><td>88%</td><td class="delta-green">+12%</td></tr>
            <tr class="metric-green"><td>Latency p50</td><td>620ms</td><td>440ms</td><td class="delta-green">−180ms</td></tr>
            <tr class="metric-green"><td>Tool accuracy</td><td>81%</td><td>89%</td><td class="delta-green">+8%</td></tr>
            <tr class="metric-neutral"><td>Safety filter</td><td>99.2%</td><td>99.2%</td><td class="delta-neutral">+0%</td></tr>
            <tr class="metric-red"><td>Hallucination rate</td><td>4.1%</td><td>6.1%</td><td class="delta-red">+2%</td></tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</div>

<!-- Low Floor, High Ceiling Section -->
<div class="ceiling-section">
  <h2>Low floor, high ceiling</h2>
  <p class="section-subtitle">Start simple. Scale to production. ADK grows with you.</p>
  <div id="features-carousel" class="splide" aria-label="Key features">
    <div class="splide__track">
      <ul class="splide__list">
        <li class="splide__slide">
          <a class="carousel-card" href="context/">
            <span class="card-icon">🧩</span>
            <h3>Structured Context</h3>
            <p>Compiled view of structured context lets agents reason about complex state without losing track.</p>
          </a>
        </li>
        <li class="splide__slide">
          <a class="carousel-card" href="callbacks/">
            <span class="card-icon">🔌</span>
            <h3>Callbacks &amp; Plugins</h3>
            <p>Callbacks change the behavior of ADK at every level — customize auth, logging, tool resolution, and more.</p>
          </a>
        </li>
        <li class="splide__slide">
          <a class="carousel-card" href="agents/workflow-agents/">
            <span class="card-icon">🔀</span>
            <h3>Graph Workflows</h3>
            <p>Need fine-grained control? Graph-based workflows give you deterministic execution paths with AI-powered nodes.</p>
          </a>
        </li>
        <li class="splide__slide">
          <a class="carousel-card" href="deploy/">
            <span class="card-icon">🏗️</span>
            <h3>Battle-tested at Scale</h3>
            <p>Google-backed with thousands of agents in production. This isn't a weekend project.</p>
          </a>
        </li>
        <li class="splide__slide">
          <a class="carousel-card" href="agents/models/">
            <span class="card-icon">🌐</span>
            <h3>Any Model, Any Runtime</h3>
            <p>Any model, any runtime, any tools, any interface. Zero lock-in by design.</p>
          </a>
        </li>
        <li class="splide__slide">
          <a class="carousel-card" href="deploy/agent-engine/">
            <span class="card-icon">💎</span>
            <h3>Built for Gemini &amp; Google Cloud</h3>
            <p>While model-agnostic, ADK is optimized for Gemini models and Google Cloud deployment with first-class integrations.</p>
          </a>
        </li>
      </ul>
    </div>
  </div>
</div>

</div>

<script>
// Tab switching logic
document.addEventListener("DOMContentLoaded", function() {
  var tabs = document.querySelectorAll('.iterm-tab');
  var langs = ['python', 'go', 'java', 'typescript'];

  tabs.forEach(function(tab) {
    tab.addEventListener('click', function() {
      var lang = this.getAttribute('data-lang');
      tabs.forEach(function(t) { t.classList.remove('active'); });
      this.classList.add('active');
      langs.forEach(function(l) {
        document.getElementById('code-' + l).style.display = l === lang ? 'block' : 'none';
        document.getElementById('install-' + l).style.display = l === lang ? 'flex' : 'none';
      });
    });
  });

  // Splide carousel
  if (typeof Splide !== 'undefined') {
    new Splide('#features-carousel', {
      type: 'loop',
      perPage: 3,
      perMove: 1,
      focus: 'center',
      gap: '1.25rem',
      padding: '2rem',
      autoplay: false,
      pagination: true,
      arrows: true,
      breakpoints: {
        1024: { perPage: 2, padding: '1rem' },
        640: { perPage: 1, padding: '2rem' }
      }
    }).mount();
  }

  // Asciinema player
  var playerEl = document.getElementById('asciinema-demo');
  if (playerEl && typeof AsciinemaPlayer !== 'undefined') {
    AsciinemaPlayer.create('assets/adk-demo.cast', playerEl, {
      theme: 'monokai',
      fit: 'width',
      autoPlay: true,
      loop: true,
      speed: 1,
      idleTimeLimit: 2,
      cols: 85,
      rows: 24,
      poster: 'npt:0:18'
    });
  }
});
</script>
