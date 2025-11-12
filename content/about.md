<style>
/* Clean, theme-consistent layout */
.about-wrapper {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 3rem;
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem 2rem 4rem;
}

@media (max-width: 900px) {
  .about-wrapper {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
}

/* Text column */
.bio p {
  margin-bottom: 1rem;
  line-height: 1.7;
}

/* Timeline column */
.timeline-column {
  border-left: 2px solid var(--accent);
  padding-left: 1.5rem;
  font-size: 0.95rem;
}

.timeline-placeholder {
  color: var(--text-secondary);
  font-style: italic;
  opacity: 0.6;
  margin-bottom: 1rem;
}

/* Entries */
.timeline-entry { margin-bottom: 1rem; position: relative; }
.timeline-entry::before {
  content: '';
  position: absolute;
  left: -12px; top: 6px;
  width: 8px; height: 8px;
  border-radius: 50%;
  background: var(--accent);
}
.timeline-year { color: var(--accent); font-weight: 600; margin-bottom: 0.2rem; }
.timeline-org { cursor: pointer; font-weight: 600; }
.timeline-role { font-style: italic; color: var(--text-secondary); }
.timeline-details { display: none; margin-top: 0.3rem; line-height: 1.5; }

/* Trigger link */
.timeline-trigger {
  color: var(--accent);
  cursor: pointer;
  border-bottom: 1px dashed var(--accent);
}
.timeline-trigger:hover { color: var(--accent-alt); }
</style>

<div class="about-wrapper">

<div class="bio">

## Little bit about me
<p>Hey!</p>
<p>I'm Riha! You might know me as Hari/Harikrishnan.</p>

<p>I am a part anthropologist, part systems thinker, and full-time translator between people, data, and decisions. My journey in technology is driven by curiosity and a love for solving complex problems with data.</p>

I study the human side of systems: [how organizations make meaning from information, how teams use (or ignore) data, and how decisions ripple through real-world outcomes.]() My approach blends data science, anthropology, and systems thinking to build tools that serve both insight and empathy.

[I’ve worked across corporate, startup, and non-profit ecosystems, designing data systems that adapt to each context]() — from fast-paced innovation labs to grounded field programs. This breadth helps me translate across worlds: tech and operations, business and impact, boardrooms and grassroots.

<p>In every setting, my goal is the same — to make data human, useful, and quietly powerful.</p>

## Areas I work in 
    - Business Intelligence & Decision Support 
    - Data Science for Impact Measurement 
    - Systems Thinking & Organizational Anthropology 
    - Low-code solutions & Automation Workflows
    - Data Literacy Training & Change Enablement 
    - Executive Analytics & Strategic Dashboards

## What I do I help organizations: 
    - Turn fragmented data into clear insights 
    - Build live dashboards that drive real decisions 
    - Automate repetitive reporting and monitoring 
    - Design feedback loops between field and leadership 
    - Translate complex analytics into operational clarity

## Skills & Technologies 
    - Programming Languages : Python, R, SQL 
    - Data Visualization    : Matplotlib, Seaborn, Plotly, D3.js 
    - Web Technologies      : HTML, CSS, JavaScript 
    - Tools                 : Streamlit, Snowflake, CODA, ODK, Google App Scripts,
                              ArcGIS, Tableau, PowerBI

## Certifications
    - Google   : Business Intelligence Certificate
    - Asana    : Workflow Specialist Certificate
    - ESRI     : Spatial Data Science
    - LinkedIn : The Data Science of Nonprofit Service Organizations

<p>If you want your organization to think in systems and act on evidence while staying deeply human — let’s collaborate.  
<a href="mailto:rawringriha@gmail.com">Click here or copy this email ID: rawringriha@gmail.com</a></p>


</div>

<div class="timeline-column" id="timeline-column">
  <div class="timeline-placeholder">Professional Experience.</div>

  <div class="timeline-entry">
    <div class="timeline-year">Jun 2025 – Present</div>
    <button class="timeline-org" aria-expanded="false">
      ShhorAI
      <span class="timeline-role">Lead — Data & Strategy</span>
    </button>
    <div class="timeline-details">
      Designing wellbeing frameworks and linking ecological, economic, and cultural indicators.<br>
      Leading projects on climate resilience and indigenous restoration models.
    </div>
  </div>

  <div class="timeline-entry">
    <div class="timeline-year">Jan 2024 – May 2025</div>
    <button class="timeline-org" aria-expanded="false">
      Earthtree (Earthbanc)
      <span class="timeline-role">Senior Business Analyst</span>
    </button>
    <div class="timeline-details">
      Built low-resource data systems connecting field and executive teams.<br>
      Created impact evaluation frameworks and contributed to securing ~₹40M in climate and conservation grants.
    </div>
  </div>

  <div class="timeline-entry">
    <div class="timeline-year">May 2022 – Dec 2023</div>
    <button class="timeline-org" aria-expanded="false">
      Balipara Foundation
      <span class="timeline-role">Lead — Grants & Impact</span>
    </button>
    <div class="timeline-details">
      Designed M&E systems improving decision-making efficiency by 50%.<br>
      Trained 25+ staff and developed community-led metrics for biodiversity-linked livelihoods.
    </div>
  </div>

  <div class="timeline-entry">
    <div class="timeline-year">May 2021 – Apr 2022</div>
    <button class="timeline-org" aria-expanded="false">
      VOICE 4 Girls
      <span class="timeline-role">Monitoring & Evaluation Officer</span>
    </button>
    <div class="timeline-details">
      Conducted impact evaluations, supported research publications, and led data analysis for program outcomes.
    </div>
  </div>
</div>

</div>

<script>
document.addEventListener('DOMContentLoaded', () => {
  const entries = document.querySelectorAll('.timeline-entry');

  entries.forEach(entry => {
    const button = entry.querySelector('.timeline-org');
    button.addEventListener('click', () => {
      const isOpen = entry.classList.toggle('open');
      button.setAttribute('aria-expanded', isOpen);
    });
  });
});
</script>

