---
title: "Pre-Doctoral Journey"
permalink: /predoc-journey/
author_profile: true
---

<style>
  .pd-widget{
    --gh-border: #d0d7de;
    --gh-fg: #1f2328;
    --gh-fg-muted: #656d76;
    --gh-accent: #0969da;
    --gh-bg-subtle: #f6f8fa;
    --gh-radius: 6px;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Noto Sans", Helvetica, Arial, sans-serif;
    color: var(--gh-fg);
  }
  .pd-widget b{ color: var(--gh-fg); }

  /* stat strip */
  .pd-stats{
    display:grid; grid-template-columns:repeat(4,1fr); gap:12px;
    margin: 24px 0 32px;
  }
  .pd-stat{
    border:1px solid var(--gh-border); border-radius:var(--gh-radius);
    background:#fff; padding:16px 12px; text-align:center;
  }
  .pd-stat .pd-num{ display:block; font-size:28px; font-weight:700; color:var(--gh-accent); line-height:1.1;}
  .pd-stat .pd-lbl{ font-size:12px; color:var(--gh-fg-muted); margin-top:4px;}
  @media (max-width:560px){ .pd-stats{ grid-template-columns:repeat(2,1fr);} }

  /* details/summary */
  .pd-widget details{
    border:1px solid var(--gh-border); border-radius:var(--gh-radius);
    margin-bottom:8px; background:#fff; padding:0;
  }
  .pd-widget summary{
    padding:12px 16px; cursor:pointer; font-weight:600; list-style:none;
    display:flex; align-items:center; gap:8px;
  }
  .pd-widget summary::-webkit-details-marker{ display:none; }
  .pd-widget summary::before{
    content:"▸"; color:var(--gh-fg-muted); font-size:12px; transition:transform .15s ease;
  }
  .pd-widget details[open] summary::before{ transform:rotate(90deg); }
  .pd-widget summary:hover{ background:var(--gh-bg-subtle); }
  .pd-widget .pd-details-body{
    padding:2px 16px 16px 34px; color:var(--gh-fg-muted); font-size:14.5px; line-height:1.65;
  }
  .pd-widget .pd-details-body p{ margin:0 0 10px; }
  .pd-widget .pd-details-body ul{ margin:0; padding-left:18px;}
  .pd-widget .pd-details-body li{ margin-bottom:6px;}

  /* filter chips + table */
  .pd-filters{ display:flex; gap:8px; flex-wrap:wrap; margin:16px 0; }
  .pd-chip{
    font-size:12px; padding:5px 12px; border-radius:16px; border:1px solid var(--gh-border);
    background:#fff; color:var(--gh-fg-muted); cursor:pointer;
  }
  .pd-chip.active{ background:var(--gh-accent); color:#fff; border-color:var(--gh-accent); font-weight:600;}
  .pd-table{ width:100%; border-collapse:collapse; font-size:14px; margin-bottom:8px;}
  .pd-table th, .pd-table td{ border:1px solid var(--gh-border); padding:8px 12px; text-align:left; vertical-align:top;}
  .pd-table th{ background:var(--gh-bg-subtle); font-weight:600;}
  .pd-table tr.pd-hide{ display:none;}
  .pd-status{ font-size:11px; padding:2px 8px; border-radius:12px; display:inline-block; font-weight:600;}
  .pd-status.offer{ background:#dafbe1; color:#116329;}
  .pd-status.declined{ background:#fff1e5; color:#9a6700;}
  .pd-status.waitlist{ background:#f6f8fa; color:#656d76;}
  .pd-status.rejected{ background:#ffebe9; color:#82071e;}

  /* checklist */
  .pd-checklist{ list-style:none; padding:0; margin:0; }
  .pd-checklist li{ display:flex; gap:10px; align-items:flex-start; padding:8px 0; border-bottom:1px solid var(--gh-border);}
  .pd-checklist li:last-child{ border-bottom:none;}
  .pd-checklist input{ margin-top:3px; }
  .pd-checklist label{ cursor:pointer; }
  .pd-checklist li.pd-checked label{ text-decoration:line-through; color:var(--gh-fg-muted);}
</style>

## Introduction

This page documents my journey to entering a Ph.D. in Applied Economics—from building research experience and preparing my application to navigating interviews, offers, and ultimately choosing Penn State University.

During my application cycle, I received **funded Ph.D. offers**. Among them were offers from **Penn State University (EEFE)**, the **National University of Singapore (Economics)**, the **University of Georgia (Agricultural & Applied Economics)**, the **University of Maryland (Public Policy)**, and **Indiana University Bloomington (Public Affairs)**.

I hope this page serves as a useful resource for future applicants, especially those coming from non-traditional backgrounds. There is no single path to entering a Ph.D.—this was mine.

> ### 📍 At a Glance
>
> - 🎓 **Background:** Chemical Engineering → Applied Economics
> - 🔬 **Research:** 3+ years @ Center for Global Sustainability + 1 year @ World Bank
> - 📄 **Research Output:** Solo-authored causal inference paper + multiple co-authored studies
> - 📨 **Application Cycle:** 37 applications → 7 funded Ph.D. offers
> - 🏛️ **Final Destination:** Penn State University (EEFE)

<div class="pd-widget">
<div class="pd-stats">
  <div class="pd-stat"><span class="pd-num" data-target="37">0</span><span class="pd-lbl">Applications sent</span></div>
  <div class="pd-stat"><span class="pd-num" data-target="34">0</span><span class="pd-lbl">Reached a decision</span></div>
  <div class="pd-stat"><span class="pd-num" data-target="12">0</span><span class="pd-lbl">Positive outcomes</span></div>
  <div class="pd-stat"><span class="pd-num" data-target="7">0</span><span class="pd-lbl">Funded offers</span></div>
</div>
</div>

---

## Research Experience Before the Ph.D.

After completing my M.S. in Applied Economics at the University of Maryland, I worked as a **Research Assistant** at the **Center for Global Sustainability** for over three years. Although my position was not formally labelled a pre-doctoral fellowship, it functioned much like one: I worked closely with faculty on research projects, developed independent research skills, and gained extensive experience in empirical economic research.

My work focused on **energy, equity, transportation, and climate policy**, where I developed skills in **econometrics, causal inference, geospatial analysis, literature review, scientific writing, and research communication**.

Alongside this, I worked for one year as a **Research Analyst Consultant** to a **Senior Economist at the World Bank**, contributing to research on agriculture in **Sub-Saharan Africa**. This experience further strengthened my empirical research, quantitative analysis, critical thinking, and policy evaluation skills.

During these years, I collaborated on several research projects, including a **second-authored journal article with Jiehong Lou**, which was **under revise-and-resubmit at _Environmental Research & Social Science_ during my Ph.D. application cycle**.

---

## Building My Application Beyond Research

### Academic Preparation

**B.Tech. Chemical Engineering**
*Dr. Babasaheb Ambedkar Technological University*

**Relevant Coursework:** Calculus, Linear Algebra, Differential Equations.

*I did not have formal coursework in Real Analysis. Contrary to popular belief, that wasn't the end of the world for me. 😄*

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
<p>Around the 50th percentile at the time... yep, not exactly the score Reddit wanted me to have. Everywhere I looked people seemed to be scoring <b>165+</b>, including several of my friends at Maryland, Cornell and Virginia Tech. Naturally, I thought, "One more attempt should do it..." So I took the GRE <b>four more times</b>. Still no 165. 🤷‍♂️ On the bright side, every attempt ended with sushi 🍣 somewhere in the D.C. area, so I'm still not convinced I was taking the GRE... I may have just been reviewing sushi restaurants. 😅🍱</p>
</div>
</details>

<details>
<summary>📄 Research Writing Sample</summary>
<div class="pd-details-body">
<p>One <b>solo-authored empirical research paper</b> using causal inference methods. It was only <b>six pages long</b>, but it represented nearly <b>6–7 months</b> of work ⏳, plus about <b>10 pages of supplementary material</b> 📑. Those six pages ended up doing an incredible amount of heavy lifting—they came up in almost every interview 🎤 and probably had a stronger social life than I did. 😂</p>
</div>
</details>

<details>
<summary>✉️ Recommendation Letters</summary>
<div class="pd-details-body">
<ul>
<li>👨‍🔬👩‍🔬 Two research supervisors (a combination of supervisors from the <b>Center for Global Sustainability</b> and the <b>World Bank</b>, depending on whether the programme was in Economics or Public Policy).</li>
<li>🎓 One academic recommendation from <b>instructors</b> in the University of Maryland's Applied Economics program. <i>(Yes—instructors, not professors! 😄 Great recommendation letters come from people who genuinely know your work, not necessarily the fanciest title.)</i> 🌟</li>
</ul>
</div>
</details>

<details>
<summary>🌶️ Secret Sauce</summary>
<div class="pd-details-body">
<p>No successful Ph.D. application is built alone. If my application had a secret sauce, it was the <b>weekly mentorship</b> I received from an economist working at <b>Amazon</b> (at the time... and maybe still there today). From my solo-authored research paper and Statement of Purpose to CV reviews, school selection, and mock interviews, he invested an incredible amount of time helping me build the strongest application possible. I owe a great deal of my application's success to his guidance, which taught me not only how to build a stronger application but also how to think more critically as a researcher.</p>
<p><i>P.S. 🤫 His identity shall remain classified. Every applicant deserves to find their own secret sauce.</i></p>
</div>
</details>

</div>

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

The table below summarizes the progression of my applications — filter it by outcome if you like.

<div class="pd-widget">
<div class="pd-filters" id="pdFilters">
  <button class="pd-chip active" data-filter="all">All (12)</button>
  <button class="pd-chip" data-filter="offer">Funded Offer, Accepted</button>
  <button class="pd-chip" data-filter="declined">Declined by Me</button>
  <button class="pd-chip" data-filter="waitlist">Waitlist / Not Pursued</button>
  <button class="pd-chip" data-filter="rejected">Not Admitted</button>
</div>

<table class="pd-table" id="pdTable">
<tr><th>University</th><th>Programme</th><th>Application Journey</th></tr>
<tr data-status="offer"><td><b>Penn State University</b></td><td>Energy, Environmental & Food Economics</td><td>Application → 1st Interview → 2nd Interview → ✅ Funded Offer → <b>Accepted</b></td></tr>
<tr data-status="declined"><td><b>National University of Singapore</b></td><td>Economics</td><td>Application → Interview → ✅ Funded Offer → Declined (Chose Penn State)</td></tr>
<tr data-status="declined"><td><b>University of California, Santa Cruz</b></td><td>Economics</td><td>Application → Interview → Oral Offer → Declined (Penn State was the better research fit)</td></tr>
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

- **No Final Decision or very late beyond april decisons:** NC State University, Virginia Tech, Simon Fraser University (I did not follow up after receiving funded offers elsewhere).--- I lost 3 applications just like that and some $$.

<div class="pd-widget">
<details>
<summary>🎓 Rejections: The "Character Development" Section</summary>
<div class="pd-details-body">
<p>Every Ph.D. applicant has a rejection folder. Here's part of mine 😄: Stanford University (ESS), Duke University (UPEP), Carnegie Mellon University (Public Policy), Columbia University (Sustainable Development), Economics programmes at UC San Diego, UT Austin, and Michigan State, and Agricultural Economics programmes at the University of Maryland, UC Berkeley, UIUC, and UW–Madison.</p>
</div>
</details>
</div>

---

### Interviews

One of the most enjoyable parts of the application cycle was the interviews.
Most of them felt much more like research conversations than formal interviews. Faculty were generally interested in discussing my research experiences, future ideas, and overall fit with the department rather than asking technical questions. Looking back, I think thorough preparation for my research paper, statement of purpose, and prior projects mattered far more than memorising answers to interview questions.

---

## Why Penn State?

After considering all of my offers, I ultimately chose **Penn State University's Energy, Environmental & Food Economics (EEFE)** program. My decision was primarily driven by **research fit**, faculty interests, long-term career goals, funding, and the opportunity to work in energy, environmental, and applied economics within an interdisciplinary department.

---

## Lessons Learned

<div class="pd-widget">
<ul class="pd-checklist" id="pdChecklist">
  <li><input type="checkbox" id="pd-l1"><label for="pd-l1">Research experience mattered far more than I initially expected.</label></li>
  <li><input type="checkbox" id="pd-l2"><label for="pd-l2">A strong research writing sample can open more doors than a slightly higher GRE score.</label></li>
  <li><input type="checkbox" id="pd-l3"><label for="pd-l3">Great recommendation letters come from people who genuinely know your work—not necessarily the most famous names.</label></li>
  <li><input type="checkbox" id="pd-l4"><label for="pd-l4">Mentorship is invaluable.</label></li>
  <li><input type="checkbox" id="pd-l5"><label for="pd-l5">Apply broadly, but apply strategically.</label></li>
  <li><input type="checkbox" id="pd-l6"><label for="pd-l6">Most importantly, there is no single path into a Ph.D.</label></li>
</ul>
</div>

---

## Final Thoughts

If this page helps even one applicant realise that there is no single blueprint for getting into a Ph.D. programme, then it has served its purpose.

If you're currently preparing your own applications, I wish you the very best. Good luck! 🚀

<script>
(function(){
  // animated stat counters
  var nums = document.querySelectorAll('.pd-num');
  if ('IntersectionObserver' in window) {
    var io = new IntersectionObserver(function(entries){
      entries.forEach(function(entry){
        if (entry.isIntersecting) {
          var el = entry.target;
          var target = parseInt(el.getAttribute('data-target'), 10);
          var cur = 0;
          var step = Math.max(1, Math.round(target / 30));
          (function tick(){
            cur += step;
            if (cur >= target) { el.textContent = target; return; }
            el.textContent = cur;
            requestAnimationFrame(tick);
          })();
          io.unobserve(el);
        }
      });
    }, { threshold: 0.5 });
    nums.forEach(function(el){ io.observe(el); });
  }

  // table filters
  var chips = document.querySelectorAll('.pd-chip');
  var rows = document.querySelectorAll('#pdTable tr[data-status]');
  chips.forEach(function(chip){
    chip.addEventListener('click', function(){
      chips.forEach(function(c){ c.classList.remove('active'); });
      chip.classList.add('active');
      var f = chip.getAttribute('data-filter');
      rows.forEach(function(row){
        row.classList.toggle('pd-hide', f !== 'all' && row.getAttribute('data-status') !== f);
      });
    });
  });

  // checklist strike-through
  document.querySelectorAll('#pdChecklist input[type="checkbox"]').forEach(function(box){
    box.addEventListener('change', function(){
      box.closest('li').classList.toggle('pd-checked', box.checked);
    });
  });
})();
</script>
