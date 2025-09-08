# --- Build a simple personal website and run it locally ---
set -e

# 1) Make project folder
SITE_DIR="nd-esteem-portfolio"
mkdir -p "$SITE_DIR"/assets
cd "$SITE_DIR"

# 2) HTML
cat > index.html <<'EOF'
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mo Mo — Notre Dame ESTEEM</title>
  <meta name="description" content="Notre Dame ESTEEM student with a heavy startup background who loves pickleball and soccer." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><rect width=%22100%22 height=%22100%22 rx=%2215%22 fill=%22%230C2340%22/><text x=%2250%25%22 y=%2257%25%22 text-anchor=%22middle%22 font-size=%2270%22 fill=%22%23AE9142%22 font-family=%22Georgia,serif%22>ND</text></svg>">
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="nav">
    <a class="brand" href="#top">Mo Mo</a>
    <nav>
      <a href="#about">About</a>
      <a href="#experience">Startups</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
      <button id="themeToggle" aria-label="Toggle theme">☾</button>
    </nav>
  </header>

  <main id="top">
    <section class="hero">
      <div class="badge">Notre Dame • ESTEEM</div>
      <h1>Builder at heart. <span class="accent">Startup-savvy.</span><br />Pickleball &amp; soccer enthusiast.</h1>
      <p class="lead">
        I’m a student in Notre Dame’s ESTEEM program with a heavy background in startups.
        I love turning messy problems into crisp products—and when I’m not iterating,
        you’ll find me on a pickleball court or a soccer pitch.
      </p>
      <div class="cta">
        <a class="btn primary" href="#projects">See Projects</a>
        <a class="btn ghost" href="#contact">Get in Touch</a>
      </div>
      <div class="hero-art" aria-hidden="true">
        <!-- Simple inline SVG flair: a ball + paddle + soccer ball -->
        <svg viewBox="0 0 360 160" width="100%" height="100%" role="img">
          <!-- Paddle -->
          <rect x="20" y="45" rx="14" ry="14" width="120" height="80" class="paddle"/>
          <rect x="135" y="78" width="30" height="14" class="handle"/>
          <!-- Pickleball -->
          <circle cx="210" cy="85" r="22" class="pickleball"/>
          <circle cx="210" cy="85" r="4" class="hole"/><circle cx="194" cy="77" r="4" class="hole"/>
          <circle cx="226" cy="93" r="4" class="hole"/><circle cx="224" cy="73" r="4" class="hole"/>
          <circle cx="198" cy="96" r="4" class="hole"/><circle cx="217" cy="104" r="4" class="hole"/>
          <!-- Soccer ball (hex pattern simplified) -->
          <circle cx="300" cy="90" r="28" class="soccer"/>
          <polygon points="300,72 313,80 308,96 292,96 287,80" class="soccer-cell"/>
          <polygon points="300,108 313,100 308,84 292,84 287,100" class="soccer-cell"/>
        </svg>
      </div>
    </section>

    <section id="about" class="section">
      <h2>About</h2>
      <p>
        I’m currently at <strong>Notre Dame</strong> in the <strong>ESTEEM</strong> program,
        focusing on venture creation and applied innovation. My background spans
        <em>early-stage startups</em>, hands-on product building, and data-driven
        experimentation. I thrive at the intersection of customer insight,
        rapid prototyping, and go-to-market.
      </p>
      <ul class="grid two">
        <li>
          <h3>Strengths</h3>
          <p>Zero-to-one product work, user discovery, scrappy analytics, pitch craft, and shipping.</p>
        </li>
        <li>
          <h3>On the side</h3>
          <p>Pickleball (doubles addict), weekend soccer games, and tinkering with AI tools to speed up ops.</p>
        </li>
      </ul>
    </section>

    <section id="experience" class="section">
      <h2>Startup Experience</h2>
      <div class="cards">
        <article class="card">
          <h3>Operator & Builder</h3>
          <p>Led experiments across marketing, onboarding, and pricing. Built lightweight tools and dashboards to unlock growth.</p>
          <span class="tag">0→1</span><span class="tag">Experiments</span><span class="tag">GTM</span>
        </article>
        <article class="card">
          <h3>Product Prototyper</h3>
          <p>Shipped MVPs in days, not months—using customer interviews, Figma, and code where it counts.</p>
          <span class="tag">MVP</span><span class="tag">UX</span><span class="tag">Scrappy</span>
        </article>
        <article class="card">
          <h3>Ops + AI</h3>
          <p>Automated repetitive workflows, set up data plumbing, and piloted AI-assisted processes.</p>
          <span class="tag">Automation</span><span class="tag">AI</span><span class="tag">Ops</span>
        </article>
      </div>
    </section>

    <section id="projects" class="section">
      <h2>Projects</h2>
      <div class="grid three">
        <article class="tile">
          <h3>Interview Engine</h3>
          <p>Lightweight system to turn qualitative interviews into structured insights and prioritized roadmaps.</p>
          <a class="link" href="#" aria-disabled="true">Case study (coming soon)</a>
        </article>
        <article class="tile">
          <h3>Ops Autopilot</h3>
          <p>AI-assisted invoicing + inventory checks that cut errors and saved hours per week.</p>
          <a class="link" href="#" aria-disabled="true">Before/After (coming soon)</a>
        </article>
        <article class="tile">
          <h3>Rec Sports Tracker</h3>
          <p>Pickleball &amp; soccer stat tracker for friendly rivalries. Built for fun, kept for motivation.</p>
          <a class="link" href="#" aria-disabled="true">Demo (coming soon)</a>
        </article>
      </div>
    </section>

    <section id="contact" class="section">
      <h2>Contact</h2>
      <p>Have a project, a startup idea, or a scrappy experiment in mind? I’d love to connect.</p>
      <div class="cta">
        <a class="btn primary" href="mailto:hello@example.com">Email Me</a>
        <a class="btn ghost" href="https://www.linkedin.com/" target="_blank" rel="noopener">LinkedIn</a>
      </div>
    </section>
  </main>

  <footer class="footer">
    <p>© <span id="year"></span> Mo Mo • Built with love at Notre Dame.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
EOF

# 3) CSS
cat > styles.css <<'EOF'
:root{
  --nd-navy:#0C2340;
  --nd-gold:#AE9142;
  --ink:#111827;
  --paper:#FFFFFF;
  --muted:#6B7280;
  --card:#F9FAFB;
  --ring:rgba(12,35,64,.15);
}
:root[data-theme="dark"]{
  --paper:#0B1020;
  --ink:#E5E7EB;
  --muted:#9CA3AF;
  --card:#121a2c;
  --ring:rgba(174,145,66,.25);
}
*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
  color:var(--ink);
  background:var(--paper);
  line-height:1.6;
}

/* Nav */
.nav{
  position:sticky; top:0; z-index:50;
  display:flex; justify-content:space-between; align-items:center;
  padding:14px 20px;
  background:linear-gradient(to bottom, rgba(255,255,255,.85), rgba(255,255,255,.6));
  backdrop-filter:saturate(180%) blur(12px);
  border-bottom:1px solid var(--ring);
}
:root[data-theme="dark"] .nav{
  background:linear-gradient(to bottom, rgba(11,16,32,.85), rgba(11,16,32,.6));
}
.nav a{text-decoration:none; color:var(--ink); margin:0 10px; font-weight:600}
.nav .brand{color:var(--nd-navy)}
.nav #themeToggle{
  margin-left:10px; border:1px solid var(--ring); background:transparent; color:var(--ink);
  padding:8px 10px; border-radius:10px; cursor:pointer;
}

/* Hero */
.hero{
  padding:72px 20px 20px; max-width:1100px; margin:0 auto;
  display:grid; gap:24px; grid-template-columns:1.2fr .8fr; align-items:center;
}
.badge{
  display:inline-block; background:var(--nd-navy); color:white; padding:6px 10px; border-radius:999px; font-size:12px;
}
.hero h1{font-size:40px; line-height:1.2; margin:12px 0 6px}
@media (min-width:900px){ .hero h1{font-size:56px} }
.lead{font-size:18px; color:var(--muted); max-width:65ch}
.accent{color:var(--nd-gold)}
.cta{display:flex; gap:12px; margin-top:12px}
.btn{
  display:inline-block; padding:12px 18px; border-radius:12px; text-decoration:none; font-weight:700; border:1px solid var(--ring)
}
.btn.primary{background:var(--nd-gold); color:#112; border-color:transparent}
.btn.ghost{background:transparent; color:var(--ink)}
.btn:hover{transform:translateY(-1px)}
.hero-art{width:100%; height:160px}
.paddle{fill:#AE9142; opacity:.9}
.handle{fill:#8c7536}
.pickleball{fill:#ffd34d}
.hole{fill:#e0b800}
.soccer{fill:#ffffff; stroke:#0C2340; stroke-width:3}
.soccer-cell{fill:#0C2340}

/* Sections */
.section{padding:48px 20px; max-width:1100px; margin:0 auto}
.section h2{font-size:28px; margin:0 0 16px}
.grid{display:grid; gap:16px}
.grid.two{grid-template-columns:1fr}
.grid.three{grid-template-columns:1fr}
@media (min-width:800px){
  .grid.two{grid-template-columns:1fr 1fr}
  .grid.three{grid-template-columns:repeat(3,1fr)}
}
.cards{display:grid; gap:16px; grid-template-columns:1fr; }
@media (min-width:900px){ .cards{grid-template-columns:repeat(3,1fr)} }
.card, .tile{
  background:var(--card); border:1px solid var(--ring); padding:18px; border-radius:16px;
  box-shadow:0 8px 24px rgba(0,0,0,.05)
}
.card h3, .tile h3{margin-top:0}
.tag{
  display:inline-block; font-size:12px; background:#fff2; border:1px solid var(--ring);
  padding:4px 8px; border-radius:999px; margin-right:6px
}
.link{color:var(--nd-navy); text-decoration:none; font-weight:700}
.link[aria-disabled="true"]{opacity:.55; pointer-events:none}

/* Footer */
.footer{
  border-top:1px solid var(--ring); padding:24px 20px; text-align:center; color:var(--muted)
}
EOF

# 4) JS
cat > script.js <<'EOF'
(function(){
  // Year
  document.getElementById('year').textContent = new Date().getFullYear();

  // Theme toggle (persist to localStorage)
  const root = document.documentElement;
  const stored = localStorage.getItem('theme');
  if (stored) root.setAttribute('data-theme', stored);
  const btn = document.getElementById('themeToggle');
  function current(){ return root.getAttribute('data-theme') || 'light'; }
  btn.addEventListener('click', () => {
    const next = current() === 'dark' ? 'light' : 'dark';
    root.setAttribute('data-theme', next);
    localStorage.setItem('theme', next);
    btn.textContent = next === 'dark' ? '☼' : '☾';
  });
  // Initialize icon
  btn.textContent = current() === 'dark' ? '☼' : '☾';

  // Smooth scroll for same-page links
  document.querySelectorAll('a[href^="#"]').forEach(a=>{
    a.addEventListener('click', e=>{
      const id = a.getAttribute('href').slice(1);
      const el = document.getElementById(id);
      if(el){
        e.preventDefault();
        el.scrollIntoView({behavior:'smooth', block:'start'});
        history.pushState(null,'',`#${id}`);
      }
    });
  });
})();
EOF

# 5) Quick start message
cat > README.txt <<'EOF'
Local dev:
  python3 -m http.server 5500
Then open: http://localhost:5500
EOF

# 6) Run a local server (Ctrl+C to stop)
echo "Launching local server at http://localhost:5500 (press Ctrl+C to stop)..."
python3 -m http.server 5500




