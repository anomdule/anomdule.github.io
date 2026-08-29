---
layout: archive
title: ""
permalink: /publications/
author_profile: true
---

<style>
  .pub-page{
    --pub-text:#182033;
    --pub-muted:#667085;
    --pub-border:rgba(24,32,51,.12);
    --pub-blue:#3157d5;
    --pub-purple:#6d4ed8;
    --pub-green:#17765c;
    --pub-orange:#9a5b00;
    --pub-cyan:#176c9c;
    --pub-bg:#ffffff;
    --pub-soft:#f7f9fc;
    --pub-shadow:0 10px 30px rgba(15,23,42,.07);
    color:var(--pub-text);
    font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Helvetica,Arial,sans-serif;
  }

  .pub-hero{
    position:relative;
    overflow:hidden;
    margin:0 0 28px;
    padding:34px 30px;
    border:1px solid var(--pub-border);
    border-radius:22px;
    background:
      radial-gradient(circle at 92% 10%,rgba(49,87,213,.07),transparent 28%),
      linear-gradient(135deg,#ffffff 0%,#fafbff 58%,#f8f6ff 100%);
    box-shadow:var(--pub-shadow);
  }

  .pub-hero h1{
    margin:0 0 10px;
    font-size:clamp(2rem,4vw,2.75rem);
    line-height:1.08;
    letter-spacing:-.035em;
    background:linear-gradient(90deg,var(--pub-blue),var(--pub-purple));
    -webkit-background-clip:text;
    background-clip:text;
    color:transparent;
  }

  .pub-hero p{
    max-width:760px;
    margin:0;
    color:var(--pub-muted);
    font-size:15.5px;
    line-height:1.7;
  }

  .pub-stats{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:12px;
    margin:20px 0 26px;
  }

  .pub-stat{
    padding:18px 12px;
    text-align:center;
    border:1px solid var(--pub-border);
    border-radius:16px;
    background:#fff;
    box-shadow:0 5px 18px rgba(15,23,42,.04);
    transition:transform .2s ease,box-shadow .2s ease,border-color .2s ease;
  }

  .pub-stat:hover{
    transform:translateY(-4px);
    border-color:rgba(49,87,213,.23);
    box-shadow:0 12px 28px rgba(15,23,42,.09);
  }

  .pub-stat-number{
    display:block;
    font-size:28px;
    line-height:1;
    font-weight:800;
    color:var(--pub-blue);
  }

  .pub-stat-label{
    display:block;
    margin-top:7px;
    color:var(--pub-muted);
    font-size:12px;
  }

  .pub-controls{
    display:flex;
    align-items:center;
    gap:10px;
    flex-wrap:wrap;
    margin:0 0 26px;
    padding:12px;
    border:1px solid var(--pub-border);
    border-radius:16px;
    background:linear-gradient(135deg,#fbfcff,#faf9ff);
  }

  .pub-search{
    flex:1 1 240px;
    min-width:0;
    padding:10px 14px;
    border:1px solid var(--pub-border);
    border-radius:999px;
    background:#fff;
    color:var(--pub-text);
    font:inherit;
    outline:none;
    transition:border-color .2s ease,box-shadow .2s ease;
  }

  .pub-search:focus{
    border-color:rgba(49,87,213,.45);
    box-shadow:0 0 0 4px rgba(49,87,213,.08);
  }

  .pub-filters{
    display:flex;
    gap:7px;
    flex-wrap:wrap;
  }

  .pub-filter{
    padding:7px 11px;
    border:1px solid var(--pub-border);
    border-radius:999px;
    background:#fff;
    color:var(--pub-muted);
    font-size:12px;
    cursor:pointer;
    transition:transform .15s ease,border-color .15s ease,background .15s ease,color .15s ease;
  }

  .pub-filter:hover{
    transform:translateY(-1px);
    border-color:rgba(49,87,213,.3);
  }

  .pub-filter.active{
    border-color:transparent;
    background:linear-gradient(90deg,var(--pub-blue),var(--pub-purple));
    color:#fff;
    font-weight:700;
    box-shadow:0 5px 14px rgba(49,87,213,.18);
  }

  .pub-section{
    margin:34px 0;
  }

  .pub-section-heading{
    display:flex;
    align-items:center;
    gap:10px;
    margin:0 0 16px;
    font-size:21px;
    letter-spacing:-.02em;
  }

  .pub-section-heading::after{
    content:"";
    flex:1;
    height:1px;
    background:linear-gradient(90deg,var(--pub-border),transparent);
  }

  .pub-grid{
    display:grid;
    gap:15px;
  }

  .pub-card{
    position:relative;
    overflow:hidden;
    padding:21px 22px;
    border:1px solid var(--pub-border);
    border-radius:18px;
    background:#fff;
    box-shadow:0 6px 20px rgba(15,23,42,.045);
    transition:transform .22s ease,box-shadow .22s ease,border-color .22s ease;
  }

  .pub-card::before{
    content:"";
    position:absolute;
    top:0;
    bottom:0;
    left:0;
    width:4px;
    background:linear-gradient(180deg,var(--pub-blue),var(--pub-purple));
  }

  .pub-card:hover{
    transform:translateY(-4px);
    border-color:rgba(49,87,213,.24);
    box-shadow:0 14px 34px rgba(15,23,42,.09);
  }

  .pub-card-top{
    display:flex;
    align-items:flex-start;
    justify-content:space-between;
    gap:14px;
    margin-bottom:10px;
  }

  .pub-title{
    margin:0;
    font-size:18px;
    line-height:1.42;
    letter-spacing:-.015em;
  }

  .pub-badge{
    flex:0 0 auto;
    display:inline-block;
    padding:4px 9px;
    border-radius:999px;
    font-size:11px;
    line-height:1.4;
    font-weight:700;
    white-space:nowrap;
  }

  .pub-badge.working{
    background:#eef2ff;
    color:#3f51b5;
  }

  .pub-badge.article{
    background:#e8f8f1;
    color:#137052;
  }

  .pub-badge.brief{
    background:#fff7e6;
    color:#9a5b00;
  }

  .pub-badge.conference{
    background:#f3edff;
    color:#6842b8;
  }

  .pub-badge.database{
    background:#e8f5ff;
    color:#176c9c;
  }

  .pub-authors{
    margin:0 0 8px;
    color:var(--pub-muted);
    font-size:14px;
    line-height:1.68;
  }

  .pub-authors strong{
    color:var(--pub-text);
  }

  .pub-venue{
    margin:0;
    color:#344054;
    font-size:14px;
    line-height:1.62;
  }

  .pub-meta{
    margin-top:8px;
    color:var(--pub-muted);
    font-size:12.5px;
    line-height:1.55;
  }

  .pub-actions{
    display:flex;
    gap:8px;
    flex-wrap:wrap;
    margin-top:15px;
  }

  .pub-button{
    display:inline-flex;
    align-items:center;
    gap:6px;
    padding:7px 11px;
    border:1px solid var(--pub-border);
    border-radius:9px;
    background:#fff;
    color:var(--pub-blue);
    font-size:12px;
    font-weight:650;
    cursor:pointer;
    text-decoration:none !important;
    transition:background .15s ease,border-color .15s ease,transform .15s ease;
  }

  .pub-button:hover{
    transform:translateY(-1px);
    border-color:rgba(49,87,213,.3);
    background:#f7f9ff;
  }

  .pub-button.disabled{
    color:var(--pub-muted);
    cursor:default;
    background:var(--pub-soft);
  }

  .pub-button.disabled:hover{
    transform:none;
    border-color:var(--pub-border);
  }

  .pub-hidden{
    display:none !important;
  }

  .pub-empty{
    display:none;
    padding:34px 20px;
    text-align:center;
    border:1px dashed var(--pub-border);
    border-radius:18px;
    color:var(--pub-muted);
  }

  .pub-reveal{
    opacity:0;
    transform:translateY(13px);
    transition:opacity .5s ease,transform .5s ease;
  }

  .pub-reveal.pub-visible{
    opacity:1;
    transform:none;
  }

  @media(max-width:720px){
    .pub-stats{
      grid-template-columns:repeat(2,1fr);
    }

    .pub-hero{
      padding:29px 20px;
    }

    .pub-card{
      padding:19px 17px;
    }

    .pub-card-top{
      display:block;
    }

    .pub-badge{
      margin-top:9px;
    }
  }

  @media(prefers-reduced-motion:reduce){
    .pub-reveal{
      opacity:1;
      transform:none;
    }

    *,
    *::before,
    *::after{
      animation-duration:.01ms !important;
      transition-duration:.01ms !important;
    }
  }
</style>

<div class="pub-page">

  <header class="pub-hero">
    <h1>Publications & Work In Progess</h1>
    <p>
    </p>
  </header>

  <div class="pub-stats">
    <div class="pub-stat">
      <span class="pub-stat-number" data-target="1">1</span>
      <span class="pub-stat-label">Work in Progress</span>
    </div>

    <div class="pub-stat">
      <span class="pub-stat-number" data-target="2">2</span>
      <span class="pub-stat-label">Journal Articles</span>
    </div>

    <div class="pub-stat">
      <span class="pub-stat-number" data-target="1">1</span>
      <span class="pub-stat-label">Policy Brief</span>
    </div>

    <div class="pub-stat">
      <span class="pub-stat-number" data-target="2">2</span>
      <span class="pub-stat-label">Other Research Outputs</span>
    </div>
  </div>

  <div class="pub-controls">
    <input
      type="search"
      id="pubSearch"
      class="pub-search"
      placeholder="Search by title, author, journal, or topic…"
      aria-label="Search publications"
    >

    <div class="pub-filters" id="pubFilters">
      <button class="pub-filter active" data-filter="all">All</button>
      <button class="pub-filter" data-filter="working">Work in Progress</button>
      <button class="pub-filter" data-filter="article">Journal Articles</button>
      <button class="pub-filter" data-filter="brief">Policy Brief</button>
      <button class="pub-filter" data-filter="conference">Conference</button>
      <button class="pub-filter" data-filter="database">Database</button>
    </div>
  </div>

  <section class="pub-section" data-section="working">
    <h2 class="pub-section-heading">📄 Independent Research</h2>

    <div class="pub-grid">
      <article
        class="pub-card"
        data-category="working"
        data-search="power outages crime working paper anom dule independent research"
      >
        <div class="pub-card-top">
          <h3 class="pub-title">The Effect of Power Outages on Crime</h3>
          <span class="pub-badge working">Work in Progress</span>
        </div>

        <p class="pub-authors">
          <strong>A. Dule</strong>
        </p>

        <p class="pub-venue">
          Independent research project.
        </p>

        <div class="pub-actions">
          <span class="pub-button disabled">🔗 Paper forthcoming</span>

          <button
            class="pub-button pub-copy"
            type="button"
            data-citation="Dule, A. “The Effect of Power Outages on Crime.” Work in Progress."
          >
            📋 Copy citation
          </button>
        </div>
      </article>
    </div>
  </section>

  <section class="pub-section" data-section="article">
    <h2 class="pub-section-heading">📑 Journal Articles</h2>

    <div class="pub-grid">
      <article
        class="pub-card"
        data-category="article"
        data-search="advancing equity electric vehicle infrastructure charging accessibility national electric vehicle infrastructure nevi energy research social science lou dule shen hultman"
      >
        <div class="pub-card-top">
          <h3 class="pub-title">
            Advancing Equity in Electric Vehicle Infrastructure:
            Assessing Charging Accessibility Under the National Electric
            Vehicle Infrastructure (NEVI) Program
          </h3>

          <span class="pub-badge article">Journal Article</span>
        </div>

        <p class="pub-authors">
          Jiehong Lou,
          <strong>Anom Ashok Dule</strong>,
          Xingchi Shen,
          Nathan Hultman
        </p>

        <p class="pub-venue">
          <strong>Energy Research &amp; Social Science</strong>,
          Volume 134, 2026, 104620.
        </p>

        <p class="pub-meta">
          ISSN 2214-6296
        </p>

        <div class="pub-actions">
          <a
            class="pub-button"
            href="https://doi.org/10.1016/j.erss.2026.104620"
            target="_blank"
            rel="noopener"
          >
            🔗 View DOI
          </a>

          <button
            class="pub-button pub-copy"
            type="button"
            data-citation="Lou, J., Dule, A. A., Shen, X., and Hultman, N. “Advancing Equity in Electric Vehicle Infrastructure: Assessing Charging Accessibility Under the National Electric Vehicle Infrastructure (NEVI) Program.” Energy Research & Social Science, 134 (2026), 104620. https://doi.org/10.1016/j.erss.2026.104620."
          >
            📋 Copy citation
          </button>
        </div>
      </article>

      <article
        class="pub-card"
        data-category="article"
        data-search="united states china anthropogenic methane emissions uncertainties collaborative opportunities earth future behrendt smith yu chen zhang zhu williams cheng dule li cui hultman"
      >
        <div class="pub-card-top">
          <h3 class="pub-title">
            United States and China Anthropogenic Methane Emissions:
            A Review of Uncertainties and Collaborative Opportunities
          </h3>

          <span class="pub-badge article">Journal Article</span>
        </div>

        <p class="pub-authors">
          J. Behrendt, S. Smith, S. Yu, S. Chen, H. Zhang, M. Zhu,
          J. Williams, X. Cheng, <strong>A. Dule</strong>, W. Li,
          R. Cui, N. Hultman
        </p>

        <p class="pub-venue">
          <strong>Earth’s Future</strong>, 13, e2024EF005298.
        </p>

        <div class="pub-actions">
          <button
            class="pub-button pub-copy"
            type="button"
            data-citation="Behrendt, J., Smith, S., Yu, S., Chen, S., Zhang, H., Zhu, M., Williams, J., Cheng, X., Dule, A., Li, W., Cui, R., and Hultman, N. “United States and China Anthropogenic Methane Emissions: A Review of Uncertainties and Collaborative Opportunities.” Earth’s Future, 13, e2024EF005298."
          >
            📋 Copy citation
          </button>
        </div>
      </article>
    </div>
  </section>

  <section class="pub-section" data-section="brief">
    <h2 class="pub-section-heading">📘 Policy Brief</h2>

    <div class="pub-grid">
      <article
        class="pub-card"
        data-category="brief"
        data-search="coal mine methane shanxi province mitigation opportunities center global sustainability university maryland behrendt cheng chen dule zhang smith zhu cui mei li fu hultman"
      >
        <div class="pub-card-top">
          <h3 class="pub-title">
            Understanding Coal Mine Methane Sources and Mitigation
            Opportunities in Shanxi Province
          </h3>

          <span class="pub-badge brief">Policy Brief</span>
        </div>

        <p class="pub-authors">
          J. Behrendt, X. Cheng, S. Chen, <strong>A. Dule</strong>,
          H. Zhang, S.J. Smith, M. Zhu, R. Cui, C. Mei, L. Chen,
          M. Li, S. Fu, N. Hultman
        </p>

        <p class="pub-venue">
          <strong>Center for Global Sustainability</strong>,
          University of Maryland. 15 pages.
        </p>

        <div class="pub-actions">
          <button
            class="pub-button pub-copy"
            type="button"
            data-citation="Behrendt, J., Cheng, X., Chen, S., Dule, A., Zhang, H., Smith, S.J., Zhu, M., Cui, R., Mei, C., Chen, L., Li, M., Fu, S., and Hultman, N. “Understanding Coal Mine Methane Sources and Mitigation Opportunities in Shanxi Province.” Center for Global Sustainability, University of Maryland."
          >
            📋 Copy citation
          </button>
        </div>
      </article>
    </div>
  </section>

  <section class="pub-section" data-section="conference">
    <h2 class="pub-section-heading">🗣️ Conference Presentation</h2>

    <div class="pub-grid">
      <article
        class="pub-card"
        data-category="conference"
        data-search="refugee population asylum country gdp per capita western economic association international weai melbourne 2023 dule"
      >
        <div class="pub-card-top">
          <h3 class="pub-title">
            What is the Effect of Refugee Population on the
            Asylum Country’s GDP per Capita?
          </h3>

          <span class="pub-badge conference">Conference Paper</span>
        </div>

        <p class="pub-authors">
          <strong>A. Dule</strong>
        </p>

        <p class="pub-venue">
          <strong>Western Economic Association International (WEAI) Conference</strong>,
          Melbourne, 2023.
        </p>

        <div class="pub-actions">
          <button
            class="pub-button pub-copy"
            type="button"
            data-citation="Dule, A. “What is the Effect of Refugee Population on the Asylum Country’s GDP per Capita?” Presented at the Western Economic Association International Conference, Melbourne, 2023."
          >
            📋 Copy citation
          </button>
        </div>
      </article>
    </div>
  </section>

  <section class="pub-section" data-section="database">
    <h2 class="pub-section-heading">🧮 Database Creation</h2>

    <div class="pub-grid">
      <article
        class="pub-card"
        data-category="database"
        data-search="global methane abatement solutions tracker gmast center global sustainability zhu hu cheng sahu li vaddeboina sharma kalra thakkar dule lu singh cui"
      >
        <div class="pub-card-top">
          <h3 class="pub-title">
            Global Methane Abatement Solutions Tracker (G-MAST)
          </h3>

          <span class="pub-badge database">Research Database</span>
        </div>

        <p class="pub-authors">
          M. Zhu, G. Hu, X. Cheng, S. Sahu, Y. Li, S. Vaddeboina,
          A. Sharma, I. Kalra, D. Thakkar, <strong>A. Dule</strong>,
          Z. Lu, H. Singh, R. Cui
        </p>

        <p class="pub-venue">
          <strong>Center for Global Sustainability</strong>,
          University of Maryland, 2025.
        </p>

        <div class="pub-actions">
          <button
            class="pub-button pub-copy"
            type="button"
            data-citation="Zhu, M., Hu, G., Cheng, X., Sahu, S., Li, Y., Vaddeboina, S., Sharma, A., Kalra, I., Thakkar, D., Dule, A., Lu, Z., Singh, H., and Cui, R. “Global Methane Abatement Solutions Tracker (G-MAST).” Center for Global Sustainability, University of Maryland, 2025."
          >
            📋 Copy citation
          </button>
        </div>
      </article>
    </div>
  </section>

  <div class="pub-empty" id="pubEmpty">
    No research outputs matched your search.
  </div>

</div>

<script>
function initialisePublicationsPage(){
  var search=document.getElementById("pubSearch");
  var filters=document.querySelectorAll(".pub-filter");
  var cards=document.querySelectorAll(".pub-card");
  var sections=document.querySelectorAll(".pub-section");
  var emptyMessage=document.getElementById("pubEmpty");
  var activeCategory="all";

  function updatePublications(){
    var query=search.value.trim().toLowerCase();
    var visibleCards=0;

    cards.forEach(function(card){
      var category=card.getAttribute("data-category");
      var searchText=(
        (card.getAttribute("data-search") || "") +
        " " +
        card.textContent
      ).toLowerCase();

      var matchesCategory=
        activeCategory==="all" ||
        category===activeCategory;

      var matchesSearch=
        query==="" ||
        searchText.indexOf(query)!==-1;

      var show=matchesCategory && matchesSearch;

      card.classList.toggle("pub-hidden",!show);

      if(show){
        visibleCards+=1;
      }
    });

    sections.forEach(function(section){
      var visibleInside=section.querySelector(
        ".pub-card:not(.pub-hidden)"
      );

      section.classList.toggle(
        "pub-hidden",
        !visibleInside
      );
    });

    emptyMessage.style.display=
      visibleCards===0 ? "block" : "none";
  }

  filters.forEach(function(button){
    button.addEventListener("click",function(){
      filters.forEach(function(item){
        item.classList.remove("active");
      });

      button.classList.add("active");
      activeCategory=button.getAttribute("data-filter");
      updatePublications();
    });
  });

  search.addEventListener("input",updatePublications);

  document.querySelectorAll(".pub-copy").forEach(function(button){
    button.addEventListener("click",function(){
      var citation=button.getAttribute("data-citation");
      var oldText=button.textContent;

      if(navigator.clipboard && navigator.clipboard.writeText){
        navigator.clipboard.writeText(citation).then(function(){
          button.textContent="✓ Citation copied";

          setTimeout(function(){
            button.textContent=oldText;
          },1600);
        }).catch(function(){
          button.textContent="Copy unavailable";

          setTimeout(function(){
            button.textContent=oldText;
          },1600);
        });
      }else{
        button.textContent="Copy unavailable";

        setTimeout(function(){
          button.textContent=oldText;
        },1600);
      }
    });
  });

  try{
    var counters=document.querySelectorAll(".pub-stat-number");

    var counterObserver=new IntersectionObserver(
      function(entries,observer){
        entries.forEach(function(entry){
          if(!entry.isIntersecting){
            return;
          }

          var element=entry.target;
          var target=parseInt(
            element.getAttribute("data-target"),
            10
          );

          var start=null;
          var duration=700;

          function animate(timestamp){
            if(!start){
              start=timestamp;
            }

            var progress=Math.min(
              (timestamp-start)/duration,
              1
            );

            element.textContent=Math.round(
              target*(1-Math.pow(1-progress,3))
            );

            if(progress<1){
              requestAnimationFrame(animate);
            }else{
              element.textContent=target;
            }
          }

          element.textContent="0";
          requestAnimationFrame(animate);
          observer.unobserve(element);
        });
      },
      {threshold:.45}
    );

    counters.forEach(function(counter){
      counterObserver.observe(counter);
    });
  }catch(error){}

  try{
    var revealItems=document.querySelectorAll(
      ".pub-card, .pub-section-heading, .pub-stats"
    );

    revealItems.forEach(function(item){
      item.classList.add("pub-reveal");
    });

    var revealObserver=new IntersectionObserver(
      function(entries,observer){
        entries.forEach(function(entry){
          if(entry.isIntersecting){
            entry.target.classList.add("pub-visible");
            observer.unobserve(entry.target);
          }
        });
      },
      {
        threshold:.08,
        rootMargin:"0px 0px -25px 0px"
      }
    );

    revealItems.forEach(function(item){
      revealObserver.observe(item);
    });
  }catch(error){}
}

if(document.readyState==="loading"){
  document.addEventListener(
    "DOMContentLoaded",
    initialisePublicationsPage
  );
}else{
  initialisePublicationsPage();
}
</script>

<style>
@media screen and (min-width: 1024px) {

  .page__inner-wrap,
  .page__content {
    width: 100% !important;
    max-width: none !important;
  }

  .page__content > div,
  .page__content > section,
  .page__content .container,
  .page__content .wrapper {
    width: 100% !important;
    max-width: none !important;
    box-sizing: border-box;
  }

}
</style>
