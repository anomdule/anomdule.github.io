<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pre-Doctoral Journey — Origin Story</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bangers&family=Bebas+Neue&family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@500&display=swap" rel="stylesheet">
<style>
  :root{
    --font-body: 'Inter', system-ui, sans-serif;
    --font-mono: 'JetBrains Mono', monospace;
    --radius: 14px;
    /* Spidey palette (default) */
    --bg: #0d1b2a;
    --bg-2: #10233a;
    --panel: #132a44;
    --primary: #e0281c;
    --secondary: #2e6fce;
    --accent: #f6f1e7;
    --text: #eef3f8;
    --text-dim: #9fb3c8;
    --line: rgba(255,255,255,0.10);
    --font-display: 'Bangers', cursive;
    --glow: rgba(224,40,28,0.35);
  }
  body.theme-bat{
    --bg: #08090c;
    --bg-2: #101216;
    --panel: #16181d;
    --primary: #e8c14a;
    --secondary: #6b7280;
    --accent: #e8c14a;
    --text: #eceef1;
    --text-dim: #8a8f98;
    --line: rgba(232,193,74,0.14);
    --font-display: 'Bebas Neue', sans-serif;
    --glow: rgba(232,193,74,0.28);
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background: radial-gradient(circle at 20% 0%, var(--bg-2), var(--bg) 60%);
    color:var(--text);
    font-family:var(--font-body);
    line-height:1.6;
    transition: background .5s ease, color .5s ease;
    overflow-x:hidden;
  }
  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.01ms !important; transition-duration:0.01ms !important;}
  }

  /* cursor fx layer */
  #fx{
    position:fixed; inset:0; pointer-events:none; z-index:5; mix-blend-mode: screen;
  }
  .bat-glow{
    position:fixed; width:340px; height:340px; border-radius:50%;
    background: radial-gradient(circle, var(--glow), transparent 70%);
    transform:translate(-50%,-50%); pointer-events:none; z-index:4;
    transition: opacity .3s ease;
  }
  .web-dot{
    position:fixed; width:6px; height:6px; border-radius:50%;
    background: var(--primary); opacity:0.7; pointer-events:none; z-index:4;
    box-shadow: 0 0 8px var(--glow);
  }

  .wrap{max-width:980px; margin:0 auto; padding:0 24px;}

  /* topbar */
  .topbar{
    position:sticky; top:0; z-index:20;
    backdrop-filter: blur(10px);
    background: rgba(8,10,14,0.55);
    border-bottom:1px solid var(--line);
  }
  .topbar-inner{
    max-width:980px; margin:0 auto; padding:14px 24px;
    display:flex; align-items:center; justify-content:space-between; gap:16px;
  }
  .brand{ font-family:var(--font-display); letter-spacing:0.5px; font-size:22px; color:var(--primary);}
  .toggle{
    display:flex; align-items:center; gap:10px; font-family:var(--font-mono); font-size:12px; color:var(--text-dim);
  }
  .switch{
    position:relative; width:64px; height:30px; border-radius:30px;
    background: var(--panel); border:1px solid var(--line); cursor:pointer;
  }
  .switch .knob{
    position:absolute; top:3px; left:3px; width:24px; height:24px; border-radius:50%;
    background: var(--primary); transition: left .35s cubic-bezier(.2,.9,.3,1.2), background .35s ease;
    display:flex; align-items:center; justify-content:center; font-size:13px;
  }
  body.theme-bat .switch .knob{ left:37px; }

  /* hero */
  .hero{ position:relative; padding:96px 0 64px; overflow:hidden;}
  .hero::before{
    content:""; position:absolute; inset:0; z-index:0; opacity:0.5;
    background-image:
      repeating-linear-gradient(60deg, var(--line) 0 1px, transparent 1px 90px),
      repeating-linear-gradient(-60deg, var(--line) 0 1px, transparent 1px 90px),
      repeating-linear-gradient(0deg, var(--line) 0 1px, transparent 1px 90px);
    mask-image: radial-gradient(circle at 30% 20%, black, transparent 70%);
  }
  body.theme-bat .hero::before{
    background-image: radial-gradient(circle at 25% 15%, var(--glow), transparent 45%);
    mask-image:none;
  }
  .eyebrow{
    font-family:var(--font-mono); font-size:12px; letter-spacing:2px; text-transform:uppercase;
    color:var(--primary); display:inline-block; margin-bottom:14px; position:relative; z-index:1;
  }
  h1.title{
    font-family:var(--font-display); font-size:clamp(42px, 8vw, 78px); line-height:1.02; margin:0 0 18px;
    color:var(--accent); position:relative; z-index:1; letter-spacing:0.5px;
  }
  body.theme-bat h1.title{ text-shadow: 0 0 24px var(--glow); }
  .hero p.sub{ max-width:560px; color:var(--text-dim); font-size:17px; position:relative; z-index:1;}
  .hero-tag{
    display:inline-flex; gap:8px; align-items:center; margin-top:22px; position:relative; z-index:1;
    font-family:var(--font-mono); font-size:12px; color:var(--text-dim); border:1px solid var(--line);
    padding:8px 14px; border-radius:30px; background:rgba(255,255,255,0.02);
  }
  .hero-tag b{ color:var(--primary);}

  /* stats */
  .stats{ display:grid; grid-template-columns:repeat(4,1fr); gap:1px; background:var(--line); border:1px solid var(--line); border-radius:var(--radius); overflow:hidden; margin:40px 0 72px;}
  .stat{ background:var(--panel); padding:26px 18px; text-align:center;}
  .stat .num{ font-family:var(--font-display); font-size:40px; color:var(--primary); display:block;}
  .stat .lbl{ font-size:12px; color:var(--text-dim); text-transform:uppercase; letter-spacing:1px; margin-top:4px;}
  @media (max-width:640px){ .stats{grid-template-columns:repeat(2,1fr);} }

  section{ padding:56px 0; border-top:1px solid var(--line);}
  .section-head{ display:flex; align-items:baseline; gap:14px; margin-bottom:28px;}
  .section-num{ font-family:var(--font-mono); color:var(--primary); font-size:13px;}
  h2{ font-family:var(--font-display); font-size:32px; margin:0; letter-spacing:0.3px; color:var(--accent);}
  h2 + p.lead{ color:var(--text-dim); max-width:640px; margin-top:-14px;}

  /* origin timeline */
  .timeline{ position:relative; margin-top:32px; padding-left:28px;}
  .timeline::before{
    content:""; position:absolute; left:5px; top:6px; bottom:6px; width:2px;
    background: linear-gradient(var(--primary), var(--secondary));
    opacity:0.5;
  }
  .t-item{ position:relative; padding:0 0 34px 20px; cursor:pointer;}
  .t-item:last-child{ padding-bottom:0;}
  .t-dot{
    position:absolute; left:-28px; top:2px; width:12px; height:12px; border-radius:50%;
    background:var(--bg); border:2px solid var(--primary); transition: all .25s ease;
  }
  .t-item.active .t-dot{ background:var(--primary); box-shadow:0 0 12px var(--glow); transform:scale(1.2);}
  .t-year{ font-family:var(--font-mono); font-size:11px; color:var(--primary); text-transform:uppercase; letter-spacing:1px;}
  .t-title{ font-weight:700; font-size:16px; margin:2px 0 6px;}
  .t-detail{ color:var(--text-dim); font-size:14.5px; max-height:0; overflow:hidden; transition: max-height .35s ease;}
  .t-item.active .t-detail{ max-height:200px;}

  /* accordion */
  .acc-item{ border:1px solid var(--line); border-radius:var(--radius); margin-bottom:10px; overflow:hidden; background:var(--panel);}
  .acc-head{ padding:16px 20px; display:flex; justify-content:space-between; align-items:center; cursor:pointer; font-weight:600;}
  .acc-head .plus{ color:var(--primary); font-family:var(--font-mono); transition:transform .3s ease;}
  .acc-item.open .plus{ transform:rotate(45deg);}
  .acc-body{ max-height:0; overflow:hidden; transition:max-height .4s ease;}
  .acc-body-inner{ padding:0 20px 18px; color:var(--text-dim); font-size:14.5px;}
  .acc-body-inner b{ color:var(--text);}

  /* filter + cards */
  .filters{ display:flex; gap:8px; flex-wrap:wrap; margin-bottom:22px;}
  .chip{
    font-family:var(--font-mono); font-size:12px; padding:8px 14px; border-radius:30px;
    border:1px solid var(--line); color:var(--text-dim); cursor:pointer; background:transparent; transition:.2s ease;
  }
  .chip.active{ background:var(--primary); color:var(--bg); border-color:var(--primary); font-weight:700;}
  .uni-grid{ display:grid; grid-template-columns:repeat(auto-fill, minmax(260px,1fr)); gap:14px;}
  .uni-card{ border:1px solid var(--line); background:var(--panel); border-radius:var(--radius); padding:18px; transition:.25s ease;}
  .uni-card:hover{ border-color:var(--primary); transform:translateY(-2px);}
  .uni-card .school{ font-weight:700; font-size:15px;}
  .uni-card .program{ color:var(--text-dim); font-size:13px; margin:2px 0 12px;}
  .badge{ display:inline-block; font-size:11px; font-family:var(--font-mono); padding:3px 9px; border-radius:20px; margin-bottom:10px;}
  .badge.offer{ background:rgba(46,150,90,0.15); color:#5fd18a;}
  .badge.declined{ background:rgba(224,40,28,0.12); color:var(--primary);}
  .badge.rejected{ background:rgba(150,150,150,0.15); color:#a8a8a8;}
  .badge.waitlist{ background:rgba(232,193,74,0.15); color:#e8c14a;}
  .journey-steps{ font-size:13px; color:var(--text-dim); line-height:1.8;}

  /* reveal */
  .reveal-btn{
    font-family:var(--font-mono); font-size:13px; background:var(--panel); color:var(--primary);
    border:1px solid var(--line); padding:10px 18px; border-radius:30px; cursor:pointer;
  }
  .reveal-box{ max-height:0; overflow:hidden; transition:max-height .5s ease; margin-top:16px;}
  .reveal-box.open{ max-height:400px;}
  .reveal-box p{ color:var(--text-dim); font-size:14.5px;}

  /* checklist */
  .lessons{ list-style:none; padding:0; margin:0; display:grid; gap:10px;}
  .lessons li{
    display:flex; gap:12px; align-items:flex-start; padding:14px 16px; border:1px solid var(--line);
    border-radius:var(--radius); background:var(--panel); cursor:pointer; transition:.2s ease;
  }
  .lessons li:hover{ border-color:var(--primary);}
  .lessons li .box{
    flex:0 0 18px; height:18px; width:18px; border:2px solid var(--primary); border-radius:4px; margin-top:2px;
    display:flex; align-items:center; justify-content:center; font-size:12px; color:var(--bg);
  }
  .lessons li.checked .box{ background:var(--primary);}
  .lessons li.checked span.txt{ text-decoration:line-through; color:var(--text-dim);}

  blockquote.callout{
    border-left:3px solid var(--primary); padding:14px 20px; background:rgba(255,255,255,0.02);
    border-radius:0 var(--radius) var(--radius) 0; color:var(--text-dim); font-size:14.5px;
  }
  footer{ text-align:center; padding:60px 0 40px; color:var(--text-dim); font-size:13px; font-family:var(--font-mono);}
  a{ color:var(--primary);}
</style>
</head>
<body>

<div class="bat-glow" id="glow" style="opacity:0"></div>

<nav class="topbar">
  <div class="topbar-inner">
    <div class="brand">PhD // Origin Story</div>
    <div class="toggle">
      <span id="labelLeft">🕸️ Web-Slinger</span>
      <div class="switch" id="themeSwitch"><div class="knob" id="knob">🕸️</div></div>
      <span id="labelRight">🦇 Dark Knight</span>
    </div>
  </div>
</nav>

<header class="hero">
  <div class="wrap">
    <span class="eyebrow">Chemical Engineering → Applied Economics</span>
    <h1 class="title">Every Hero<br>Has an Origin Story.</h1>
    <p class="sub">This page documents my journey to a Ph.D. in Applied Economics — from building research experience to navigating interviews, offers, and ultimately choosing Penn State University.</p>
    <div class="hero-tag">🎓 Final Destination: <b>Penn State University (EEFE)</b></div>
  </div>
</header>

<div class="wrap">
  <div class="stats">
    <div class="stat"><span class="num" data-target="37">0</span><span class="lbl">Applications sent</span></div>
    <div class="stat"><span class="num" data-target="34">0</span><span class="lbl">Reached a decision</span></div>
    <div class="stat"><span class="num" data-target="12">0</span><span class="lbl">Positive outcomes</span></div>
    <div class="stat"><span class="num" data-target="7">0</span><span class="lbl">Funded offers</span></div>
  </div>

  <section id="origin">
    <div class="section-head"><span class="section-num">01</span><h2>Origin Story</h2></div>
    <p class="lead">Click a milestone to expand it — the training arc before the offers started coming in.</p>
    <div class="timeline" id="timeline">
      <div class="t-item active">
        <div class="t-dot"></div>
        <div class="t-year">B.Tech</div>
        <div class="t-title">Chemical Engineering — Dr. Babasaheb Ambedkar Technological University</div>
        <div class="t-detail">Coursework in Calculus, Linear Algebra, Differential Equations. No formal Real Analysis — contrary to popular belief, that wasn't the end of the world.</div>
      </div>
      <div class="t-item">
        <div class="t-dot"></div>
        <div class="t-year">Gap Years</div>
        <div class="t-title">Three years away from formal education</div>
        <div class="t-detail">Personal and family circumstances. Kept learning independently through MITx courses in Probability, Statistics, and Microeconomics.</div>
      </div>
      <div class="t-item">
        <div class="t-dot"></div>
        <div class="t-year">M.S.</div>
        <div class="t-title">Applied Economics — University of Maryland</div>
        <div class="t-detail">Core: Micro, Macro, Econometrics. Fields: Environmental Economics, Development Economics, Program Evaluation, Game Theory.</div>
      </div>
      <div class="t-item">
        <div class="t-dot"></div>
        <div class="t-year">3+ Years</div>
        <div class="t-title">Research Assistant — Center for Global Sustainability</div>
        <div class="t-detail">Focus on energy, equity, transportation, and climate policy. Built skills in econometrics, causal inference, geospatial analysis, and scientific writing.</div>
      </div>
      <div class="t-item">
        <div class="t-dot"></div>
        <div class="t-year">1 Year</div>
        <div class="t-title">Research Analyst Consultant — World Bank</div>
        <div class="t-detail">Supported a Senior Economist on agriculture research in Sub-Saharan Africa. Strengthened empirical research and policy evaluation skills.</div>
      </div>
      <div class="t-item">
        <div class="t-dot"></div>
        <div class="t-year">Cycle</div>
        <div class="t-title">37 applications, 7 funded offers</div>
        <div class="t-detail">Including a second-authored paper with Jiehong Lou, under revise-and-resubmit at Environmental Research & Social Science during the cycle.</div>
      </div>
      <div class="t-item">
        <div class="t-dot"></div>
        <div class="t-year">Now</div>
        <div class="t-title">Ph.D. candidate — Penn State University (EEFE)</div>
        <div class="t-detail">Energy, Environmental & Food Economics. Chosen for research fit, faculty interests, and long-term career goals.</div>
      </div>
    </div>
  </section>

  <section id="builder">
    <div class="section-head"><span class="section-num">02</span><h2>Building the Application</h2></div>
    <p class="lead">Five components did most of the work. Tap each to open it.</p>
    <div id="accordion">
      <div class="acc-item">
        <div class="acc-head">📚 GRE Quantitative: 160 <span class="plus">+</span></div>
        <div class="acc-body"><div class="acc-body-inner">Around the 50th percentile at the time — not exactly what Reddit wanted. Friends at Maryland, Cornell, and Virginia Tech were scoring 165+. Took the GRE <b>four more times</b> chasing that number. Still no 165. Every attempt ended with sushi somewhere in the D.C. area, so it's unclear whether this was test prep or a restaurant tour.</div></div>
      </div>
      <div class="acc-item">
        <div class="acc-head">📄 Research Writing Sample <span class="plus">+</span></div>
        <div class="acc-body"><div class="acc-body-inner">One solo-authored empirical paper using causal inference methods. <b>Six pages</b>, representing <b>6–7 months</b> of work, plus ~10 pages of supplementary material. Those six pages came up in almost every interview.</div></div>
      </div>
      <div class="acc-item">
        <div class="acc-head">✉️ Recommendation Letters <span class="plus">+</span></div>
        <div class="acc-body"><div class="acc-body-inner">Two research supervisors (Center for Global Sustainability + World Bank, depending on program), and one academic letter from <b>instructors</b> — not professors — in Maryland's Applied Economics program. Great letters come from people who genuinely know your work.</div></div>
      </div>
      <div class="acc-item">
        <div class="acc-head">🌶️ The Secret Sauce <span class="plus">+</span></div>
        <div class="acc-body"><div class="acc-body-inner">Weekly mentorship from an economist at Amazon — writing sample, Statement of Purpose, CV, school selection, mock interviews, all of it. Identity classified. Every applicant deserves to find their own.</div></div>
      </div>
      <div class="acc-item">
        <div class="acc-head">🎤 Interviews <span class="plus">+</span></div>
        <div class="acc-body"><div class="acc-body-inner">Mostly felt like research conversations, not interrogations. Faculty cared about research experience, future ideas, and fit — thorough prep on the writing sample and SOP mattered more than rehearsed answers.</div></div>
      </div>
    </div>
  </section>

  <section id="outcomes">
    <div class="section-head"><span class="section-num">03</span><h2>The Application Map</h2></div>
    <p class="lead">37 applications, filtered by how the story ended.</p>
    <div class="filters" id="filters">
      <button class="chip active" data-filter="all">All (12)</button>
      <button class="chip" data-filter="offer">Funded Offers (7)</button>
      <button class="chip" data-filter="declined">Declined by Me</button>
      <button class="chip" data-filter="waitlist">Waitlist / Pending</button>
      <button class="chip" data-filter="rejected">Not Admitted</button>
    </div>
    <div class="uni-grid" id="uniGrid"></div>
  </section>

  <section id="rejections">
    <div class="section-head"><span class="section-num">04</span><h2>Character Development</h2></div>
    <p class="lead">Every applicant has a rejection folder. Here's part of mine.</p>
    <button class="reveal-btn" id="revealBtn">🕶️ Open the folder</button>
    <div class="reveal-box" id="revealBox">
      <p>Stanford University (ESS), Duke University (UPEP), Carnegie Mellon University (Public Policy), Columbia University (Sustainable Development), Economics programmes at UC San Diego, UT Austin, and Michigan State, and Agricultural Economics programmes at the University of Maryland, UC Berkeley, UIUC, and UW–Madison.</p>
      <blockquote class="callout">No health insurance was a deal-breaker already 😅 — Georgia State waitlist, not pursued.</blockquote>
    </div>
  </section>

  <section id="lessons">
    <div class="section-head"><span class="section-num">05</span><h2>Lessons Learned</h2></div>
    <p class="lead">Check them off as you internalize them.</p>
    <ul class="lessons" id="lessonsList">
      <li><div class="box">✓</div><span class="txt">Research experience mattered far more than expected.</span></li>
      <li><div class="box">✓</div><span class="txt">A strong writing sample opens more doors than a slightly higher GRE score.</span></li>
      <li><div class="box">✓</div><span class="txt">Great recommendation letters come from people who know your work — not the most famous names.</span></li>
      <li><div class="box">✓</div><span class="txt">Mentorship is invaluable.</span></li>
      <li><div class="box">✓</div><span class="txt">Apply broadly, but apply strategically.</span></li>
      <li><div class="box">✓</div><span class="txt">There is no single path into a Ph.D.</span></li>
    </ul>
  </section>

  <section id="why">
    <div class="section-head"><span class="section-num">06</span><h2>Why Penn State?</h2></div>
    <p class="lead">Research fit, faculty interests, long-term career goals, funding, and the chance to work in energy, environmental, and applied economics within an interdisciplinary department.</p>
  </section>
</div>

<footer>
  If this page helps even one applicant see there's no single blueprint into a Ph.D. — it's served its purpose. Good luck 🚀
</footer>

<script>
(function(){
  const body = document.body;
  const themeSwitch = document.getElementById('themeSwitch');
  const knob = document.getElementById('knob');
  const glow = document.getElementById('glow');
  let isBat = false;

  themeSwitch.addEventListener('click', () => {
    isBat = !isBat;
    body.classList.toggle('theme-bat', isBat);
    knob.textContent = isBat ? '🦇' : '🕸️';
    glow.style.opacity = isBat ? '1' : '0';
  });

  // cursor fx
  const dots = [];
  document.addEventListener('mousemove', (e) => {
    if (isBat) {
      glow.style.left = e.clientX + 'px';
      glow.style.top = e.clientY + 'px';
    } else {
      const d = document.createElement('div');
      d.className = 'web-dot';
      d.style.left = e.clientX + 'px';
      d.style.top = e.clientY + 'px';
      document.body.appendChild(d);
      setTimeout(() => d.remove(), 400);
    }
  });

  // stat counters
  const stats = document.querySelectorAll('.stat .num');
  const io = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const el = entry.target;
        const target = parseInt(el.dataset.target, 10);
        let cur = 0;
        const step = Math.max(1, Math.round(target / 40));
        const tick = () => {
          cur += step;
          if (cur >= target) { el.textContent = target; return; }
          el.textContent = cur;
          requestAnimationFrame(tick);
        };
        tick();
        io.unobserve(el);
      }
    });
  }, { threshold: 0.5 });
  stats.forEach(s => io.observe(s));

  // timeline
  document.querySelectorAll('.t-item').forEach(item => {
    item.addEventListener('click', () => {
      const wasActive = item.classList.contains('active');
      document.querySelectorAll('.t-item').forEach(i => i.classList.remove('active'));
      if (!wasActive) item.classList.add('active');
    });
  });

  // accordion
  document.querySelectorAll('.acc-item').forEach(item => {
    const head = item.querySelector('.acc-head');
    const bodyEl = item.querySelector('.acc-body');
    head.addEventListener('click', () => {
      const isOpen = item.classList.contains('open');
      document.querySelectorAll('.acc-item').forEach(i => {
        i.classList.remove('open');
        i.querySelector('.acc-body').style.maxHeight = null;
      });
      if (!isOpen) {
        item.classList.add('open');
        bodyEl.style.maxHeight = bodyEl.scrollHeight + 'px';
      }
    });
  });

  // reveal
  const revealBtn = document.getElementById('revealBtn');
  const revealBox = document.getElementById('revealBox');
  revealBtn.addEventListener('click', () => {
    revealBox.classList.toggle('open');
    revealBtn.textContent = revealBox.classList.contains('open') ? '🕶️ Close the folder' : '🕶️ Open the folder';
  });

  // lessons checklist
  document.querySelectorAll('#lessonsList li').forEach(li => {
    li.addEventListener('click', () => li.classList.toggle('checked'));
  });

  // university data
  const unis = [
    {school:"Penn State University", program:"Energy, Environmental & Food Economics", status:"offer", steps:"Application → 1st Interview → 2nd Interview → Funded Offer → Accepted"},
    {school:"National University of Singapore", program:"Economics", status:"declined", steps:"Application → Interview → Funded Offer → Declined (chose Penn State)"},
    {school:"UC Santa Cruz", program:"Economics", status:"declined", steps:"Application → Interview → Oral Offer → Declined (research fit)"},
    {school:"University of Maryland", program:"Public Policy", status:"declined", steps:"Application → Funded Offer → Declined (chose Penn State)"},
    {school:"University of Georgia", program:"Agricultural & Applied Economics", status:"declined", steps:"Application → Admission → Funding Pending → Funded Offer → Declined"},
    {school:"Indiana University Bloomington", program:"Public Affairs", status:"declined", steps:"Application → Interview → Funded Offer → Declined"},
    {school:"University of New Mexico", program:"Economics", status:"declined", steps:"Application → Funded Offer → Declined"},
    {school:"Washington State University", program:"Economics", status:"declined", steps:"Application → Funded Offer → Declined"},
    {school:"University of Connecticut", program:"Agricultural & Resource Economics", status:"waitlist", steps:"Application → Admission → Funding Waitlist → Not pursued"},
    {school:"University of Florida", program:"Food & Resource Economics", status:"rejected", steps:"Application → Interview → Not admitted (advisor mismatch)"},
    {school:"University of Calgary", program:"Economics", status:"waitlist", steps:"Application → Funding Waitlist → Not pursued"},
    {school:"Georgia State University", program:"Economics", status:"waitlist", steps:"Application → Waitlist → Not pursued"},
  ];
  const badgeLabel = { offer:"Funded Offer", declined:"Declined by Me", waitlist:"Waitlist / Pending", rejected:"Not Admitted" };
  const grid = document.getElementById('uniGrid');

  function render(filter) {
    grid.innerHTML = '';
    unis.filter(u => filter === 'all' || u.status === filter).forEach(u => {
      const card = document.createElement('div');
      card.className = 'uni-card';
      card.innerHTML = `
        <span class="badge ${u.status}">${badgeLabel[u.status]}</span>
        <div class="school">${u.school}</div>
        <div class="program">${u.program}</div>
        <div class="journey-steps">${u.steps}</div>
      `;
      grid.appendChild(card);
    });
  }
  render('all');

  document.querySelectorAll('.chip').forEach(chip => {
    chip.addEventListener('click', () => {
      document.querySelectorAll('.chip').forEach(c => c.classList.remove('active'));
      chip.classList.add('active');
      render(chip.dataset.filter);
    });
  });
})();
</script>
</body>
</html>
