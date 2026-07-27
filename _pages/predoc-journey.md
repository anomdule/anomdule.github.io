---
title: ""
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

<div align="center">

<h1>Welcome to My Pre-Doctoral Journey </h1>

<p><em>Hello • नमस्ते • 你好 (Nǐ hǎo) • Hola </em></p>

</div>

This page documents my journey to entering a Ph.D. in Applied Economics—from building research experience and preparing my application to navigating interviews, offers, and ultimately choosing Penn State University.

During my application cycle, I received funded Ph.D. offers. Among them were offers from **Penn State University (EEFE)**, the **National University of Singapore (Economics)**, the **University of Georgia (Agricultural & Applied Economics)**, the **University of Maryland (Public Policy)**, and **Indiana University Bloomington (Public Affairs)**.

I hope this page serves as a useful resource for future applicants, especially those coming from non-traditional backgrounds. There is no single path to entering a Ph.D.— this was mine.

> ### 📍 At a Glance
>
> - 🎓 **Background:** B.Tech. Chemical Engineering → M.S. Applied Economics
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

## Research Experience Before the Ph.D.

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
<tr data-status="declined"><td><b>University of California, Santa Cruz</b></td><td>Economics</td><td>Application → Interview → Oral Offer → Funded offer was highly likely, but declined prior as Penn State was the better fit</td></tr>
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
  try {
    // animated stat counters — numbers already show the real value in HTML;
    // this just animates them up from 0 for a bit of polish. If anything
    // above fails, the real numbers stay visible regardless.
    var nums = document.querySelectorAll('.pd-num');
    nums.forEach(function(el){
      var target = parseInt(el.getAttribute('data-target'), 10);
      if (isNaN(target)) return;
      var cur = 0;
      el.textContent = '0';
      var step = Math.max(1, Math.round(target / 30));
      (function tick(){
        cur += step;
        if (cur >= target) { el.textContent = target; return; }
        el.textContent = cur;
        requestAnimationFrame(tick);
      })();
    });
  } catch (e) { /* leave static numbers as-is */ }

  try {
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
  } catch (e) {}

  try {
    // checklist strike-through
    document.querySelectorAll('#pdChecklist input[type="checkbox"]').forEach(function(box){
      box.addEventListener('change', function(){
        box.closest('li').classList.toggle('pd-checked', box.checked);
      });
    });
  } catch (e) {}
}

if (document.readyState === 'loading') {
  document.addEventListener('DOMContentLoaded', pdInit);
} else {
  pdInit();
}
</script>
