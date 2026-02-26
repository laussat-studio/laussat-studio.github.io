<script setup lang="ts">
const year = new Date().getFullYear()
</script>

<template>
  <main class="root">
    <header class="header">
      <div class="brand">laussat.studio</div>
      <nav class="nav">
        <a href="#work">Work</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
        <a href="/documentation/index/">Docs</a>
      </nav>
    </header>

    <section class="hero">
      <h1>Laussat Studio</h1>
      <p>Design + engineering. A small studio building calm, precise software.</p>
      <div class="cta">
        <a class="btn" href="#contact">Get in touch</a>
        <a class="btn secondary" href="/documentation/index/">Documentation</a>
      </div>
    </section>

    <section id="work" class="section">
      <h2>Work</h2>
      <p>We build and ship product—fast, clean, and maintainable.</p>
      <div class="grid">
        <div class="card">
          <h3>Web</h3>
          <p>Landing pages, apps, and systems that feel premium.</p>
        </div>
        <div class="card">
          <h3>iOS/macOS</h3>
          <p>Native experiences with thoughtful UX and performance.</p>
        </div>
        <div class="card">
          <h3>Infra</h3>
          <p>Deploy pipelines and automation you can trust.</p>
        </div>
      </div>
    </section>

    <section id="about" class="section">
      <h2>About</h2>
      <p>Laussat Studio is a small team focused on craft. We care about typography, speed, and systems.</p>
    </section>

    <section id="contact" class="section">
      <h2>Contact</h2>
      <p>Email: <a href="mailto:hello@laussat.studio">hello@laussat.studio</a></p>
    </section>

    <footer class="footer">
      <span>© {{ year }} laussat.studio</span>
    </footer>
  </main>
</template>

<style>
:root{
  --bg: #07080a;
  --fg: #eef2ff;
  --muted:#a2a9bd;
  --accent:#8b5cf6;
  --card:#0d1017;
  --border: rgba(255,255,255,0.10);
}
*{box-sizing:border-box}
html,body{height:100%}
body{margin:0;background:radial-gradient(1200px 800px at 50% 10%, rgba(139,92,246,0.18), transparent 60%), var(--bg); color:var(--fg);
  font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial;
}
a{color:inherit}
.root{min-height:100vh;max-width:1060px;margin:0 auto;padding:34px 22px}
.header{display:flex;align-items:center;justify-content:space-between;gap:18px;position:sticky;top:0;padding:14px 18px;border:1px solid var(--border);border-radius:14px;background:rgba(7,8,10,0.6);backdrop-filter: blur(10px)}
.brand{letter-spacing:0.06em;font-weight:600}
.nav{display:flex;gap:14px;flex-wrap:wrap}
.nav a{color:var(--muted);text-decoration:none}
.nav a:hover{color:var(--fg)}
.hero{padding:56px 18px 26px}
.hero h1{margin:0 0 12px 0;font-size:46px;letter-spacing:-0.02em}
.hero p{margin:0;color:var(--muted);font-size:18px;max-width:68ch}
.cta{display:flex;gap:12px;margin-top:22px;flex-wrap:wrap}
.btn{display:inline-flex;align-items:center;justify-content:center;padding:10px 14px;border-radius:12px;border:1px solid var(--border);text-decoration:none;background:linear-gradient(180deg, rgba(139,92,246,0.35), rgba(139,92,246,0.12))}
.btn.secondary{background:rgba(255,255,255,0.04)}
.section{padding:26px 18px}
.section h2{margin:0 0 10px 0;letter-spacing:-0.01em}
.section p{margin:0;color:var(--muted)}
.grid{display:grid;grid-template-columns:repeat(3, minmax(0, 1fr));gap:14px;margin-top:16px}
.card{padding:16px;border:1px solid var(--border);border-radius:14px;background:var(--card)}
.card h3{margin:0 0 6px 0}
.card p{margin:0;color:var(--muted)}
.footer{padding:28px 18px;color:rgba(162,169,189,0.8);text-align:center}
@media (max-width: 820px){
  .grid{grid-template-columns:1fr}
  .hero h1{font-size:38px}
}
</style>
