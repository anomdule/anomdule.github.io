---
title: "Pre-Doctoral Journey"
permalink: /predoc-journey/
author_profile: true
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bangers&family=Bebas+Neue&family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@500&display=swap" rel="stylesheet">
<style>
  #predoc{
    --font-body: 'Inter', system-ui, sans-serif;
    --font-mono: 'JetBrains Mono', monospace;
    --radius: 14px;
    --bg: #0d1b2a;
    --bg-2: #10233a;
    --panel: #132a44;
    --primary: #e0281c;
    --secondary: #2e6fce;
    --accent: #f6f1e7;
    --text: #eef3f8;
    --text-dim: #b9c8d8;
    --line: rgba(255,255,255,0.12);
    --font-display: 'Bangers', cursive;
    --glow: rgba(224,40,28,0.35);
    background: radial-gradient(circle at 20% 0%, var(--bg-2), var(--bg) 60%);
    color: var(--text);
    font-family: var(--font-body);
    line-height: 1.65;
    border-radius: 20px;
    padding: 0 0 40px;
    margin: 20px 0;
    position: relative;
    overflow: hidden;
  }
  #predoc.theme-bat{
    --bg: #08090c;
    --bg-2: #101216;
    --panel: #16181d;
    --primary: #e8c14a;
    --secondary: #6b7280;
    --accent: #e8c14a;
    --text: #eceef1;
    --text-dim: #b7bcc4;
    --line: rgba(232,193,74,0.16);
    --font-display: 'Bebas Neue', sans-serif;
    --glow: rgba(232,193,74,0.28);
  }
  #predoc *{ box-sizing: border-box; }
  @media (prefers-reduced-motion: reduce){ #predoc *{ animation-duration:0.01ms !important; transition-duration:0.01ms !important; } }

  #predoc .bat-glow{
    position:fixed; width:340px; height:340px; border-radius:50%;
    background: radial-gradient(circle, var(--glow), transparent 70%);
    transform:translate(-50%,-50%); pointer-events:none; z-index:4; opacity:0; transition:opacity .3s ease;
  }
  #predoc .web-dot{
    position:fixed; width:6px; height:6px; border-radius:50%;
    background: var(--primary); opacity:0.7; pointer-events:none; z-index:4; box-shadow: 0 0 8px var(--glow);
  }
  #predoc .wrap{ max-width:920px; margin:0 auto; padding:0 24px; }

  #predoc .topbar{
    position:sticky; top:0; z-index:20; backdrop-filter: blur(10px);
    background: rgba(8,10,14,0.6); border-bottom:1px solid var(--line); border-radius:20px 20px 0 0;
  }
  #predoc .topbar-inner{ max-width:920px; margin:0 auto; padding:14px 24px; display:flex; align-items:center; justify-content:space-between; gap:16px; flex-wrap:wrap; }
  #predoc .brand{ font-family:var(--font-display); letter-spacing:0.5px; font-size:20px; color:var(--primary); }
  #predoc .toggle{ display:flex; align-items:center; gap:10px; font-family:var(--font-mono); font-size:11px; color:var(--text-dim); }
  #predoc .switch{ position:relative; width:60px; height:28px; border-radius:30px; background: var(--panel); border:1px solid var(--line); cursor:pointer; }
  #predoc .switch .knob{
    position:absolute; top:3px; left:3px; width:20px; height:20px; border-radius:50%; background: var(--primary);
    transition: left .35s cubic-bezier(.2,.9,.3,1.2), background .35s ease; display:flex; align-items:center; justify-content:center; font-size:11px;
  }
  #predoc.theme-bat .switch .knob{ left:37px; }

  #predoc .hero{ position:relative; padding:64px 0 40px; overflow:hidden; }
  #predoc .hero::before{
    content:""; position:absolute; inset:0; z-index:0; opacity:0.5;
    background-image:
      repeating-linear-gradient(60deg, var(--line) 0 1px, transparent 1px 90px),
      repeating-linear-gradient(-60deg, var(--line) 0 1px, transparent 1px 90px),
      repeating-linear-gradient(0deg, var(--line) 0 1px, transparent 1px 90px);
    mask-image: radial-gradient(circle at 30% 20%, black, transparent 70%);
  }
  #predoc.theme-bat .hero::before{ background-image: radial-gradient(circle at 25% 15%, var(--glow), transparent 45%); mask-image:none; }
  #predoc .eyebrow{ font-family:var(--font-mono); font-size:12px; letter-spacing:2px; text-transform:uppercase; color:var(--primary); display:inline-block; margin-bottom:14px; position:relative; z-index:1; }
  #predoc h1.title{ font-family:var(--font-display); font-size:clamp(36px, 7vw, 62px); line-height:1.05; margin:0 0 18px; color:var(--accent); position:relative; z-index:1; }
  #predoc.theme-bat h1.title{ text-shadow: 0 0 24px var(--glow); }
  #predoc .hero p{ max-width:640px; color:var(--text-dim); font-size:16.5px; position:relative; z-index:1; }
  #predoc .hero-tag{
    display:inline-flex; gap:8px; align-items:center; margin-top:18px; position:relative; z-index:1;
    font-family:var(--font-mono); font-size:12px; color:var(--text-dim); border:1px solid var(--line);
    padding:8px 14px; border-radius:30px; background:rgba(255,255,255,0.03);
  }
  #predoc .hero-tag b{ color:var(--primary); }

  #predoc .callout{
    border-left:3px solid var(--primary); padding:20px 24px; background:rgba(255,255,255,0.03);
    border-radius:0 var(--radius) var(--radius) 0; margin:32px 0; position:relative; z-index:1;
  }
  #predoc .callout h4{ margin:0 0 12px; font-family:var(--font-mono); font-size:13px; text-transform:uppercase; letter-spacing:1px; color:var(--primary); }
  #predoc .callout ul{ margin:0; padding-left:20px; color:var(--text-dim); }
  #predoc .callout li{ margin-bottom:6px; }
  #predoc .callout b{ color:var(--text); }

  #predoc .stats{ display:grid; grid-template-columns:repeat(4,1fr); gap:1px; background:var(--line); border:1px solid var(--line); border-radius:var(--radius); overflow:hidden; margin:40px 0 60px; }
  #predoc .stat{ background:var(--panel); padding:22px 14px; text-align:center; }
  #predoc .stat .num{ font-family:var(--font-display); font-size:34px; color:var(--primary); display:block; }
  #predoc .stat .lbl{ font-size:11px; color:var(--text-dim); text-transform:uppercase; letter-spacing:1px; margin-top:4px; }
  @media (max-width:640px){ #predoc .stats{ grid-template-columns:repeat(2,1fr); } }

  #predoc section{ padding:48px 0; border-top:1px solid var(--line); }
  #predoc .section-head{ display:flex; align-items:baseline; gap:14px; margin-bottom:22px; }
  #predoc .section-num{ font-family:var(--font-mono); color:var(--primary); font-size:13px; }
  #predoc h2{ font-family:var(--font-display); font-size:28px; margin:0; color:var(--accent); }
  #predoc h2 + p.lead{ color:var(--text-dim); max-width:640px; margin-top:-10px; }
  #predoc p{ color: var(--text-dim); }
  #predoc p b, #predoc li b, #predoc .t-detail b, #predoc .acc-body-inner b{ color: var(--text); }

  #predoc .timeline{ position:relative; margin-top:28px; padding-left:28px; }
  #predoc .timeline::before{ content:""; position:absolute; left:5px; top:6px; bottom:6px; width:2px; background: linear-gradient(var(--primary), var(--secondary)); opacity:0.5; }
  #predoc .t-item{ position:relative; padding:0 0 30px 20px; cursor:pointer; }
  #predoc .t-item:last-child{ padding-bottom:0; }
  #predoc .t-dot{ position:absolute; left:-28px; top:2px; width:12px; height:12px; border-radius:50%; background:var(--bg); border:2px solid var(--primary); transition: all .25s ease; }
  #predoc .t-item.active .t-dot{ background:var(--primary); box-shadow:0 0 12px var(--glow); transform:scale(1.2); }
  #predoc .t-year{ font-family:var(--font-mono); font-size:11px; color:var(--primary); text-transform:uppercase; letter-spacing:1px; }
  #predoc .t-title{ font-weight:700; font-size:16px; margin:2px 0 6px; color:var(--text); }
  #predoc .t-detail{ color:var(--text-dim); font-size:14.5px; max-height:0; overflow:hidden; transition: max-height .4s ease; }
  #predoc .t-item.active .t-detail{ max-height:600px; }

  #predoc .acc-item{ border:1px solid var(--line); border-radius:var(--radius); margin-bottom:10px; overflow:hidden; background:var(--panel); }
  #predoc .acc-head{ padding:16px 20px; display:flex; justify-content:space-between; align-items:center; cursor:pointer; font-weight:700; }
  #predoc .acc-head .plus{ color:var(--primary); font-family:var(--font-mono); transition:transform .3s ease; flex-shrink:0; margin-left:10px; }
  #predoc .acc-item.open .plus{ transform:rotate(45deg); }
  #predoc .acc-body{ max-height:0; overflow:hidden; transition:max-height .45s ease; }
  #predoc .acc-body-inner{ padding:0 20px 18px; color:var(--text-dim); font-size:14.5px; }
  #predoc .acc-body-inner ul{ padding-left:20px; }
  #predoc .acc-body-inner li{ margin-bottom:6px; }

  #predoc .stat-table{ width:100%; border-collapse:collapse; margin:24px 0; font-size:14.5px; }
  #predoc .stat-table th, #predoc .stat-table td{ padding:10px 14px; border:1px solid var(--line); text-align:left; }
  #predoc .stat-table th{ color:var(--primary); font-family:var(--font-mono); font-size:12px; text-transform:uppercase; }
  #predoc .rate-list{ padding-left:0; list-style:none; }
  #predoc .rate-list li{ margin-bottom:8px; }
  #predoc .footnote{ font-size:13px; font-style:italic; color:var(--text-dim); opacity:0.85; }

  #predoc .filters{ display:flex; gap:8px; flex-wrap:wrap; margin-bottom:20px; }
  #predoc .chip{ font-family:var(--font-mono); font-size:12px; padding:8px 14px; border-radius:30px; border:1px solid var(--line); color:var(--text-dim); cursor:pointer; background:transparent; transition:.2s ease; }
  #predoc .chip.active{ background:var(--primary); color:var(--bg); border-color:var(--primary); font-weight:700; }
  #predoc .uni-grid{ display:grid; grid-template-columns:repeat(auto-fill, minmax(250px,1fr)); gap:14px; }
  #predoc .uni-card{ border:1px solid var(--line); background:var(--panel); border-radius:var(--radius); padding:18px; transition:.25s ease; }
  #predoc .uni-card:hover{ border-color:var(--primary); transform:translateY(-2px); }
  #predoc .uni-card .school{ font-weight:700; font-size:15px; color:var(--text); }
  #predoc .uni-card .program{ color:var(--text-dim); font-size:13px; margin:2px 0 12px; }
  #predoc .badge{ display:inline-block; font-size:11px; font-family:var(--font-mono); padding:3px 9px; border-radius:20px; margin-bottom:10px; }
  #predoc .badge.offer{ background:rgba(46,150,90,0.18); color:#5fd18a; }
  #predoc .badge.declined{ background:rgba(224,40,28,0.15); color:var(--primary); }
  #predoc .badge.rejected{ background:rgba(150,150,150,0.18); color:#c2c2c2; }
  #predoc .badge.waitlist{ background:rgba(232,193,74,0.18); color:#e8c14a; }
  #predoc .journey-steps{ font-size:13px; color:var(--text-dim); line-height:1.8; }
  #predoc .no-decision-note{ margin-top:20px; padding:16px 20px; border:1px dashed var(--line); border-radius:var(--radius); font-size:14px; color:var(--text-dim); }

  #predoc .reveal-btn{ font-family:var(--font-mono); font-size:13px; background:var(--panel); color:var(--primary); border:1px solid var(--line); padding:10px 18px; border-radius:30px; cursor:pointer; }
  #predoc .reveal-box{ max-height:0; overflow:hidden; transition:max-height .5s ease; margin-top:16px; }
  #predoc .reveal-box.open{ max-height:400px; }

  #predoc .lessons{ list-style:none; padding:0; margin:0; display:grid; gap:10px; }
  #predoc .lessons li{ display:flex; gap:12px; align-items:flex-start; padding:14px 16px; border:1px solid var(--line); border-radius:var(--radius); background:var(--panel); cursor:pointer; transition:.2s ease; }
  #predoc .lessons li:hover{ border-color:var(--primary); }
  #predoc .lessons li .box{ flex:0 0 18px; height:18px; width:18px; border:2px solid var(--primary); border-radius:4px; margin-top:2px; display:flex; align-items:center; justify-content:center; font-size:12px; color:var(--bg); }
  #predoc .lessons li.checked .box{ background:var(--primary); }
  #predoc .lessons li.checked span.txt{ text-decoration:line-through; color:var(--text-dim); }
  #predoc .lessons span.txt{ color: var(--text); }

  #predoc footer{ text-align:center; padding:50px 24px 10px; color:var(--text-dim); font-size:13px; font-family:var(--font-mono); }
  #predoc a{ color:var(--primary); }
</style>

<div id="predoc">
  <div class="bat-glow" id="predocGlow"></div>

  <nav class="topbar">
    <div class="topbar-inner">
      <div class="brand">PhD // Origin Story</div>
      <div class="toggle">
        <span>🕸️ Web-Slinger</span>
        <div class="switch" id="predocSwitch"><div class="knob" id="predocKnob">🕸️</div></div>
        <span>🦇 Dark Knight</span>
      </div>
    </div>
  </nav>

  <header class="hero">
    <div class="wrap">
      <span class="eyebrow">Chemical Engineering → Applied Economics</span>
      <h1 class="title">Every Hero Has an Origin Story.</h1>
      <p>This page documents my journey to entering a Ph.D. in Applied Economics—from building research experience and preparing my application to navigating interviews, offers, and ultimately choosing Penn State University.</p>
      <p>During my application cycle, I received <b>funded Ph.D. offers</b>. Among them were offers from <b>Penn State University (EEFE)</b>, the <b>National University of Singapore (Economics)</b>, the <b>University of Georgia (Agricultural &amp; Applied Economics)</b>, the <b>University of Maryland (Public Policy)</b>, and <b>Indiana University Bloomington (Public Affairs)</b>.</p>
      <p>I hope this page serves as a useful resource for future applicants, especially those coming from non-traditional backgrounds. There is no single path to entering a Ph.D.—this was mine.</p>
      <div class="callout">
        <h4>📍 At a Glance</h4>
        <ul>
          <li>🎓 <b>Background:</b> Chemical Engineering → Applied Economics</li>
          <li>🔬 <b>Research:</b> 3+ years @ Center for Global Sustainability + 1 year @ World Bank</li>
          <li>📄 <b>Research Output:</b> Solo-authored causal inference paper + multiple co-authored studies</li>
          <li>📨 <b>Application Cycle:</b> 37 applications → 7 funded Ph.D. offers</li>
          <li>🏛️ <b>Final Destination:</b> Penn State University (EEFE)</li>
        </ul>
      </div>
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

    <section id="predoc-origin">
      <div class="section-head"><span class="section-num">01</span><h2>Research Experience Before the Ph.D.</h2></div>
      <p class="lead">Click a milestone to expand it.</p>
      <div class="timeline" id="predocTimeline">
        <div class="t-item active">
          <div class="t-dot"></div>
          <div class="t-year">B.Tech</div>
          <div class="t-title">Chemical Engineering — Dr. Babasaheb Ambedkar Technological University</div>
          <div class="t-detail">
            <p><b>Relevant Coursework:</b> Calculus, Linear Algebra, Differential Equations.</p>
            <p><i>I did not have formal coursework in Real Analysis. Contrary to popular belief, that wasn't the end of the world for me. 😄</i></p>
          </div>
        </div>
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-year">Gap Years</div>
          <div class="t-title">Three years away from formal education</div>
          <div class="t-detail">
            <p>Following my engineering degree, I took <b>three years away from formal education</b> due to personal and family circumstances. During that time, I continued learning independently through <b>MITx</b> courses in <b>Probability, Statistics, and Microeconomics</b>, which helped strengthen my quantitative foundation before pursuing my M.S. in Applied Economics.</p>
          </div>
        </div>
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-year">M.S.</div>
          <div class="t-title">Applied Economics — University of Maryland</div>
          <div class="t-detail">
            <p><b>Relevant Core:</b> Microeconomics, Macroeconomics, Econometrics.</p>
            <p><b>Relevant Field:</b> Environmental Economics, Development Economics, Program Evaluation, Game Theory.</p>
          </div>
        </div>
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-year">3+ Years</div>
          <div class="t-title">Research Assistant — Center for Global Sustainability</div>
          <div class="t-detail">
            <p>After completing my M.S. in Applied Economics at the University of Maryland, I worked as a <b>Research Assistant</b> at the <b>Center for Global Sustainability</b> for over three years. Although my position was not formally labelled a pre-doctoral fellowship, it functioned much like one: I worked closely with faculty on research projects, developed independent research skills, and gained extensive experience in empirical economic research.</p>
            <p>My work focused on <b>energy, equity, transportation, and climate policy</b>, where I developed skills in <b>econometrics, causal inference, geospatial analysis, literature review, scientific writing, and research communication</b>.</p>
          </div>
        </div>
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-year">1 Year</div>
          <div class="t-title">Research Analyst Consultant — World Bank</div>
          <div class="t-detail">
            <p>Alongside this, I worked for one year as a <b>Research Analyst Consultant</b> to a <b>Senior Economist at the World Bank</b>, contributing to research on agriculture in <b>Sub-Saharan Africa</b>. This experience further strengthened my empirical research, quantitative analysis, critical thinking, and policy evaluation skills.</p>
          </div>
        </div>
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-year">Alongside</div>
          <div class="t-title">Co-authored research</div>
          <div class="t-detail">
            <p>During these years, I collaborated on several research projects, including a <b>second-authored journal article with Jiehong Lou</b>, which was <b>under revise-and-resubmit at Environmental Research &amp; Social Science during my Ph.D. application cycle</b>.</p>
          </div>
        </div>
        <div class="t-item">
          <div class="t-dot"></div>
          <div class="t-year">Now</div>
          <div class="t-title">Ph.D. candidate — Penn State University (EEFE)</div>
          <div class="t-detail">
            <p>After considering all of my offers, I ultimately chose Penn State University's Energy, Environmental &amp; Food Economics (EEFE) program.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="predoc-builder">
      <div class="section-head"><span class="section-num">02</span><h2>Building My Application Beyond Research</h2></div>
      <p class="lead">Tap each card to open it.</p>
      <div id="predocAccordion">
        <div class="acc-item">
          <div class="acc-head">📚 GRE Quantitative: 160 😄 <span class="plus">+</span></div>
          <div class="acc-body"><div class="acc-body-inner">
            <p>Around the 50th percentile at the time... yep, not exactly the score Reddit wanted me to have. Everywhere I looked people seemed to be scoring <b>165+</b>, including several of my friends at Maryland, Cornell and Virginia Tech. Naturally, I thought, "One more attempt should do it..." So I took the GRE <b>four more times</b>. Still no 165. 🤷‍♂️ On the bright side, every attempt ended with sushi 🍣 somewhere in the D.C. area, so I'm still not convinced I was taking the GRE... I may have just been reviewing sushi restaurants. 😅🍱</p>
          </div></div>
        </div>
        <div class="acc-item">
          <div class="acc-head">📄 Research Writing Sample <span class="plus">+</span></div>
          <div class="acc-body"><div class="acc-body-inner">
            <p>One <b>solo-authored empirical research paper</b> using causal inference methods. It was only <b>six pages long</b>, but it represented nearly <b>6–7 months</b> of work ⏳, plus about <b>10 pages of supplementary material</b> 📑. Those six pages ended up doing an incredible amount of heavy lifting—they came up in almost every interview 🎤 and probably had a stronger social life than I did. 😂</p>
          </div></div>
        </div>
        <div class="acc-item">
          <div class="acc-head">✉️ Recommendation Letters <span class="plus">+</span></div>
          <div class="acc-body"><div class="acc-body-inner">
            <ul>
              <li>👨‍🔬👩‍🔬 Two research supervisors (a combination of supervisors from the <b>Center for Global Sustainability</b> and the <b>World Bank</b>, depending on whether the programme was in Economics or Public Policy).</li>
              <li>🎓 One academic recommendation from <b>instructors</b> in the University of Maryland's Applied Economics program. <i>(Yes—instructors, not professors! 😄 Great recommendation letters come from people who genuinely know your work, not necessarily the fanciest title.)</i> 🌟</li>
            </ul>
          </div></div>
        </div>
        <div class="acc-item">
          <div class="acc-head">🌶️ Secret Sauce <span class="plus">+</span></div>
          <div class="acc-body"><div class="acc-body-inner">
            <p>No successful Ph.D. application is built alone. If my application had a secret sauce, it was the <b>weekly mentorship</b> I received from an economist working at <b>Amazon</b> (at the time... and maybe still there today). From my solo-authored research paper and Statement of Purpose to CV reviews, school selection, and mock interviews, he invested an incredible amount of time helping me build the strongest application possible. I owe a great deal of my application's success to his guidance, which taught me not only how to build a stronger application but also how to think more critically as a researcher.</p>
            <p><i>P.S. 🤫 His identity shall remain classified. Every applicant deserves to find their own secret sauce.</i></p>
          </div></div>
        </div>
      </div>
    </section>

    <section id="predoc-outcome">
      <div class="section-head"><span class="section-num">03</span><h2>Outcome</h2></div>
      <p>Of the <b>37</b> Ph.D. applications I submitted, <b>34</b> reached a clear admissions outcome. Three applications remained unresolved due to delayed or no final decisions. Among those 34, <b>12</b> resulted in positive outcomes, with <b>7</b> ultimately converting into fully funded Ph.D. offers.</p>
      <table class="stat-table">
        <tr><th>Category</th><th>Count</th></tr>
        <tr><td>Applications Submitted</td><td><b>37</b></td></tr>
        <tr><td>Applications with Final Outcomes</td><td><b>34</b></td></tr>
        <tr><td>Positive Outcomes*</td><td><b>12</b></td></tr>
        <tr><td>Fully Funded Ph.D. Offers</td><td><b>7</b></td></tr>
      </table>
      <p><b>Success Rates**</b></p>
      <ul class="rate-list">
        <li>🎯 <b>Positive Outcome Rate:</b> 35.3% (12/34)</li>
        <li>🎓 <b>Fully Funded Offer Rate:</b> 20.6% (7/34)</li>
        <li>🚀 <b>Conversion Rate (Positive Outcome → Fully Funded Offer):</b> 58.3% (7/12)</li>
      </ul>
      <p class="footnote">*Positive outcomes include funded offers, admissions without funding, interviews, oral offers, and waitlists.</p>
    </section>

    <section id="predoc-map">
      <div class="section-head"><span class="section-num">04</span><h2>Understanding the Admissions Process</h2></div>
      <p>One thing I learned during this application cycle is that Ph.D. admissions are rarely a simple <b>accept/reject</b> process. Depending on the department, an application may go through several stages, including faculty review, interviews, funding decisions, and final offers. The table below summarizes the progression of my applications — filter it by how each story ended.</p>
      <div class="filters" id="predocFilters">
        <button class="chip active" data-filter="all">All (12)</button>
        <button class="chip" data-filter="offer">Funded Offers (7)</button>
        <button class="chip" data-filter="declined">Declined by Me</button>
        <button class="chip" data-filter="waitlist">Waitlist / Pending</button>
        <button class="chip" data-filter="rejected">Not Admitted</button>
      </div>
      <div class="uni-grid" id="predocUniGrid"></div>
      <div class="no-decision-note">
        <b>No Final Decision or very late beyond April decisions:</b> NC State University, Virginia Tech, Simon Fraser University (I did not follow up after receiving funded offers elsewhere). I lost 3 applications just like that and some $$.
      </div>
    </section>

    <section id="predoc-rejections">
      <div class="section-head"><span class="section-num">05</span><h2>🎓 Rejections: The "Character Development" Section</h2></div>
      <p class="lead">Every Ph.D. applicant has a rejection folder. Here's part of mine 😄:</p>
      <button class="reveal-btn" id="predocRevealBtn">🕶️ Open the folder</button>
      <div class="reveal-box" id="predocRevealBox">
        <p>Stanford University (ESS), Duke University (UPEP), Carnegie Mellon University (Public Policy), Columbia University (Sustainable Development), Economics programmes at UC San Diego, UT Austin, and Michigan State, and Agricultural Economics programmes at the University of Maryland, UC Berkeley, UIUC, and UW–Madison.</p>
      </div>
    </section>

    <section id="predoc-interviews">
      <div class="section-head"><span class="section-num">06</span><h2>Interviews</h2></div>
      <p>One of the most enjoyable parts of the application cycle was the interviews. Most of them felt much more like research conversations than formal interviews. Faculty were generally interested in discussing my research experiences, future ideas, and overall fit with the department rather than asking technical questions. Looking back, I think thorough preparation for my research paper, statement of purpose, and prior projects mattered far more than memorising answers to interview questions.</p>
    </section>

    <section id="predoc-why">
      <div class="section-head"><span class="section-num">07</span><h2>Why Penn State?</h2></div>
      <p>After considering all of my offers, I ultimately chose <b>Penn State University's Energy, Environmental &amp; Food Economics (EEFE)</b> program. My decision was primarily driven by <b>research fit</b>, faculty interests, long-term career goals, funding, and the opportunity to work in energy, environmental, and applied economics within an interdisciplinary department.</p>
    </section>

    <section id="predoc-lessons">
      <div class="section-head"><span class="section-num">08</span><h2>Lessons Learned</h2></div>
      <p class="lead">Check them off as you internalize them.</p>
      <ul class="lessons" id="predocLessons">
        <li><div class="box">✓</div><span class="txt">Research experience mattered far more than I initially expected.</span></li>
        <li><div class="box">✓</div><span class="txt">A strong research writing sample can open more doors than a slightly higher GRE score.</span></li>
        <li><div class="box">✓</div><span class="txt">Great recommendation letters come from people who genuinely know your work—not necessarily the most famous names.</span></li>
        <li><div class="box">✓</div><span class="txt">Mentorship is invaluable.</span></li>
        <li><div class="box">✓</div><span class="txt">Apply broadly, but apply strategically.</span></li>
        <li><div class="box">✓</div><span class="txt">Most importantly, there is no single path into a Ph.D.</span></li>
      </ul>
    </section>

    <section id="predoc-final">
      <div class="section-head"><span class="section-num">09</span><h2>Final Thoughts</h2></div>
      <p>If this page helps even one applicant realise that there is no single blueprint for getting into a Ph.D. programme, then it has served its purpose.</p>
      <p>If you're currently preparing your own applications, I wish you the very best. Good luck! 🚀</p>
    </section>
  </div>

  <footer>Built to help the next non-traditional applicant find their own path.</footer>
</div>

<script>
(function(){
  const root = document.getElementById('predoc');
  const themeSwitch = document.getElementById('predocSwitch');
  const knob = document.getElementById('predocKnob');
  const glow = document.getElementById('predocGlow');
  let isBat = false;

  themeSwitch.addEventListener('click', () => {
    isBat = !isBat;
    root.classList.toggle('theme-bat', isBat);
    knob.textContent = isBat ? '🦇' : '🕸️';
    glow.style.opacity = isBat ? '1' : '0';
  });

  root.addEventListener('mousemove', (e) => {
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

  const stats = root.querySelectorAll('.stat .num');
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

  root.querySelectorAll('.t-item').forEach(item => {
    item.addEventListener('click', () => {
      const wasActive = item.classList.contains('active');
      root.querySelectorAll('.t-item').forEach(i => i.classList.remove('active'));
      if (!wasActive) item.classList.add('active');
    });
  });

  root.querySelectorAll('.acc-item').forEach(item => {
    const head = item.querySelector('.acc-head');
    const bodyEl = item.querySelector('.acc-body');
    head.addEventListener('click', () => {
      const isOpen = item.classList.contains('open');
      root.querySelectorAll('.acc-item').forEach(i => {
        i.classList.remove('open');
        i.querySelector('.acc-body').style.maxHeight = null;
      });
      if (!isOpen) {
        item.classList.add('open');
        bodyEl.style.maxHeight = bodyEl.scrollHeight + 'px';
      }
    });
  });

  const revealBtn = document.getElementById('predocRevealBtn');
  const revealBox = document.getElementById('predocRevealBox');
  revealBtn.addEventListener('click', () => {
    revealBox.classList.toggle('open');
    revealBtn.textContent = revealBox.classList.contains('open') ? '🕶️ Close the folder' : '🕶️ Open the folder';
  });

  root.querySelectorAll('#predocLessons li').forEach(li => {
    li.addEventListener('click', () => li.classList.toggle('checked'));
  });

  const unis = [
    {school:"Penn State University", program:"Energy, Environmental & Food Economics", status:"offer", steps:"Application → 1st Interview → 2nd Interview → ✅ Funded Offer → Accepted"},
    {school:"National University of Singapore", program:"Economics", status:"declined", steps:"Application → Interview → ✅ Funded Offer → Declined (Chose Penn State)"},
    {school:"University of California, Santa Cruz", program:"Economics", status:"declined", steps:"Application → Interview → Oral Offer → Declined (Penn State was the better research fit)"},
    {school:"University of Maryland", program:"Public Policy", status:"declined", steps:"Application → ✅ Funded Offer → Declined (Chose Penn State)"},
    {school:"University of Georgia", program:"Agricultural & Applied Economics", status:"declined", steps:"Application → Admission → Funding Pending → ✅ Funded Offer → Declined (Chose Penn State)"},
    {school:"Indiana University Bloomington", program:"Public Affairs", status:"declined", steps:"Application → Interview → ✅ Funded Offer → Declined (Chose Penn State)"},
    {school:"University of New Mexico", program:"Economics", status:"declined", steps:"Application → ✅ Funded Offer → Declined (Chose Penn State)"},
    {school:"Washington State University", program:"Economics", status:"declined", steps:"Application → ✅ Funded Offer → Declined (Chose Penn State)"},
    {school:"University of Connecticut", program:"Agricultural & Resource Economics", status:"waitlist", steps:"Application → Admission → Funding Waitlist → Declined (Not Pursued)"},
    {school:"University of Florida", program:"Food & Resource Economics", status:"rejected", steps:"Application → Interview → Not Admitted (Advisor mismatch)"},
    {school:"University of Calgary", program:"Economics", status:"waitlist", steps:"Application → Funding Waitlist → Not Pursued"},
    {school:"Georgia State University", program:"Economics", status:"waitlist", steps:"Application → Waitlist → Not Pursued (No health insurance was a deal-breaker already😅)"},
  ];
  const badgeLabel = { offer:"Funded Offer", declined:"Declined by Me", waitlist:"Waitlist / Pending", rejected:"Not Admitted" };
  const grid = document.getElementById('predocUniGrid');

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

  root.querySelectorAll('.chip').forEach(chip => {
    chip.addEventListener('click', () => {
      root.querySelectorAll('.chip').forEach(c => c.classList.remove('active'));
      chip.classList.add('active');
      render(chip.dataset.filter);
    });
  });
})();
</script>
