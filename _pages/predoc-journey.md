---
title: ""
permalink: /predoc-journey/
author_profile: true
---

<style>
  .pd-widget,
  .pd-page-tools{
    --pd-ink:#172033;
    --pd-muted:#667085;
    --pd-border:rgba(24,39,75,.12);
    --pd-blue:#2563eb;
    --pd-violet:#7c3aed;
    --pd-cyan:#0891b2;
    --pd-green:#15803d;
    --pd-amber:#b45309;
    --pd-red:#b42318;
    --pd-surface:#ffffff;
    --pd-soft:#f7f9fc;
    --pd-radius:18px;
    --pd-shadow:0 10px 30px rgba(30,41,59,.08);
    font-family:-apple-system,BlinkMacSystemFont,"Segoe UI","Noto Sans",Helvetica,Arial,sans-serif;
    color:var(--pd-ink);
  }

  html{ scroll-behavior:smooth; }

  .pd-hero{
    position:relative;
    overflow:hidden;
    margin:0 0 36px;
    padding:42px 36px;
    border-radius:24px;

    background:
        linear-gradient(135deg,#ffffff 0%,#fbfcff 55%,#f8faff 100%);

    border:1px solid rgba(37,99,235,.08);

    box-shadow:
        0 12px 35px rgba(15,23,42,.06);
}
 .pd-hero::after{
    content:"";
    position:absolute;
    inset:0;

    background:
      radial-gradient(circle at 90% 20%,
      rgba(37,99,235,.06),
      transparent 25%);

    pointer-events:none;
}
   .pd-hero h1{
    margin:0 0 12px;
    font-size:clamp(2rem,4vw,2.7rem);
    line-height:1.12;
    font-weight:800;
    letter-spacing:-0.03em;
    letter-spacing:-.035em;
    background:linear-gradient(90deg,var(--pd-blue),var(--pd-violet),var(--pd-cyan));
    -webkit-background-clip:text;
    background-clip:text;
    color:transparent;
  }
  .pd-hero p{ margin:0; color:var(--pd-muted); }

  .pd-widget b{ color:var(--pd-ink); }

  .pd-stats{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:14px;
    margin:24px 0 34px;
  }
  .pd-stat{
    position:relative;
    overflow:hidden;
    border:1px solid var(--pd-border);
    border-radius:var(--pd-radius);
    background:linear-gradient(180deg,#fff,#fbfcff);
    padding:20px 14px;
    text-align:center;
    box-shadow:0 6px 20px rgba(15,23,42,.05);
    transition:transform .22s ease,box-shadow .22s ease,border-color .22s ease;
  }
  .pd-stat::before{
    content:"";
    position:absolute;
    inset:0 0 auto;
    height:4px;
    background:linear-gradient(90deg,var(--pd-blue),var(--pd-violet),var(--pd-cyan));
  }
  .pd-stat:hover{
    transform:translateY(-5px);
    box-shadow:0 15px 32px rgba(30,41,59,.12);
    border-color:rgba(37,99,235,.28);
  }
  .pd-stat .pd-num{
    display:block;
    font-size:34px;
    font-weight:800;
    letter-spacing:-.03em;
    color:var(--pd-blue);
    line-height:1.05;
  }
  .pd-stat .pd-lbl{
    display:block;
    font-size:12px;
    color:var(--pd-muted);
    margin-top:7px;
    letter-spacing:.02em;
  }

  .pd-widget details{
    border:1px solid var(--pd-border);
    border-radius:16px;
    margin-bottom:11px;
    background:rgba(255,255,255,.92);
    padding:0;
    box-shadow:0 4px 16px rgba(15,23,42,.04);
    transition:border-color .2s ease,box-shadow .2s ease,transform .2s ease;
  }
  .pd-widget details:hover{
    transform:translateY(-1px);
    border-color:rgba(37,99,235,.26);
    box-shadow:0 9px 24px rgba(30,41,59,.08);
  }
  .pd-widget details[open]{
    border-color:rgba(124,58,237,.26);
    background:linear-gradient(180deg,#fff,#fbfaff);
  }
  .pd-widget summary{
    padding:15px 17px;
    cursor:pointer;
    font-weight:700;
    list-style:none;
    display:flex;
    align-items:center;
    gap:10px;
    border-radius:16px;
    transition:background .18s ease,color .18s ease;
  }
  .pd-widget summary::-webkit-details-marker{ display:none; }
  .pd-widget summary::before{
    content:"＋";
    display:grid;
    place-items:center;
    width:22px;height:22px;
    flex:0 0 22px;
    border-radius:50%;
    background:#eef4ff;
    color:var(--pd-blue);
    font-size:14px;
    transition:transform .2s ease,background .2s ease,color .2s ease;
  }
  .pd-widget details[open] summary::before{
    content:"−";
    transform:rotate(180deg);
    background:#f1ebff;
    color:var(--pd-violet);
  }
  .pd-widget summary:hover{
    background:linear-gradient(90deg,rgba(37,99,235,.055),rgba(124,58,237,.05));
  }
  .pd-widget .pd-details-body{
    padding:2px 18px 18px 50px;
    color:var(--pd-muted);
    font-size:14.8px;
    line-height:1.72;
    animation:pdFade .22s ease;
  }
  .pd-widget .pd-details-body p{ margin:0 0 11px; }
  .pd-widget .pd-details-body ul{ margin:0;padding-left:18px; }
  .pd-widget .pd-details-body li{ margin-bottom:7px; }

  .pd-controls{
    display:flex;
    align-items:center;
    gap:10px;
    flex-wrap:wrap;
    margin:18px 0 14px;
    padding:13px;
    border:1px solid var(--pd-border);
    border-radius:16px;
    background:linear-gradient(135deg,#fbfdff,#faf8ff);
  }
  .pd-search{
    flex:1 1 230px;
    min-width:0;
    border:1px solid var(--pd-border);
    border-radius:999px;
    padding:9px 14px;
    background:#fff;
    color:var(--pd-ink);
    outline:none;
    transition:border-color .2s ease,box-shadow .2s ease;
  }
  .pd-search:focus{
    border-color:rgba(37,99,235,.5);
    box-shadow:0 0 0 4px rgba(37,99,235,.09);
  }
  .pd-filters{
    display:flex;
    gap:8px;
    flex-wrap:wrap;
    margin:0;
  }
  .pd-chip{
    font-size:12px;
    padding:7px 12px;
    border-radius:999px;
    border:1px solid var(--pd-border);
    background:#fff;
    color:var(--pd-muted);
    cursor:pointer;
    transition:transform .15s ease,background .15s ease,color .15s ease,border-color .15s ease;
  }
  .pd-chip:hover{ transform:translateY(-1px);border-color:rgba(37,99,235,.3); }
  .pd-chip.active{
    background:linear-gradient(90deg,var(--pd-blue),var(--pd-violet));
    color:#fff;
    border-color:transparent;
    font-weight:700;
    box-shadow:0 5px 14px rgba(79,70,229,.2);
  }

  .pd-table-wrap{
    width:100%;
    overflow-x:auto;
    border:1px solid var(--pd-border);
    border-radius:16px;
    box-shadow:0 7px 22px rgba(15,23,42,.05);
  }
  .pd-table{
    width:100%;
    border-collapse:separate;
    border-spacing:0;
    font-size:14px;
    margin:0;
    background:#fff;
  }
  .pd-table th,.pd-table td{
    border:0;
    border-bottom:1px solid var(--pd-border);
    padding:11px 13px;
    text-align:left;
    vertical-align:top;
  }
  .pd-table th{
    position:sticky;
    top:0;
    z-index:1;
    background:linear-gradient(90deg,#eef5ff,#f5f0ff);
    font-weight:750;
    color:#344054;
  }
  .pd-table tr:last-child td{ border-bottom:0; }
  .pd-table tr[data-status]{
    transition:background .16s ease,transform .16s ease;
  }
  .pd-table tr[data-status]:hover{ background:#fafcff; }
  .pd-table tr.pd-hide{ display:none; }

  .pd-status{
    font-size:11px;
    padding:3px 8px;
    border-radius:999px;
    display:inline-block;
    font-weight:700;
  }
  .pd-status.offer{ background:#dcfce7;color:#166534; }
  .pd-status.declined{ background:#fff7ed;color:#9a3412; }
  .pd-status.waitlist{ background:#f1f5f9;color:#475569; }
  .pd-status.rejected{ background:#fee2e2;color:#991b1b; }

  .pd-progress{
    position:fixed;
    z-index:9999;
    left:0;top:0;
    width:0;
    height:4px;
    background:linear-gradient(90deg,var(--pd-blue),var(--pd-violet),var(--pd-cyan));
    box-shadow:0 1px 8px rgba(37,99,235,.28);
  }
  .pd-top{
    position:fixed;
    z-index:9998;
    right:18px;
    bottom:18px;
    width:44px;height:44px;
    border:0;
    border-radius:50%;
    background:linear-gradient(135deg,var(--pd-blue),var(--pd-violet));
    color:#fff;
    cursor:pointer;
    box-shadow:0 10px 24px rgba(37,99,235,.3);
    opacity:0;
    transform:translateY(12px);
    pointer-events:none;
    transition:opacity .2s ease,transform .2s ease;
  }
  .pd-top.show{
    opacity:1;
    transform:translateY(0);
    pointer-events:auto;
  }

  .pd-reveal{
    opacity:0;
    transform:translateY(14px);
    transition:opacity .55s ease,transform .55s ease;
  }
  .pd-reveal.pd-visible{
    opacity:1;
    transform:none;
  }

  @keyframes pdFade{
    from{ opacity:0;transform:translateY(-4px); }
    to{ opacity:1;transform:none; }
  }

  @media (max-width:720px){
    .pd-stats{ grid-template-columns:repeat(2,1fr); }
    .pd-hero{ padding:28px 18px 23px; }
    .pd-widget .pd-details-body{ padding-left:18px; }
    .pd-table{ min-width:760px; }
  }
  @media (max-width:420px){
    .pd-stats{ grid-template-columns:1fr 1fr;gap:10px; }
    .pd-stat{ padding:17px 8px; }
    .pd-stat .pd-num{ font-size:29px; }
  }
  @media (prefers-reduced-motion:reduce){
    html{ scroll-behavior:auto; }
    *,*::before,*::after{
      animation-duration:.01ms!important;
      animation-iteration-count:1!important;
      transition-duration:.01ms!important;
    }
    .pd-reveal{ opacity:1;transform:none; }
  }
</style>

<div align="center">

<h1>Welcome to My Pre-Doctoral Journey </h1>

<p><em>Hello • नमस्ते • 你好 • Hola </em></p>

</div>

This page documents my journey to entering a Ph.D. in Applied Economics—from building research experience and preparing my application to navigating interviews, offers, and ultimately choosing Penn State University.

During my application cycle, I received funded Ph.D. offers. Among them were offers from **Penn State University (EEFE)**, the **National University of Singapore (Economics)**, the **University of Georgia (Agricultural & Applied Economics)**, the **University of Maryland (Public Policy)**, and **Indiana University Bloomington (Public Affairs)**.

I hope this page serves as a useful resource for future applicants, especially those coming from non-traditional backgrounds. There is no single path to entering a Ph.D.— this was mine.

> ### 📍 At a Glance
>
> - 🎓 **Background:** B.Tech. Chemical Engineering and M.S. Applied Economics
> - 🔬 **Research:** 3+ years @ Center for Global Sustainability + 1 year @ World Bank
> - 📄 **Research Output:** Multiple co-authored journal articles + one solo research writing sample
> - 📨 **Application Cycle:** 37 applications → 7 funded Ph.D. offers (More details in the Application Statistics section)
> - 🏛️ **Final Destination:** Penn State University (EEFE)

<div class="pd-widget">
<div class="pd-stats">
  <div class="pd-stat"><span class="pd-num" data-target="37">37</span><span class="pd-lbl">Applications sent</span></div>
  <div class="pd-stat"><span class="pd-num" data-target="34">34</span><span class="pd-lbl">Reached a decision</span></div>
  <div class="pd-stat"><span class="pd-num" data-target="12">12</span><span class="pd-lbl">Positive outcomes</span></div>
  <div class="pd-stat"><span class="pd-num" data-target="7">7</span><span class="pd-lbl">Funded offers</span></div>
</div>
</div>

---

## Research Experience

After completing my M.S. in Applied Economics at the University of Maryland, I worked as a **Research Assistant** at the **Center for Global Sustainability** for over three years. Although not formally labelled a pre-doc, it functioned much like one: I worked closely with three faculties, Dr. Jiehong Lou, Dr. Mengye Zhu, and Jenna Behrendt, on research projects, developed independent research skills, and gained extensive experience in applied economics and public policy. My work focused on energy, equity, and climate policy, where I developed and sharpened my skillset and knowledge in econometrics, geospatial analysis, literature review, scientific writing, and research communication.

Alongside this, I worked for one year as a **Research Analyst Consultant** to a **Senior Economist at the World Bank**, contributing to research on agriculture in Sub-Saharan Africa. This experience further strengthened my empirical research, quantitative analysis, critical thinking, and policy evaluation skills.

During these years, I collaborated on several research projects, including a **second-authored journal article with Dr. Lou**, which was under revise-and-resubmit at _Energy Research & Social Science_ during my Ph.D. application cycle.

---

## My Application Beyond Research

### Academic Preparation

**B.Tech. Chemical Engineering**
*Dr. Babasaheb Ambedkar Technological University*

**Relevant Coursework:** Calculus, Linear Algebra, Differential Equations, Other Engineering Courses.

*I did not have formal coursework in Real Analysis.*

---

Following my engineering degree, I took **three years away from formal education** due to personal and family circumstances. During that time, I continued learning independently through **MITx** courses in **Probability, Statistics, and Microeconomics**, which helped strengthen my quantitative foundation before pursuing my M.S. in Applied Economics.

---

**M.S. Applied Economics**
*University of Maryland*

**Relevant Core:** Microeconomics, Macroeconomics, Econometrics.

**Relevant Field:** Environmental Economics, Development Economics, Program Evaluation, Game Theory.

---

### Other Important Components of My Application

<div class="pd-widget">

<details>
<summary>📚 GRE Quantitative: 160 😄</summary>
<div class="pd-details-body">
<p>Around the 50th percentile at the time... yep, certainly not the kind of score that makes admissions committees throw confetti 🎉. Everywhere I looked people seemed to be scoring <b>165+</b>, including several of my friends at Maryland, Cornell and Virginia Tech. Naturally, I thought, "One more attempt should do it..." So I took the GRE <b>four more times</b>. Still no at least 165. Jokes- 🤷‍♂️ On the bright side, every attempt ended with sushi 🍣 somewhere in the D.C. area, so I'm still not convinced I was taking the GRE... I may have just been reviewing sushi restaurants. 😅🍱</p>
</div>
</details>

<details>
<summary>📄 Research Writing Sample</summary>
<div class="pd-details-body">
<p>One <b>Solo-authored sample research paper</b> using causal inference methods. It was only <b>six pages long</b>, but it represented nearly <b>6–7 months</b> of work ⏳, plus about <b>10 pages of supplementary material</b> 📑. Those six pages ended up doing an incredible amount of heavy lifting—they came up in almost every interview 🎤 and probably had a stronger social life than I did. 😂</p>
</div>
</details>

<details>
<summary>✉️ Recommendation Letters</summary>
<div class="pd-details-body">
<ul>
<li>👨‍🔬👩‍🔬 Two research supervisors (a combination of supervisors from the <b>Center for Global Sustainability</b> and the <b>World Bank</b>, depending on whether the program was in Econ/ Ag Econ/ Public Policy). Great recommendation letters come from people who genuinely know your work, not necessarily the fanciest title.</li>
<li>🎓 One academic recommendation from faculty instructors in the University of Maryland's Applied Economics program🌟</li>
</ul>
</div>
</details>

<details>
<summary> 🧪 Secret Sauce</summary>
<div class="pd-details-body">
<p>No successful Ph.D. application is built alone. If my application had a secret sauce, it was the weekly mentorship I received from an economist working at Amazon (at the time... and maybe still there today). From my solo-authored research paper to mock interviews, he helped me build the strongest application possible. That mentorship taught me not only how to build a stronger application, but also how to think more critically as a researcher.</p>
<p><i>P.S. 🤫 His identity shall remain classified. Every applicant deserves to find their own secret sauce.</i></p>
</div>
</details>

</div>

---

### 📬 Reaching Out to Faculty

I reached out to only a handful of faculty members at Carnegie Mellon (Policy), Duke (UPEP), and the University of Maryland (Ag Econ), some of whom I had met during World Bank seminars. Although I was not admitted to those programmes, the conversations were extremely valuable. I received thoughtful feedback on my research interests and even my solo-authored research paper.

Interestingly, I did not reach out to faculty at other remaining universities that later admitted me, including Penn State, NUS, and the University of Georgia.

**My takeaway:** Reach out when there is a genuine research fit and a meaningful reason to connect. Better is to meet in-person if possible at seminars or conferences. In my experience, it helped much more with networking, feedback, and understanding research fit than with increasing admission chances.

---

## Outcome

### Application Statistics

Of the **37** Ph.D. applications I submitted, **34** reached a clear admissions outcome. Three applications remained unresolved due to delayed or no final decisions. Among those 34, **12** resulted in positive outcomes, with **7** ultimately converting into fully funded Ph.D. offers.

| Category | Count |
|-----------|------:|
| Applications Submitted | **37** |
| Applications with Final Outcomes | **34** |
| Positive Outcomes* | **12** |
| Fully Funded Ph.D. Offers | **7** |

*Success Rates**

- 🎯 **Positive Outcome Rate:** **35.3%** (12/34)
- 🎓 **Fully Funded Offer Rate:** **20.6%** (7/34)
- 🚀 **Conversion Rate (Positive Outcome → Fully Funded Offer):** **58.3%** (7/12)

*Positive outcomes include funded offers, admissions without funding, interviews, oral offers, and waitlists.

---

### Understanding the Admissions Process

One thing I learned during this application cycle is that Ph.D. admissions are rarely a simple **accept/reject** process. Depending on the department, an application may go through several stages, including faculty review, interviews, funding decisions, and final offers.

The table below summarizes the progression of my applications — 

<div class="pd-widget">
<div class="pd-filters" id="pdFilters">
  <button class="pd-chip active" data-filter="all">Positive Outcomes (12)</button>
</div>

<table class="pd-table" id="pdTable">
<tr><th>University</th><th>Programme</th><th>Application Journey</th></tr>
<tr data-status="offer"><td><b>Penn State University</b></td><td>Energy, Environmental & Food Economics</td><td>Application → 1st Interview → 2nd Interview → ✅ Funded Offer → <b>Accepted</b></td></tr>
<tr data-status="declined"><td><b>National University of Singapore</b></td><td>Economics</td><td>Application → Interview → ✅ Funded Offer → Declined (Chose Penn State)</td></tr>
<tr data-status="declined"><td><b>University of California, Santa Cruz</b></td><td>Economics</td><td>Application → Interview → Positive email follow-up from department → Withdrew before formal offer </td></tr>
<tr data-status="declined"><td><b>University of Maryland</b></td><td>Public Policy</td><td>Application → ✅ Funded Offer → Declined (Chose Penn State)</td></tr>
<tr data-status="declined"><td><b>University of Georgia</b></td><td>Agricultural & Applied Economics</td><td>Application → Admission → Funding Pending → ✅ Funded Offer → Declined (Chose Penn State)</td></tr>
<tr data-status="declined"><td><b>Indiana University Bloomington</b></td><td>Public Affairs</td><td>Application → Interview → ✅ Funded Offer → Declined (Chose Penn State)</td></tr>
<tr data-status="declined"><td><b>University of New Mexico</b></td><td>Economics</td><td>Application → ✅ Funded Offer → Declined (Chose Penn State)</td></tr>
<tr data-status="declined"><td><b>Washington State University</b></td><td>Economics</td><td>Application → ✅ Funded Offer → Declined (Chose Penn State)</td></tr>
<tr data-status="waitlist"><td><b>University of Connecticut</b></td><td>Agricultural & Resource Economics</td><td>Application → Admission → Funding Waitlist → Declined (Not Pursued)</td></tr>
<tr data-status="rejected"><td><b>University of Florida</b></td><td>Food & Resource Economics</td><td>Application → Interview → Not Admitted (Advisor mismatch)</td></tr>
<tr data-status="waitlist"><td><b>University of Calgary</b></td><td>Economics</td><td>Application → Funding Waitlist → Not Pursued</td></tr>
<tr data-status="waitlist"><td><b>Georgia State University</b></td><td>Economics</td><td>Application → Waitlist → Not Pursued <i>(No health insurance was a deal-breaker already😅)</i></td></tr>
</table>
</div>

<div class="pd-widget">
<details>
<summary>🎓 Rejections: The "Character Development"</summary>
<div class="pd-details-body">
<p>Every Ph.D. applicant has a rejection folder. Here's part of mine 😄: Stanford University (ESS), Duke University (UPEP), Carnegie Mellon University (Public Policy), Columbia University (Sustainable Development), Economics programmes at UC San Diego, UT Austin, and Michigan State, and Agricultural Economics programmes at the University of Maryland, UC Berkeley, UIUC, and UW–Madison. Additional universities reject exist but aren't necessary to list at this point</p>
</div>
</details>
</div>

<div class="pd-widget">
<details>
<summary>No Final Decision or very late beyond april decisons</summary>
<div class="pd-details-body">
<p>NC State University, Virginia Tech, Simon Fraser University (I did not follow up after receiving funded offers elsewhere).--- I lost 3 applications just like that and therefore some $$.</p>
</div>
</details>
</div>

---

### Interviews

One of the most enjoyable parts of my application cycle was the interviews. Most felt more like research conversations than formal interviews (NUS was the exception—it included questions on matrices and calculus 🤯).

To prepare, I brainstormed potential questions based on my research, Statement of Purpose, and CV, and compiled them into an interview preparation document. It served as a guide, not a script.

In the end, the interviews were less about memorised answers and more about discussing research ideas and demonstrating genuine interest. Looking back, a deep understanding of my research, writing sample, and prior projects mattered far more than rehearsed responses.

---

## Why Penn State?

After considering all of my offers, I ultimately chose **Penn State University's Energy, Environmental & Food Economics (EEFE)** program. My decision was primarily driven by research fit, primary advisor match, faculty interests, location, long-term career goals, and funding.

---

## Lessons Learned

- 🔬 **Research experience and writing sample mattered far more than I initially expected.** My research experience became the strongest part of my application, while my co-authored studies and six-page solo research paper carried much of my Statement of Purpose and featured and pitched for in almost every interview. Looking back, those mattered to me far more than a slightly higher GRE score.

- ✉️ **LOR** Great recommendation letters come from people who genuinely know your work— not necessarily the most famous names.

- 📄 **Mentorship is invaluable.** Constructive feedback from mentors significantly improved my research, statement of purpose, interviews, and overall application package.

- 🎯 **Prepare for interviews by understanding your own work, not by memorising answers.** My interview preparation document was a guide, but the actual interviews felt like research conversations rather than question-and-answer sessions.

- 📚 - 🎯 **Apply broadly, but apply strategically.** In my experience, the strongest applications were those where my past research, current interests, and future research agenda formed a coherent story that aligned well with the faculty and department. This is certainly subjective, but I found that staying true to my research trajectory was more valuable than trying to anticipate what admissions committees might want to see.
  
- 🚀 **Most importantly, there is no single path into a Ph.D.** Every applicant's journey is different, and success can come through many routes.

---

## Final Thoughts

If there is one message I hope readers take away from this page, it is this:

There is no single blueprint for getting into a Ph.D. programme. Build genuine research experience, stay curious, seek good mentors, and let your application tell a coherent story about who you are and the researcher you hope to become.

Finally, if you're reading this while preparing your own applications, I wish you the very best. I know how uncertain, stressful, and sometimes overwhelming the process can feel. Trust your journey, keep improving your craft, and remember that one decision does not define your worth or future.

**P.S. Potential Applicants: If you've actually read everything above... first of all, are you okay? 😄 Go grab a cup of tea ☕, coffee ☕, or matcha 🍵—you've earned it! Congratulations, you've officially reached the end. There isn't a hidden Google Drive, secret SOP, interview question bank, or a mythical "Guaranteed Ph.D. Admit" cheat code waiting below. Everything I'm willing to share is already on this page. The rest is left as an exercise for future applicants. 😉 Now close this tab, go work on your own application, and most importantly... find your own *secret sauce*. 🧪**

<p align="center">
<strong>Thank you • धन्यवाद • 谢谢 • Gracias</strong>
</p>

<script>
function pdInit(){
  try{
    var progress=document.createElement('div');
    progress.className='pd-progress pd-page-tools';
    document.body.appendChild(progress);

    var topBtn=document.createElement('button');
    topBtn.className='pd-top pd-page-tools';
    topBtn.type='button';
    topBtn.setAttribute('aria-label','Back to top');
    topBtn.innerHTML='↑';
    document.body.appendChild(topBtn);

    function updateScrollUI(){
      var doc=document.documentElement;
      var max=doc.scrollHeight-doc.clientHeight;
      var pct=max>0?(doc.scrollTop/max)*100:0;
      progress.style.width=pct+'%';
      topBtn.classList.toggle('show',doc.scrollTop>500);
    }
    window.addEventListener('scroll',updateScrollUI,{passive:true});
    topBtn.addEventListener('click',function(){window.scrollTo({top:0,behavior:'smooth'});});
    updateScrollUI();
  }catch(e){}

  try{
    var heroHeading=document.querySelector('div[align="center"] h1');
    if(heroHeading){
      var hero=heroHeading.parentElement;
      hero.classList.add('pd-hero','pd-widget');
    }
  }catch(e){}

  try{
    var nums=document.querySelectorAll('.pd-num');
    var counterObserver=new IntersectionObserver(function(entries,observer){
      entries.forEach(function(entry){
        if(!entry.isIntersecting)return;
        var el=entry.target;
        var target=parseInt(el.getAttribute('data-target'),10);
        if(isNaN(target))return;
        var start=null,duration=850;
        function animate(ts){
          if(!start)start=ts;
          var p=Math.min((ts-start)/duration,1);
          var eased=1-Math.pow(1-p,3);
          el.textContent=Math.round(target*eased);
          if(p<1)requestAnimationFrame(animate);
          else el.textContent=target;
        }
        requestAnimationFrame(animate);
        observer.unobserve(el);
      });
    },{threshold:.45});
    nums.forEach(function(el){counterObserver.observe(el);});
  }catch(e){}

  try{
    document.querySelectorAll('.pd-widget, h2, h3').forEach(function(el){
      el.classList.add('pd-reveal');
    });
    var revealObserver=new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if(entry.isIntersecting){
          entry.target.classList.add('pd-visible');
          revealObserver.unobserve(entry.target);
        }
      });
    },{threshold:.08,rootMargin:'0px 0px -30px 0px'});
    document.querySelectorAll('.pd-reveal').forEach(function(el){revealObserver.observe(el);});
  }catch(e){}

  try{
    var table=document.getElementById('pdTable');
    var originalFilters=document.getElementById('pdFilters');
    if(table && originalFilters){
      var labels={
        all:'All positive outcomes',
        offer:'Accepted',
        declined:'Other offers / withdrew',
        waitlist:'Waitlists',
        rejected:'Interview, not admitted'
      };
      originalFilters.innerHTML='';
      ['all','offer','declined','waitlist','rejected'].forEach(function(key){
        var count=key==='all'
          ? table.querySelectorAll('tr[data-status]').length
          : table.querySelectorAll('tr[data-status="'+key+'"]').length;
        if(key!=='all' && count===0)return;
        var btn=document.createElement('button');
        btn.className='pd-chip'+(key==='all'?' active':'');
        btn.type='button';
        btn.setAttribute('data-filter',key);
        btn.textContent=labels[key]+' ('+count+')';
        originalFilters.appendChild(btn);
      });

      var controls=document.createElement('div');
      controls.className='pd-controls';
      originalFilters.parentNode.insertBefore(controls,originalFilters);
      controls.appendChild(originalFilters);

      

      var wrap=document.createElement('div');
      wrap.className='pd-table-wrap';
      table.parentNode.insertBefore(wrap,table);
      wrap.appendChild(table);

      var activeFilter='all';
      var rows=table.querySelectorAll('tr[data-status]');

      function applyFilters(){
        var q="";
        rows.forEach(function(row){
          var statusOK=activeFilter==='all'||row.getAttribute('data-status')===activeFilter;
          var searchOK=!q||row.textContent.toLowerCase().indexOf(q)!==-1;
          row.classList.toggle('pd-hide',!(statusOK&&searchOK));
        });
      }

      originalFilters.querySelectorAll('.pd-chip').forEach(function(chip){
        chip.addEventListener('click',function(){
          originalFilters.querySelectorAll('.pd-chip').forEach(function(c){c.classList.remove('active');});
          chip.classList.add('active');
          activeFilter=chip.getAttribute('data-filter');
          applyFilters();
        });
      });

    }
  }catch(e){}

  try{
    document.querySelectorAll('#pdChecklist input[type="checkbox"]').forEach(function(box){
      box.addEventListener('change',function(){
        var li=box.closest('li');
        if(li)li.classList.toggle('pd-checked',box.checked);
      });
    });
  }catch(e){}
}

if(document.readyState==='loading'){
  document.addEventListener('DOMContentLoaded',pdInit);
}else{
  pdInit();
}
</script>
