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
  --muted:#A3A9B4;
  --card:#121a2c;
  --ring:rgba(174,145,66,.25);
}
*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family:'Inter',system-ui,-apple-system,Segoe UI,Roboto,Helvetica,Arial,sans-serif;
  color:var(--ink); background:var(--paper); line-height:1.6;
}
img{max-width:100%; height:auto; display:block}
a{color:inherit}

/* Accessibility */
.skip-link{
  position:absolute; left:-9999px; top:auto; width:1px; height:1px; overflow:hidden;
}
.skip-link:focus{
  position:static; width:auto; height:auto; padding:8px 12px; background:var(--nd-gold); color:#111; z-index:1000;
}

/* Nav */
.nav{position:sticky; top:0; z-index:50; border-bottom:1px solid var(--ring);
  background:linear-gradient(to bottom, rgba(255,255,255,.85), rgba(255,255,255,.6));
  backdrop-filter:saturate(180%) blur(12px);
}
:root[data-theme="dark"] .nav{
  background:linear-gradient(to bottom, rgba(11,16,32,.85), rgba(11,16,32,.6));
}
.nav-inner{max-width:1100px; margin:0 auto; display:flex; gap:16px; align-items:center; justify-content:space-between; padding:12px 16px}
.brand{font-weight:800; text-decoration:none; color:var(--nd-navy)}
.nav a{text-decoration:none; margin:0 8px; font-weight:600}
#themeToggle{margin-left:4px; border:1px solid var(--ring); background:transparent; color:var(--ink); padding:8px 10px; border-radius:10px; cursor:pointer}

/* Hero */
.hero{max-width:1100px; margin:0 auto; padding:56px 16px 24px; display:grid; gap:24px; grid-template-columns:1.1fr .9fr; align-items:center}
@media (max-width:900px){ .hero{grid-template-columns:1fr} }
.badge{display:inline-block; background:var(--nd-navy); color:white; padding:6px 10px; border-radius:999px; font-size:12px}
.hero h1{font-size:40px; line-height:1.2; margin:10px 0 6px}
@media (min-width:900px){ .hero h1{font-size:56px} }
.lead{font-size:18px; color:var(--muted); max-width:65ch}
.accent{color:var(--nd-gold)}
.cta{display:flex; gap:12px; margin-top:14px}
.btn{display:inline-block; padding:12px 18px; border-radius:12px; text-decoration:none; font-weight:700; border:1px solid var(--ring)}
.btn.primary{background:var(--nd-gold); color:#111; border-color:transparent}
.btn.ghost{background:transparent}
.btn:hover{transform:translateY(-1px)}
.hero-art{width:100%; height:160px}
.helmet{fill:#AE9142}
.helmet-face{fill:#8c7536}
.paddle{fill:#AE9142}
.handle{fill:#8c7536}
.pickleball{fill:#ffd34d}
.pb-hole{fill:#e0b800}

/* Sections */
.section{padding:48px 16px; max-width:1100px; margin:0 auto}
.section h2{font-size:28px; margin:0 0 16px}
.grid{display:grid; gap:16px}
.grid.two{grid-template-columns:1fr}
@media (min-width:900px){ .grid.two{grid-template-columns:repeat(2,1fr)} }

.card{
  background:var(--card); border:1px solid var(--ring); padding:18px; border-radius:16px;
  box-shadow:0 8px 24px rgba(0,0,0,.05)
}
.bullets{padding-left:18px}
.banner{margin-top:16px; border:1px solid var(--ring); border-radius:16px; overflow:hidden; background:var(--card)}
.banner figcaption{padding:10px 12px; color:var(--muted); font-size:14px}
.links{display:flex; gap:12px; flex-wrap:wrap; margin-top:16px}
.link{color:var(--nd-navy); text-decoration:none; font-weight:700}

/* Footer */
.footer{border-top:1px solid var(--ring); padding:24px 16px; text-align:center; color:var(--muted)}
