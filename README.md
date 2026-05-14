<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mayank Waiker — GitHub README Preview</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Syne:wght@400;700;800&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --border: #30363d;
    --accent: #58a6ff;
    --accent2: #3fb950;
    --accent3: #f78166;
    --accent4: #d2a8ff;
    --text: #e6edf3;
    --muted: #8b949e;
    --mono: 'JetBrains Mono', monospace;
    --display: 'Syne', sans-serif;
  }

  body {
    background: #010409;
    color: var(--text);
    font-family: var(--mono);
    min-height: 100vh;
    padding: 2rem 1rem;
  }

  .page-label {
    text-align: center;
    font-family: var(--display);
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    color: var(--muted);
    margin-bottom: 1.5rem;
    text-transform: uppercase;
  }

  .readme-frame {
    max-width: 860px;
    margin: 0 auto;
    background: var(--bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 0 0 1px #ffffff08, 0 24px 64px #00000088;
  }

  /* GitHub-style top bar */
  .frame-bar {
    background: var(--surface);
    border-bottom: 1px solid var(--border);
    padding: 10px 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .dot { width: 12px; height: 12px; border-radius: 50%; }
  .dot-r { background: #ff5f57; }
  .dot-y { background: #febc2e; }
  .dot-g { background: #28c840; }
  .frame-title {
    flex: 1;
    text-align: center;
    font-size: 0.72rem;
    color: var(--muted);
    letter-spacing: 0.05em;
  }

  .readme-body {
    padding: 2.5rem 2.8rem;
    line-height: 1.7;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    margin-bottom: 2.5rem;
    position: relative;
  }

  .typing-line {
    font-size: 0.8rem;
    color: var(--accent2);
    margin-bottom: 0.6rem;
    letter-spacing: 0.08em;
  }

  .hero h1 {
    font-family: var(--display);
    font-size: 2.6rem;
    font-weight: 800;
    line-height: 1.1;
    background: linear-gradient(135deg, #e6edf3 30%, #58a6ff 70%, #d2a8ff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 0.5rem;
  }

  .hero-sub {
    font-size: 0.85rem;
    color: var(--muted);
    margin-bottom: 1.4rem;
  }

  .badge-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    justify-content: center;
    margin-bottom: 1.2rem;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.04em;
    border: 1px solid;
    transition: transform 0.15s, box-shadow 0.15s;
    cursor: default;
    text-decoration: none;
  }
  .badge:hover { transform: translateY(-2px); box-shadow: 0 4px 16px #00000040; }
  .badge-blue  { background: #1f3a5c; border-color: #58a6ff; color: #58a6ff; }
  .badge-green { background: #1a3a27; border-color: #3fb950; color: #3fb950; }
  .badge-purple{ background: #2d1f4a; border-color: #d2a8ff; color: #d2a8ff; }
  .badge-red   { background: #3a1f1f; border-color: #f78166; color: #f78166; }
  .badge-gold  { background: #3a2f10; border-color: #e3b341; color: #e3b341; }

  /* ── SECTION ── */
  .section { margin-bottom: 2rem; }

  .section-title {
    font-family: var(--display);
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
    border-bottom: 1px solid var(--border);
    padding-bottom: 6px;
    margin-bottom: 1rem;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-title::before {
    content: '';
    display: inline-block;
    width: 3px;
    height: 14px;
    background: var(--accent);
    border-radius: 2px;
  }

  /* ── ABOUT ── */
  .about-text {
    font-size: 0.83rem;
    color: #c9d1d9;
    line-height: 1.8;
  }
  .about-text .hl { color: var(--accent); font-weight: 700; }
  .about-text .hl2 { color: var(--accent2); font-weight: 700; }
  .about-text .hl3 { color: var(--accent4); font-weight: 700; }

  /* ── SKILLS GRID ── */
  .skills-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
  }

  .skill-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 12px 14px;
    transition: border-color 0.2s, transform 0.15s;
  }
  .skill-card:hover { border-color: var(--accent); transform: translateY(-2px); }

  .skill-card-label {
    font-size: 0.65rem;
    color: var(--muted);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 6px;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
  }

  .tag {
    font-size: 0.68rem;
    padding: 2px 8px;
    border-radius: 4px;
    background: #21262d;
    border: 1px solid #30363d;
    color: #c9d1d9;
  }
  .tag.blue   { background: #1f3a5c44; border-color: #58a6ff55; color: #79c0ff; }
  .tag.green  { background: #1a3a2744; border-color: #3fb95055; color: #56d364; }
  .tag.purple { background: #2d1f4a44; border-color: #d2a8ff55; color: #d2a8ff; }
  .tag.gold   { background: #3a2f1044; border-color: #e3b34155; color: #e3b341; }
  .tag.red    { background: #3a1f1f44; border-color: #f7816655; color: #ffa198; }

  /* ── PROJECTS ── */
  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 18px;
    margin-bottom: 10px;
    transition: border-color 0.2s, transform 0.15s;
    position: relative;
    overflow: hidden;
  }
  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px; height: 100%;
    border-radius: 2px 0 0 2px;
  }
  .project-card.blue::before  { background: var(--accent); }
  .project-card.green::before { background: var(--accent2); }
  .project-card:hover { border-color: #58a6ff55; transform: translateX(3px); }

  .project-name {
    font-family: var(--display);
    font-size: 0.9rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 5px;
  }
  .project-desc {
    font-size: 0.76rem;
    color: var(--muted);
    margin-bottom: 10px;
    line-height: 1.6;
  }
  .project-tech { display: flex; flex-wrap: wrap; gap: 5px; }

  /* ── STATS ── */
  .stats-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
    margin-bottom: 1rem;
  }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 14px;
    text-align: center;
  }
  .stat-num {
    font-family: var(--display);
    font-size: 1.6rem;
    font-weight: 800;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 4px;
  }
  .stat-label {
    font-size: 0.62rem;
    color: var(--muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  /* ── ACTIVITY BAR ── */
  .activity-section { margin-bottom: 2rem; }

  .contrib-grid {
    display: flex;
    gap: 3px;
    flex-wrap: wrap;
  }
  .contrib-week { display: flex; flex-direction: column; gap: 3px; }
  .contrib-day {
    width: 11px; height: 11px;
    border-radius: 2px;
    background: #161b22;
    border: 1px solid #30363d22;
    transition: transform 0.1s;
    cursor: default;
  }
  .contrib-day:hover { transform: scale(1.4); }
  .c1 { background: #0e4429; border-color: #0e442966; }
  .c2 { background: #006d32; border-color: #006d3266; }
  .c3 { background: #26a641; border-color: #26a64166; }
  .c4 { background: #39d353; border-color: #39d35366; }

  /* ── LEADERSHIP ── */
  .leadership-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 18px;
    margin-bottom: 10px;
    display: flex;
    gap: 14px;
    align-items: flex-start;
    transition: border-color 0.2s;
  }
  .leadership-card:hover { border-color: var(--accent4); }
  .lead-icon {
    width: 36px; height: 36px;
    border-radius: 8px;
    background: #2d1f4a;
    border: 1px solid #d2a8ff33;
    display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem;
    flex-shrink: 0;
  }
  .lead-title {
    font-family: var(--display);
    font-size: 0.88rem;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 3px;
  }
  .lead-desc { font-size: 0.74rem; color: var(--muted); line-height: 1.6; }
  .lead-power {
    font-size: 0.68rem;
    color: var(--accent4);
    font-weight: 700;
    margin-top: 5px;
  }

  /* ── CONNECT ── */
  .connect-row {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
  }
  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 8px 16px;
    border-radius: 8px;
    font-size: 0.75rem;
    font-weight: 700;
    font-family: var(--mono);
    letter-spacing: 0.04em;
    border: 1px solid;
    text-decoration: none;
    transition: transform 0.15s, box-shadow 0.15s, background 0.15s;
    cursor: pointer;
  }
  .connect-btn:hover { transform: translateY(-2px); box-shadow: 0 6px 20px #00000050; }
  .btn-blue   { background: #1f3a5c; border-color: #58a6ff; color: #58a6ff; }
  .btn-green  { background: #1a3a27; border-color: #3fb950; color: #3fb950; }
  .btn-purple { background: #2d1f4a; border-color: #d2a8ff; color: #d2a8ff; }

  /* ── FOOTER ── */
  .readme-footer {
    border-top: 1px solid var(--border);
    margin-top: 2rem;
    padding-top: 1.2rem;
    text-align: center;
    font-size: 0.68rem;
    color: var(--muted);
    letter-spacing: 0.06em;
  }
  .readme-footer span { color: var(--accent3); }

  /* ── COPY SECTION ── */
  .copy-section {
    max-width: 860px;
    margin: 2rem auto 0;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }
  .copy-bar {
    background: #21262d;
    border-bottom: 1px solid var(--border);
    padding: 10px 16px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .copy-bar-title { font-size: 0.72rem; color: var(--muted); letter-spacing: 0.08em; }
  .copy-btn {
    font-family: var(--mono);
    font-size: 0.68rem;
    padding: 4px 12px;
    border-radius: 6px;
    border: 1px solid var(--border);
    background: #30363d;
    color: var(--text);
    cursor: pointer;
    transition: background 0.15s;
  }
  .copy-btn:hover { background: #3d444d; }
  .code-block {
    padding: 1.2rem 1.5rem;
    font-size: 0.72rem;
    color: #8b949e;
    line-height: 1.8;
    max-height: 320px;
    overflow-y: auto;
    white-space: pre;
    font-family: var(--mono);
  }
  .code-block::-webkit-scrollbar { width: 6px; }
  .code-block::-webkit-scrollbar-track { background: transparent; }
  .code-block::-webkit-scrollbar-thumb { background: #30363d; border-radius: 3px; }

  /* animations */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .hero        { animation: fadeUp 0.5s ease both; }
  .section     { animation: fadeUp 0.5s ease both; }
  .section:nth-child(2) { animation-delay: 0.08s; }
  .section:nth-child(3) { animation-delay: 0.14s; }
  .section:nth-child(4) { animation-delay: 0.20s; }
  .section:nth-child(5) { animation-delay: 0.26s; }
  .section:nth-child(6) { animation-delay: 0.32s; }
  .section:nth-child(7) { animation-delay: 0.38s; }

  /* cursor blink */
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }
  .cursor { display: inline-block; animation: blink 1s step-end infinite; color: var(--accent2); }
</style>
</head>
<body>

<p class="page-label">GitHub Profile README — Live Preview</p>

<div class="readme-frame">
  <div class="frame-bar">
    <div class="dot dot-r"></div>
    <div class="dot dot-y"></div>
    <div class="dot dot-g"></div>
    <div class="frame-title">mayank-waiker / mayank-waiker / README.md</div>
  </div>

  <div class="readme-body">

    <!-- HERO -->
    <div class="hero">
      <div class="typing-line">&gt; initializing profile<span class="cursor">_</span></div>
      <h1>Mayank Waiker</h1>
      <p class="hero-sub">Data Science Student &nbsp;·&nbsp; Algorithm Designer &nbsp;·&nbsp; BI Developer &nbsp;·&nbsp; Indore, IN</p>
      <div class="badge-row">
        <span class="badge badge-blue">🎓 B.Tech CS (Data Science)</span>
        <span class="badge badge-green">📍 IIST Indore · 2023–27</span>
        <span class="badge badge-purple">🧠 ML Enthusiast</span>
        <span class="badge badge-gold">🏆 House Captain</span>
        <span class="badge badge-red">⚡ Open to Internships</span>
      </div>
    </div>

    <!-- ABOUT -->
    <div class="section">
      <div class="section-title">About Me</div>
      <p class="about-text">
        I'm a <span class="hl">Data Science engineering student</span> who loves turning raw data into meaningful stories.
        I've built <span class="hl2">pattern-recognition algorithms</span> for computational art and designed
        <span class="hl3">interactive BI dashboards</span> that drive real business decisions.
        Currently sharpening my skills in <span class="hl">Machine Learning</span>, <span class="hl2">EDA</span>,
        and <span class="hl3">statistical analysis</span> — one project at a time.
      </p>
    </div>

    <!-- STATS -->
    <div class="section">
      <div class="section-title">At a Glance</div>
      <div class="stats-row">
        <div class="stat-card">
          <div class="stat-num">2+</div>
          <div class="stat-label">Projects Built</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">7+</div>
          <div class="stat-label">Tech Skills</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">50+</div>
          <div class="stat-label">Students Led</div>
        </div>
      </div>
    </div>

    <!-- SKILLS -->
    <div class="section">
      <div class="section-title">Tech Stack</div>
      <div class="skills-grid">
        <div class="skill-card">
          <div class="skill-card-label">Languages</div>
          <div class="skill-tags">
            <span class="tag blue">Python</span>
            <span class="tag blue">C</span>
            <span class="tag blue">C++</span>
            <span class="tag blue">SQL</span>
            <span class="tag blue">HTML/CSS</span>
          </div>
        </div>
        <div class="skill-card">
          <div class="skill-card-label">Data Science</div>
          <div class="skill-tags">
            <span class="tag green">Pandas</span>
            <span class="tag green">NumPy</span>
            <span class="tag green">SciPy</span>
            <span class="tag green">Matplotlib</span>
          </div>
        </div>
        <div class="skill-card">
          <div class="skill-card-label">Analytics & BI</div>
          <div class="skill-tags">
            <span class="tag gold">Tableau</span>
            <span class="tag gold">EDA</span>
            <span class="tag gold">KPI Analysis</span>
            <span class="tag gold">Dashboard Design</span>
          </div>
        </div>
        <div class="skill-card">
          <div class="skill-card-label">ML & Algorithms</div>
          <div class="skill-tags">
            <span class="tag purple">Scikit-learn</span>
            <span class="tag purple">Feature Eng.</span>
            <span class="tag purple">Pattern Recognition</span>
          </div>
        </div>
        <div class="skill-card">
          <div class="skill-card-label">Data Engineering</div>
          <div class="skill-tags">
            <span class="tag red">Apache Kafka</span>
            <span class="tag red">Data Wrangling</span>
            <span class="tag red">Data Cleaning</span>
          </div>
        </div>
        <div class="skill-card">
          <div class="skill-card-label">Tools</div>
          <div class="skill-tags">
            <span class="tag">Jupyter</span>
            <span class="tag">Google Colab</span>
            <span class="tag">MS Excel</span>
            <span class="tag">Git</span>
          </div>
        </div>
      </div>
    </div>

    <!-- PROJECTS -->
    <div class="section">
      <div class="section-title">Featured Projects</div>

      <div class="project-card blue">
        <div class="project-name">🎨 Computational Kolam Design Generator</div>
        <div class="project-desc">
          Designed an algorithm to analyse symmetry, loops, and geometric structures in traditional Indian Kolam art —
          then automatically generate new designs. Converts abstract mathematical rules into visual outputs using
          NumPy matrix operations and Matplotlib rendering.
        </div>
        <div class="project-tech">
          <span class="tag blue">Python</span>
          <span class="tag blue">NumPy</span>
          <span class="tag blue">Matplotlib</span>
          <span class="tag">Algorithm Design</span>
          <span class="tag">Computational Geometry</span>
          <span class="tag">Pattern Recognition</span>
        </div>
      </div>

      <div class="project-card green">
        <div class="project-name">📊 Supermarket Sales Intelligence Dashboard</div>
        <div class="project-desc">
          End-to-end BI project: cleaned and wrangled raw transactional sales data, performed full EDA,
          then built an interactive Tableau dashboard with KPI cards and trend analysis — enabling
          stakeholders to identify top-performing product lines and seasonal patterns at a glance.
        </div>
        <div class="project-tech">
          <span class="tag gold">Tableau</span>
          <span class="tag gold">EDA</span>
          <span class="tag gold">KPI Analysis</span>
          <span class="tag">Data Cleaning</span>
          <span class="tag">Trend Analysis</span>
          <span class="tag">Business Intelligence</span>
        </div>
      </div>
    </div>

    <!-- ACTIVITY -->
    <div class="section activity-section">
      <div class="section-title">Contribution Activity</div>
      <div class="contrib-grid" id="contrib"></div>
    </div>

    <!-- LEADERSHIP -->
    <div class="section">
      <div class="section-title">Leadership & Activities</div>

      <div class="leadership-card">
        <div class="lead-icon">🏆</div>
        <div>
          <div class="lead-title">School House Captain</div>
          <div class="lead-desc">Spearheaded coordination of 50+ students across academic, cultural, and competitive events. Championed communication between students and administration, mentored peers, and drove high-performance culture.</div>
          <div class="lead-power">⚡ Spearheaded · Championed · Mentored · Drove results</div>
        </div>
      </div>

      <div class="leadership-card">
        <div class="lead-icon">🚀</div>
        <div>
          <div class="lead-title">Technical Projects & Innovation</div>
          <div class="lead-desc">Consistently pursued hands-on technical challenges beyond the curriculum — proactively building data science expertise through self-initiated projects, driving ideas from ideation to working implementation.</div>
          <div class="lead-power">⚡ Proactively · Consistently · Self-initiated · End-to-end</div>
        </div>
      </div>
    </div>

    <!-- CONNECT -->
    <div class="section">
      <div class="section-title">Connect With Me</div>
      <div class="connect-row">
        <a class="connect-btn btn-blue" href="https://linkedin.com/in/mayank-waiker-043739331" target="_blank">
          💼 LinkedIn
        </a>
        <a class="connect-btn btn-purple" href="mailto:Mayankwaiker05@gmail.com">
          ✉️ Email Me
        </a>
        <a class="connect-btn btn-green" href="#">
          📄 View Resume
        </a>
      </div>
    </div>

    <div class="readme-footer">
      Built with <span>♥</span> in Indore &nbsp;·&nbsp; Data Science @ IIST &nbsp;·&nbsp; Always learning, always building
    </div>

  </div>
</div>

<!-- MARKDOWN CODE COPY SECTION -->
<div class="copy-section" style="margin-top:2rem;">
  <div class="copy-bar">
    <span class="copy-bar-title">📋 README.md — Paste this into your GitHub profile repo</span>
    <button class="copy-btn" onclick="copyCode()">Copy</button>
  </div>
  <div class="code-block" id="mdCode">
&lt;!-- MAYANK WAIKER — GitHub Profile README --&gt;
&lt;!-- Create repo: github.com/new → name it exactly your username → add README.md --&gt;

&lt;div align="center"&gt;

```
███╗   ███╗ █████╗ ██╗   ██╗ █████╗ ███╗   ██╗██╗  ██╗
████╗ ████║██╔══██╗╚██╗ ██╔╝██╔══██╗████╗  ██║██║ ██╔╝
██╔████╔██║███████║ ╚████╔╝ ███████║██╔██╗ ██║█████╔╝
██║╚██╔╝██║██╔══██║  ╚██╔╝  ██╔══██║██║╚██╗██║██╔═██╗
██║ ╚═╝ ██║██║  ██║   ██║   ██║  ██║██║ ╚████║██║  ██╗
╚═╝     ╚═╝╚═╝  ╚═╝   ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═══╝╚═╝  ╚═╝
```

### 🎓 Data Science Student · Algorithm Designer · BI Developer
### 📍 Indore Institute of Science &amp; Technology · 2023–2027

![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&amp;logo=linkedin&amp;logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&amp;logo=python&amp;logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&amp;logo=tableau&amp;logoColor=white)
![Open to Work](https://img.shields.io/badge/Open%20to-Internships-brightgreen?style=for-the-badge)

&lt;/div&gt;

---

## 👋 About Me

&gt; *"Turning raw data into meaningful stories — one algorithm at a time."*

I'm a **Data Science engineering student** who loves the intersection of mathematics, code, and insight.
I've built **pattern-recognition algorithms** for computational art and designed **interactive BI dashboards**
that drive real business decisions. Currently sharpening my edge in ML, EDA, and statistical analysis.

- 🔭 Currently working on: expanding ML project portfolio
- 🌱 Learning: Scikit-learn · TensorFlow · Hypothesis Testing
- ⚡ Fun fact: I used Python to generate traditional Indian art with math

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| **Languages** | Python · C · C++ · SQL · HTML · CSS |
| **Data Science** | Pandas · NumPy · SciPy · Matplotlib |
| **Analytics & BI** | Tableau · EDA · KPI Analysis · Dashboard Design |
| **ML & Algorithms** | Scikit-learn · Feature Engineering · Pattern Recognition |
| **Data Engineering** | Apache Kafka · Data Wrangling · Data Cleaning |
| **Tools** | Jupyter · Google Colab · MS Excel · Git |

---

## 🚀 Featured Projects

### 🎨 Computational Kolam Design Generator
&gt; *Python · NumPy · Matplotlib · Algorithm Design · Computational Geometry*

Designed an algorithm to analyse symmetry, loops, and geometric structures in traditional Indian Kolam art —
then automatically generate new designs. Converts abstract mathematical rules into visual outputs via NumPy
matrix operations and Matplotlib rendering.

**Key skills demonstrated:** Pattern Recognition · Grid-based Data Structures · Scientific Computing

---

### 📊 Supermarket Sales Intelligence Dashboard
&gt; *Tableau · EDA · Business Intelligence · KPI Analysis*

End-to-end BI project: cleaned and wrangled raw transactional data, performed full EDA, then built an
interactive Tableau dashboard with KPI cards and trend charts — enabling stakeholders to identify
top-performing product lines and seasonal patterns instantly.

**Key skills demonstrated:** Data Cleaning · Trend Analysis · Dashboard Design · Actionable Insights

---

## 🏆 Leadership

**School House Captain**
- 🚀 Spearheaded coordination of **50+ students** across academic &amp; competitive events
- 💬 Championed communication between student body and administration
- 🎯 Mentored peers and drove a high-performance, results-oriented team culture
- ✅ Demonstrated accountability, delegation, and leadership under pressure

---

## 📬 Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mayank%20Waiker-0077B5?style=flat-square&amp;logo=linkedin)](https://linkedin.com/in/mayank-waiker-043739331)
[![Email](https://img.shields.io/badge/Email-Mayankwaiker05%40gmail.com-D14836?style=flat-square&amp;logo=gmail&amp;logoColor=white)](mailto:Mayankwaiker05@gmail.com)

---

&lt;div align="center"&gt;
&lt;i&gt;Built with ♥ in Indore · Data Science @ IIST · Always learning, always building&lt;/i&gt;
&lt;/div&gt;
  </div>
</div>

<script>
// Generate contribution grid
const grid = document.getElementById('contrib');
const levels = [0,0,0,1,0,0,1,2,1,0,1,2,3,2,1,2,3,4,3,2,3,4,3,2,1,2,3,2,1,0,1,2,1,0,1,2,3,2,3,4,3,2,1,2,3,4,3,4,3,2,3,4,3,2,1];
const classMap = ['','c1','c2','c3','c4'];
let weekDiv;
levels.forEach((l, i) => {
  if (i % 7 === 0) { weekDiv = document.createElement('div'); weekDiv.className = 'contrib-week'; grid.appendChild(weekDiv); }
  const d = document.createElement('div');
  d.className = 'contrib-day ' + classMap[l];
  d.title = l === 0 ? 'No contributions' : `${l} contribution${l>1?'s':''}`;
  weekDiv.appendChild(d);
});

// Copy markdown
function copyCode() {
  const code = document.getElementById('mdCode').innerText;
  navigator.clipboard.writeText(code).then(() => {
    const btn = document.querySelector('.copy-btn');
    btn.textContent = 'Copied!';
    btn.style.color = '#3fb950';
    setTimeout(() => { btn.textContent = 'Copy'; btn.style.color = ''; }, 2000);
  });
}
</script>
</body>
</html>
