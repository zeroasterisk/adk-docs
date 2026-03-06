---
hide:
  - toc
  - navigation
---

<div class="landing-page">

  <!-- Hero Section -->
  <div class="lp-hero">
    <div class="lp-hero-content">
      <div class="lp-hero-logo">
        <img src="assets/agent-development-kit.png" alt="ADK Logo" width="80">
      </div>
      <h1 class="lp-hero-title">Agent Development Kit</h1>
      <p class="lp-hero-tagline">Start quickly, evolve your designs, and scale up to enterprise-level deployments.</p>
      <p class="lp-hero-description">
        ADK is a flexible, modular framework for developing and deploying AI agents.
        Model-agnostic. Deployment-agnostic. Open source.
      </p>
      <div class="lp-hero-actions">
        <a href="get-started/quickstart/" class="lp-btn lp-btn-primary">Get started</a>
        <a href="https://github.com/google/adk-python" class="lp-btn lp-btn-secondary" target="_blank">GitHub</a>
      </div>
    </div>
  </div>

  <!-- Install Section -->
  <div class="lp-install">
    <div class="lp-install-grid">
      <div class="lp-install-card">
        <div class="lp-install-lang">🐍 Python</div>
        <code>pip install google-adk</code>
      </div>
      <div class="lp-install-card">
        <div class="lp-install-lang">☕ Java</div>
        <code>com.google.adk:google-adk:0.6.0</code>
      </div>
      <div class="lp-install-card">
        <div class="lp-install-lang">🔷 TypeScript</div>
        <code>npm install @google/adk</code>
      </div>
      <div class="lp-install-card">
        <div class="lp-install-lang">🐹 Go</div>
        <code>go get google.golang.org/adk</code>
      </div>
    </div>
  </div>

  <!-- Open Source, Any Model -->
  <div class="lp-section">
    <h2 class="lp-section-title">Open source. Any model. Any cloud.</h2>
    <p class="lp-section-subtitle">
      Build your agents with AI models that work for you, and run them on the best infrastructure for your needs.
    </p>
    <div class="lp-features-grid">
      <div class="lp-feature-card">
        <div class="lp-feature-icon">🧠</div>
        <h3>Model-agnostic</h3>
        <p>Optimized for Gemini, but works with any LLM. Swap models without rewriting your agent logic.</p>
      </div>
      <div class="lp-feature-card">
        <div class="lp-feature-icon">☁️</div>
        <h3>Deployment-agnostic</h3>
        <p>Run locally, on Google Cloud, or any infrastructure. Your agents, your choice.</p>
      </div>
      <div class="lp-feature-card">
        <div class="lp-feature-icon">🔓</div>
        <h3>Open source</h3>
        <p>Apache 2.0 licensed. Full transparency, community-driven development, no lock-in.</p>
      </div>
      <div class="lp-feature-card">
        <div class="lp-feature-icon">🔗</div>
        <h3>Framework-compatible</h3>
        <p>Built for compatibility with LangChain, CrewAI, and other popular agent frameworks.</p>
      </div>
    </div>
  </div>

  <!-- Low Floor, High Ceiling -->
  <div class="lp-section lp-section-alt">
    <h2 class="lp-section-title">Low floor, high ceiling</h2>
    <p class="lp-section-subtitle">
      Start simple with prompt-based, single agents, and evolve into graph-based workflows with multiple, coordinated agents.
    </p>
    <div class="lp-progression">
      <div class="lp-progression-step">
        <div class="lp-progression-number">1</div>
        <h3>Single Agent</h3>
        <p>A prompt, a model, and tools. Get running in minutes.</p>
      </div>
      <div class="lp-progression-arrow">→</div>
      <div class="lp-progression-step">
        <div class="lp-progression-number">2</div>
        <h3>Multi-Agent</h3>
        <p>Compose agents that delegate to specialized sub-agents.</p>
      </div>
      <div class="lp-progression-arrow">→</div>
      <div class="lp-progression-step">
        <div class="lp-progression-number">3</div>
        <h3>Workflow Graphs</h3>
        <p>Deterministic control flow with AI-powered nodes.</p>
      </div>
    </div>
  </div>

  <!-- ADK 2.0 Workflow Graphs -->
  <div class="lp-section">
    <h2 class="lp-section-title">✨ New in ADK 2.0: Workflow Graphs</h2>
    <p class="lp-section-subtitle">
      Define agents with language and logic. Graph-based agents let you combine AI-powered functionality with deterministic code for more reliable workflows.
    </p>
    <div class="lp-code-comparison">
      <div class="lp-code-block">
        <div class="lp-code-label">Simple Agent</div>

```python
from google.adk import Agent

agent = Agent(
    name="greeter",
    model="gemini-2.0-flash",
    instruction="You are a friendly greeter.",
    tools=[get_weather],
)
```

</div>
      <div class="lp-code-block">
        <div class="lp-code-label">Graph-based Workflow</div>

```python
from google.adk import Agent, GraphAgent

researcher = Agent(name="researcher", ...)
writer = Agent(name="writer", ...)

workflow = GraphAgent(name="pipeline")
workflow.add_node(researcher)
workflow.add_node(writer)
workflow.add_edge("researcher", "writer")
```

</div>
    </div>
  </div>

  <!-- Ecosystem -->
  <div class="lp-section lp-section-alt">
    <h2 class="lp-section-title">Rich ecosystem &amp; Google Cloud ready</h2>
    <p class="lp-section-subtitle">
      Take advantage of numerous pre-built integrations from Google and our partners to build fast, and scale up your deployments to enterprise scale with full support from Google Agent Platform.
    </p>
    <div class="lp-ecosystem-grid">
      <div class="lp-ecosystem-card">
        <h3>🔧 Built-in Tools</h3>
        <p>Google Search, Code Execution, Vertex AI extensions, and more out of the box.</p>
      </div>
      <div class="lp-ecosystem-card">
        <h3>🔌 MCP Support</h3>
        <p>Connect to any Model Context Protocol server for extensible tool access.</p>
      </div>
      <div class="lp-ecosystem-card">
        <h3>🤝 A2A Protocol</h3>
        <p>Agent-to-Agent communication for cross-platform agent interoperability.</p>
      </div>
      <div class="lp-ecosystem-card">
        <h3>🚀 Agent Engine</h3>
        <p>Deploy to Google Cloud's managed Agent Engine for production-grade scaling.</p>
      </div>
      <div class="lp-ecosystem-card">
        <h3>📊 Evaluation</h3>
        <p>Built-in eval framework to test and iterate on your agents systematically.</p>
      </div>
      <div class="lp-ecosystem-card">
        <h3>🖥️ Dev UI</h3>
        <p>Interactive web UI for testing, debugging, and tracing agent behavior locally.</p>
      </div>
    </div>
  </div>

  <!-- Community -->
  <div class="lp-section">
    <h2 class="lp-section-title">Join the community</h2>
    <p class="lp-section-subtitle">ADK is open source and growing fast.</p>
    <div class="lp-community-links">
      <a href="https://github.com/google/adk-python" class="lp-community-card" target="_blank">
        <h3>ADK Python</h3>
        <p>Core Python SDK</p>
      </a>
      <a href="https://github.com/google/adk-typescript" class="lp-community-card" target="_blank">
        <h3>ADK TypeScript</h3>
        <p>TypeScript/JavaScript SDK</p>
      </a>
      <a href="https://github.com/google/adk-java" class="lp-community-card" target="_blank">
        <h3>ADK Java</h3>
        <p>Java SDK</p>
      </a>
      <a href="https://github.com/google/adk-go" class="lp-community-card" target="_blank">
        <h3>ADK Go</h3>
        <p>Go SDK</p>
      </a>
      <a href="https://github.com/google/adk-docs" class="lp-community-card" target="_blank">
        <h3>Documentation</h3>
        <p>Contribute to these docs</p>
      </a>
      <a href="community/" class="lp-community-card">
        <h3>Community</h3>
        <p>Resources, videos &amp; more</p>
      </a>
    </div>
  </div>

  <!-- Quick Links -->
  <div class="lp-section lp-section-alt lp-quicklinks">
    <div class="lp-quicklinks-grid">
      <a href="get-started/quickstart/" class="lp-quicklink">
        <strong>📖 Quickstart</strong>
        <span>Build your first agent</span>
      </a>
      <a href="agents/" class="lp-quicklink">
        <strong>🏗️ Agents</strong>
        <span>Agent types &amp; patterns</span>
      </a>
      <a href="tools/" class="lp-quicklink">
        <strong>🔧 Tools</strong>
        <span>Tool catalog &amp; usage</span>
      </a>
      <a href="deploy/" class="lp-quicklink">
        <strong>🚀 Deploy</strong>
        <span>Production deployment</span>
      </a>
    </div>
  </div>

</div>
