---
permalink: /
title: ""
excerpt: "Barış Temel — Data Scientist"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
/* ===== Barış Temel — home page (scoped under .bt) ===== */
.bt{
  --accent:#52adc8;        /* site link color */
  --accent-deep:#2b7c93;
  --ink:#2f3439;
  --muted:#6b7378;
  --line:#e7ebee;
  --card:#ffffff;
  --soft:#f4f8fa;
  --radius:14px;
  color:var(--ink);
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
}
.bt *{box-sizing:border-box;}
.bt a{color:var(--accent-deep);text-decoration:none;}
.bt a:hover{text-decoration:underline;}

/* Hero */
.bt-hero{
  background:linear-gradient(135deg,#eaf6fa 0%,#f6fbfc 55%,#ffffff 100%);
  border:1px solid var(--line);
  border-radius:var(--radius);
  padding:1.7rem 1.6rem;
  margin:.2rem 0 1.6rem;
}
.bt-eyebrow{
  display:inline-block;font-size:.72rem;letter-spacing:.14em;text-transform:uppercase;
  font-weight:700;color:var(--accent-deep);background:#dcf0f5;
  padding:.28rem .6rem;border-radius:999px;margin-bottom:.7rem;
}
.bt-hero h1{
  font-size:1.9rem;line-height:1.15;margin:.1rem 0 .5rem;border:0;padding:0;color:#1f2529;font-weight:800;
}
.bt-hero h1 .wave{display:inline-block;}
.bt-role{font-size:1.02rem;font-weight:600;color:var(--accent-deep);margin:.1rem 0 .7rem;}
.bt-lede{font-size:.98rem;color:var(--muted);margin:.2rem 0 1.1rem;max-width:60ch;}
.bt-stats{display:flex;flex-wrap:wrap;gap:.5rem;margin:.2rem 0 1.15rem;}
.bt-stat{
  background:#fff;border:1px solid var(--line);border-radius:10px;
  padding:.5rem .75rem;min-width:0;
}
.bt-stat b{display:block;font-size:1.2rem;line-height:1;color:var(--accent-deep);font-weight:800;}
.bt-stat span{font-size:.72rem;color:var(--muted);letter-spacing:.02em;}
.bt-cta{display:flex;flex-wrap:wrap;gap:.55rem;}
.bt-btn{
  display:inline-flex;align-items:center;gap:.4rem;font-size:.86rem;font-weight:600;
  padding:.55rem .95rem;border-radius:10px;border:1px solid var(--accent);
  transition:transform .08s ease, box-shadow .15s ease;
}
.bt-btn:hover{text-decoration:none;transform:translateY(-1px);}
.bt-btn--primary{background:var(--accent);color:#fff;border-color:var(--accent);box-shadow:0 6px 16px -8px rgba(43,124,147,.8);}
.bt-btn--primary:hover{background:var(--accent-deep);color:#fff;}
.bt-btn--ghost{background:#fff;color:var(--accent-deep);}
.bt-btn--ghost:hover{background:var(--soft);color:var(--accent-deep);}

/* Section */
.bt-sec{margin:2rem 0 0;}
.bt-sec > h2{
  font-size:1.18rem;font-weight:800;color:#20262b;margin:0 0 .2rem;border:0;padding:0;
  display:flex;align-items:center;gap:.55rem;
}
.bt-sec > h2::before{content:"";width:.55rem;height:1.15rem;border-radius:3px;background:var(--accent);display:inline-block;}
.bt-sec > p.bt-subtle{color:var(--muted);font-size:.9rem;margin:.1rem 0 1rem;}

/* Focus grid */
.bt-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:.8rem;}
.bt-focus{
  background:var(--card);border:1px solid var(--line);border-radius:12px;padding:.95rem 1rem;
  transition:border-color .15s ease, box-shadow .15s ease, transform .08s ease;
}
.bt-focus:hover{border-color:var(--accent);box-shadow:0 10px 24px -18px rgba(43,124,147,.9);transform:translateY(-1px);}
.bt-focus .ic{font-size:1.3rem;line-height:1;}
.bt-focus h3{font-size:.98rem;margin:.5rem 0 .3rem;color:#20262b;font-weight:700;}
.bt-focus p{font-size:.85rem;color:var(--muted);margin:0;}

/* Timeline / experience */
.bt-xp{border-left:2px solid var(--line);margin:.3rem 0 0;padding:0;list-style:none;}
.bt-xp li{position:relative;padding:0 0 1.25rem 1.25rem;}
.bt-xp li::before{
  content:"";position:absolute;left:-7px;top:.35rem;width:12px;height:12px;border-radius:50%;
  background:#fff;border:3px solid var(--accent);
}
.bt-xp li:last-child{padding-bottom:.2rem;}
.bt-xp .role{font-weight:700;color:#20262b;font-size:.98rem;}
.bt-xp .meta{font-size:.82rem;color:var(--muted);margin:.05rem 0 .45rem;}
.bt-xp .meta .co{color:var(--accent-deep);font-weight:600;}
.bt-xp ul{margin:.2rem 0 0;padding-left:1.05rem;}
.bt-xp ul li{padding:0;margin:.2rem 0;font-size:.87rem;color:var(--ink);}
.bt-xp ul li::before{display:none;}

/* Projects */
.bt-proj{display:grid;gap:.8rem;}
.bt-card{
  background:var(--card);border:1px solid var(--line);border-radius:12px;padding:1rem 1.1rem;
  transition:border-color .15s ease, box-shadow .15s ease, transform .08s ease;
}
.bt-card:hover{border-color:var(--accent);box-shadow:0 12px 26px -20px rgba(43,124,147,.9);transform:translateY(-1px);}
.bt-card.feat{background:linear-gradient(135deg,#eaf6fa,#ffffff);border-color:#bfe4ee;}
.bt-card .top{display:flex;align-items:center;justify-content:space-between;gap:.6rem;}
.bt-card h3{font-size:1rem;margin:0;color:#20262b;font-weight:700;}
.bt-card .tag{font-size:.68rem;font-weight:700;letter-spacing:.06em;text-transform:uppercase;color:var(--accent-deep);background:#dcf0f5;padding:.22rem .5rem;border-radius:999px;white-space:nowrap;}
.bt-card p{font-size:.87rem;color:var(--muted);margin:.5rem 0 0;}
.bt-card .go{font-size:.83rem;font-weight:600;margin-top:.55rem;display:inline-block;}

/* Skills */
.bt-skills{display:grid;gap:.7rem;}
.bt-skillrow{display:flex;flex-wrap:wrap;align-items:baseline;gap:.4rem;}
.bt-skillrow .lab{font-size:.8rem;font-weight:700;color:var(--muted);min-width:118px;text-transform:uppercase;letter-spacing:.05em;}
.bt-chip{
  font-size:.8rem;font-weight:600;color:#25555f;background:var(--soft);
  border:1px solid #d9e8ec;border-radius:999px;padding:.28rem .65rem;
}

/* Two-up (education + certs) */
.bt-two{display:grid;grid-template-columns:1fr 1fr;gap:.8rem;}
.bt-edu, .bt-cert{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:1rem 1.1rem;}
.bt-edu h4, .bt-cert h4{margin:0 0 .1rem;font-size:.95rem;color:#20262b;font-weight:700;}
.bt-edu .sub, .bt-cert li{font-size:.85rem;color:var(--muted);}
.bt-edu .gpa{font-size:.76rem;color:var(--accent-deep);font-weight:700;}
.bt-edu .item{padding:.15rem 0 .6rem;border-bottom:1px dashed var(--line);margin-bottom:.6rem;}
.bt-edu .item:last-child{border:0;margin:0;padding-bottom:0;}
.bt-cert ul{margin:.3rem 0 0;padding-left:1.05rem;}
.bt-cert li{margin:.28rem 0;}

/* Contact */
.bt-contact{
  margin-top:2rem;background:linear-gradient(135deg,#20323a,#2b7c93);
  border-radius:var(--radius);padding:1.5rem 1.5rem;color:#eaf6fa;text-align:center;
}
.bt-contact h2{color:#fff;border:0;font-size:1.25rem;margin:0 0 .35rem;font-weight:800;}
.bt-contact h2::before{display:none;}
.bt-contact p{color:#cfe8ef;font-size:.92rem;margin:0 auto 1rem;max-width:46ch;}
.bt-contact .bt-cta{justify-content:center;}
.bt-contact .bt-btn--primary{background:#fff;color:var(--accent-deep);border-color:#fff;}
.bt-contact .bt-btn--primary:hover{background:#eaf6fa;color:var(--accent-deep);}
.bt-contact .bt-btn--ghost{background:transparent;color:#fff;border-color:rgba(255,255,255,.6);}
.bt-contact .bt-btn--ghost:hover{background:rgba(255,255,255,.12);color:#fff;}

@media (max-width:600px){
  .bt-grid,.bt-two{grid-template-columns:1fr;}
  .bt-hero h1{font-size:1.55rem;}
  .bt-skillrow .lab{min-width:100%;}
}
</style>

<div class="bt" markdown="0">

<section class="bt-hero">
  <span class="bt-eyebrow">Data Scientist · GenAI · Analytics</span>
  <h1>Hi, I'm Barış <span class="wave">👋</span></h1>
  <div class="bt-role">Data Scientist &amp; Governance Analyst @ The Coca-Cola Company</div>
  <p class="bt-lede">I build GenAI-powered applications, predictive models, and BI solutions that turn messy, real-world data into decisions — with 6+ years across FMCG, fintech, and technology, working with teams across the EMEA region.</p>
  <div class="bt-stats">
    <div class="bt-stat"><b>6+</b><span>years in data science</span></div>
    <div class="bt-stat"><b>25+</b><span>countries supported</span></div>
    <div class="bt-stat"><b>3</b><span>sectors: FMCG · fintech · tech</span></div>
    <div class="bt-stat"><b>MSc</b><span>Data Science, Sabancı</span></div>
  </div>
  <div class="bt-cta">
    <a class="bt-btn bt-btn--primary" href="/files/Baris_Temel_Data_Science_Resume.pdf">📄 View CV</a>
    <a class="bt-btn bt-btn--ghost" href="https://atlantis.baristemel.com">🌊 Explore Atlantis</a>
    <a class="bt-btn bt-btn--ghost" href="https://www.linkedin.com/in/baris-temel/">in LinkedIn</a>
    <a class="bt-btn bt-btn--ghost" href="mailto:btemel@sabanciuniv.edu">✉ Email</a>
  </div>
</section>

<section class="bt-sec">
  <h2>What I focus on</h2>
  <div class="bt-grid">
    <div class="bt-focus">
      <div class="ic">🤖</div>
      <h3>Generative AI applications</h3>
      <p>RAG systems, agent frameworks, and vector search that make unstructured documents conversational.</p>
    </div>
    <div class="bt-focus">
      <div class="ic">📈</div>
      <h3>Predictive modeling &amp; forecasting</h3>
      <p>Time-series forecasting, clustering, and key-driver models built into planning and scenario tools.</p>
    </div>
    <div class="bt-focus">
      <div class="ic">📊</div>
      <h3>BI &amp; analytics</h3>
      <p>Power BI &amp; Tableau dashboards and automated, real-time narratives for executive decision-making.</p>
    </div>
    <div class="bt-focus">
      <div class="ic">🛡️</div>
      <h3>Data governance</h3>
      <p>Improving data quality and validation processes across 25+ countries in the EME operating unit.</p>
    </div>
  </div>
</section>

<section class="bt-sec">
  <h2>Experience</h2>
  <ul class="bt-xp">
    <li>
      <div class="role">Data Scientist &amp; Governance Analyst</div>
      <div class="meta"><span class="co">The Coca-Cola Company</span> · Istanbul · Feb 2023 – Present</div>
      <ul>
        <li>Technical owner of AI initiatives across EMEA, translating business needs into end-to-end solutions.</li>
        <li>Led an <b>AI-Enabled Knowledge Hub</b> — a GenAI tool that retrieves answers from unstructured documents, ChatGPT-style.</li>
        <li>Built <b>AI-Driven Smart Narratives</b> generating real-time dashboard insights, cutting insight time from days to hours.</li>
        <li>Shipped revenue forecasting, key-driver analysis, and clustering models used across the top 40 countries.</li>
      </ul>
    </li>
    <li>
      <div class="role">Data Scientist</div>
      <div class="meta"><span class="co">REEF</span> · Miami, US · Aug 2021 – May 2022</div>
      <ul>
        <li>Built Python web scrapers (BeautifulSoup, Selenium) and REST/SQL data structures for market analysis.</li>
        <li>Developed 20+ kitchen dashboards on Amazon Redshift and Tableau for strategy &amp; operations KPIs.</li>
      </ul>
    </li>
    <li>
      <div class="role">Teaching Assistant — Intro to Python (IF100)</div>
      <div class="meta"><span class="co">Sabancı University</span> · Istanbul · Sep 2020 – Jun 2022</div>
      <ul>
        <li>Taught computational problem-solving to freshmen, from fundamentals to intermediate concepts.</li>
      </ul>
    </li>
    <li>
      <div class="role">Data Analyst</div>
      <div class="meta"><span class="co">QNB Finansbank</span> · Istanbul · Mar 2019 – Jun 2020</div>
      <ul>
        <li>Management trainee: built models in Python &amp; R, automated reports, and delivered a credit-card fraud detection project.</li>
      </ul>
    </li>
  </ul>
</section>

<section class="bt-sec">
  <h2>Selected work</h2>
  <p class="bt-subtle">A few things I've built recently.</p>
  <div class="bt-proj">
    <div class="bt-card feat">
      <div class="top"><h3>🌊 Atlantis</h3><span class="tag">Live · GenAI RAG</span></div>
      <p>A multi-tenant Graph-RAG Q&amp;A application on AWS — my own end-to-end project spanning retrieval, a Python backend, and a cloud-native frontend.</p>
      <a class="go" href="https://atlantis.baristemel.com">Open the app →</a>
    </div>
    <div class="bt-card">
      <div class="top"><h3>AI-Enabled Knowledge Hub</h3><span class="tag">Coca-Cola</span></div>
      <p>Internal GenAI assistant that understands and retrieves information from unstructured documents for a conversational, ChatGPT-like experience.</p>
    </div>
    <div class="bt-card">
      <div class="top"><h3>Daha Daha — AI Survey Insights</h3><span class="tag">Coca-Cola</span></div>
      <p>Intelligent system analyzing large-scale open-text consumer surveys to surface pain points, sentiment, and trends — weeks of manual work down to days.</p>
    </div>
    <div class="bt-card">
      <div class="top"><h3>Follower Anomalies on Social Media</h3><span class="tag">MSc Thesis</span></div>
      <p>An open-source algorithm to detect anomalous followers on social networks, with Twitter as the primary target. Sabancı University, 2022.</p>
    </div>
  </div>
</section>

<section class="bt-sec">
  <h2>Skills &amp; tools</h2>
  <div class="bt-skills">
    <div class="bt-skillrow"><span class="lab">Languages</span>
      <span class="bt-chip">Python</span><span class="bt-chip">SQL</span><span class="bt-chip">R</span>
    </div>
    <div class="bt-skillrow"><span class="lab">ML / AI</span>
      <span class="bt-chip">Machine Learning</span><span class="bt-chip">Deep Learning</span><span class="bt-chip">LLMs &amp; Agents</span><span class="bt-chip">Vector Search</span><span class="bt-chip">Prompt Engineering</span>
    </div>
    <div class="bt-skillrow"><span class="lab">Data</span>
      <span class="bt-chip">Big Data</span><span class="bt-chip">Data Management</span><span class="bt-chip">Data Governance</span>
    </div>
    <div class="bt-skillrow"><span class="lab">Tools</span>
      <span class="bt-chip">Azure</span><span class="bt-chip">Power BI</span><span class="bt-chip">Tableau</span><span class="bt-chip">Docker</span><span class="bt-chip">Git</span><span class="bt-chip">Jira</span><span class="bt-chip">MS Copilot</span>
    </div>
  </div>
</section>

<section class="bt-sec">
  <h2>Education &amp; certifications</h2>
  <div class="bt-two">
    <div class="bt-edu">
      <div class="item">
        <h4>MSc, Data Science</h4>
        <div class="sub">Sabancı University · 2022</div>
        <div class="gpa">GPA 3.50 / 4.00</div>
      </div>
      <div class="item">
        <h4>BSc, Industrial Engineering</h4>
        <div class="sub">Sabancı University · 2019</div>
        <div class="gpa">GPA 3.01 / 4.00 · Minor in Finance</div>
      </div>
    </div>
    <div class="bt-cert">
      <h4>Certifications</h4>
      <ul>
        <li>Certified Scrum Product Owner (CSPO) — Scrum Alliance</li>
        <li>Data Scientist — DataCamp</li>
        <li>AI Engineer for Data Scientists, Associate — DataCamp</li>
      </ul>
    </div>
  </div>
</section>

<section class="bt-contact">
  <h2>Let's build something</h2>
  <p>Open to conversations about GenAI, data science, and analytics. The fastest way to reach me is email or LinkedIn.</p>
  <div class="bt-cta">
    <a class="bt-btn bt-btn--primary" href="mailto:btemel@sabanciuniv.edu">✉ Get in touch</a>
    <a class="bt-btn bt-btn--ghost" href="/files/Baris_Temel_Data_Science_Resume.pdf">📄 Download CV</a>
    <a class="bt-btn bt-btn--ghost" href="https://github.com/btemel">GitHub</a>
  </div>
</section>

</div>
