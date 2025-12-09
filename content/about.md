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
}

/* Entry */
.timeline-entry {
  margin-bottom: 1.5rem;
  position: relative;
}

.timeline-entry::before {
  content: '';
  position: absolute;
  left: -12px;
  top: 6px;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--accent);
}

/* Date */
.timeline-year {
  color: var(--text-secondary);
  font-weight: 600;
  margin-bottom: 0.2rem;
}

/* Org + Role on separate lines */
.timeline-org {
  display: block;
  font-weight: 600;
  cursor: pointer;
  background: none;
  border: none;
  padding: 0;
  color: var(--accent);
  text-align: left;
}

.timeline-role {
  display: block;
  color: var(--yellow, #f0d674);
  font-style: italic;
  margin-top: 0.1rem;
}

/* Accordion content */
.timeline-details {
  max-height: 0;
  overflow: hidden;
  opacity: 0;
  margin-top: 0.3rem;
  transition:
    max-height 0.35s ease,
    opacity 0.25s ease;
}

/* Bullet points inside details */
.timeline-details ul {
  padding-left: 1.2rem;
}

.timeline-details li {
  margin-bottom: 0.5rem;
}

/* When open */
.timeline-entry.open .timeline-details {
  max-height: 500px; /* enough space for items */
  opacity: 1;
}

.timeline-placeholder {
  color: var(--text-secondary);
  font-style: italic;
  font-size: 1.1rem;      /* make it visually distinct */
  opacity: 0.8;
  margin-bottom: 1.2rem;
  display: block;         /* prevents inline collapsing */
}

.cv-download a {
  display: inline-block;
  padding: 0.5rem 1rem;
  background: var(--accent);
  color: var(--background);
  text-decoration: none;
  border-radius: 6px;
  font-weight: 600;
  margin-top: 1rem;
  transition: background 0.2s ease;
}

.cv-download a:hover {
  background: var(--accent-alt);
}



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

<div class="cv-download">
  <a href="/files/Detailed_Resume_Harikrishnan_P.pdf" download> ↓ Download CV </a>
</div>


<p>If you want your organization to think in systems and act on evidence while staying deeply human — let’s collaborate.  
<a href="mailto:rawringriha@gmail.com">Click here or copy this email ID: rawringriha@gmail.com</a></p>


</div>

<div class="timeline-column" id="timeline-column">
  <div class="timeline-placeholder">Professional Experience.</div>

  <div class="timeline-entry">
    <div class="timeline-year">Jun 2025 – Present</div>
    <button class="timeline-org" aria-expanded="false">
      ShhorAI
      <span class="timeline-role">Senior Consultant (Contract) — Data & Strategy</span>
    </button>
    <div class="timeline-details">
      Supporting analysis and creation of India’s first large-scale proprietary AI-tagged cross-platform hate speech evidence-base, contributing to an open-source report on online abuse trends.
    </div>
  </div>

  <div class="timeline-entry">
    <div class="timeline-year">Jan 2024 – May 2025</div>
    <button class="timeline-org" aria-expanded="false">
      Earthtree (Earthbanc)
      <span class="timeline-role">Senior Business Analyst</span>
    </button>
    <div class="timeline-details">
      <ul>
        <li>Led analytics for ARR (afforestation, reforestation, restoration) projects, identifying systemic bottlenecks and boosting efficiency by 40%.</li>
        <li>Designed Python-Snowflake dashboards to simplify complex datasets, reducing reporting time by 50% for senior leadership.</li>
        <li>Built feedback systems that improved data quality by 60%, strengthening monitoring of sustainability indicators and executive planning.</li>
        <li>Conducted process mapping and internal audits to bridge operations and tech, ensuring reliable reporting for C-suite executives.</li>
      </ul>
    </div>
  </div>

  <div class="timeline-entry">
    <div class="timeline-year">May 2022 – Dec 2023</div>
    <button class="timeline-org" aria-expanded="false">
      Balipara Foundation
      <span class="timeline-role">Lead — Grants & Impact</span>
    </button>
    <div class="timeline-details">
      <ul>
        <li>Built low-resource data systems connecting field and executive teams.</li>
        <li>Created impact evaluation frameworks and contributed to securing ~₹40M in climate and conservation grants.</li>
        <li>Designed wellbeing frameworks and linking ecological, economic, and cultural indicators.</li>
        <li>Lead projects on climate resilience and indigenous restoration models.</li>
      </ul>  
    </div>
  </div>

  <div class="timeline-entry">
    <div class="timeline-year">May 2021 – Apr 2022</div>
    <button class="timeline-org" aria-expanded="false">
      VOICE 4 Girls
      <span class="timeline-role">Monitoring & Evaluation Officer</span>
    </button>
    <div class="timeline-details">
      <ul>
        <li>Led longitudinal research surveys of 8,000+ students to track program effectiveness.</li>
        <li>Conducted impact evaluations, supported research publications, and led data analysis for program outcomes.</li>
      </ul>   
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
      const isOpen = entry.classList.contains('open');

      // Close all entries
      entries.forEach(e => e.classList.remove('open'));

      // If the clicked one wasn’t open, open it
      if (!isOpen) entry.classList.add('open');
    });
  });
});

/* Convert details text into bullet lines automatically */
document.querySelectorAll('.timeline-details').forEach(details => {
  
  const raw = details.textContent.trim();

  // Split by periods but keep the period
  const lines = raw
    .split(/(?<=\.)\s+/)  // split on period+space
    .filter(line => line.trim().length > 0);

  details.innerHTML = lines
    .map(line => `<span>${line.trim()}</span>`)
    .join('');
});


</script>

