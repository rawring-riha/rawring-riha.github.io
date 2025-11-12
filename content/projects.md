---
title: "Projects /.."
readingTime: false
Toc: false
draft: false
---


A curated collection of projects exploring data, systems, and storytelling through code.  
Each project includes links to the **GitHub repo**, a **live demo** (if deployed), and a **write-up** for deeper context.  
Newest projects appear first.

---

<style>
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}
.project-card {
  border: 1px solid var(--accent);
  border-radius: 10px;
  padding: 1rem;
  background-color: var(--background-secondary);
}
.project-card img {
  width: 100%;
  border-radius: 6px;
  margin-bottom: 0.8rem;
}
.project-buttons {
  margin-top: 0.8rem;
}
.project-buttons a {
  display: inline-block;
  padding: 0.4rem 0.8rem;
  margin-right: 0.5rem;
  border-radius: 5px;
  background: var(--accent);
  color: var(--background);
  text-decoration: none;
  font-weight: 600;
  font-size: 0.9rem;
}
.project-buttons a:hover {
  background: var(--accent-alt);
}
</style>



<div class="project-grid">

<div class="project-card">
  <img src="/img/projects/chord_diagram_story.png" alt="Chord Diagram Story Visualization Screenshot">
  <h3>Intersections of Hate — Chord Diagram Story</h3>
  <p>A scrollytelling data visualization built with <code>D3.js</code> that explores the interconnected nature of online hate speech.  
  As users scroll, the chord diagram transitions through stages — highlighting how sexist, political, and communal hate speech overlap across narratives.</p>
  <p><strong>Tech:</strong> D3.js, JavaScript, HTML, CSS, Data Visualization, Scrollytelling UX</p>
  <p><em>Added:</em> Nov 2025</p>
  <div class="project-buttons">
    <a href="https://github.com/rawring-riha/intersections-of-hate" target="_blank">GitHub</a>
    <a href="#" target="_blank">Live Demo</a>
    <a href="#" target="_blank">Write-up</a>
  </div>
</div>

<div class="project-card">
  <img src="/img/projects/portfolio_site.png" alt="rawring-riha personal site screenshot">
  <h3>rawring-riha — Personal Portfolio</h3>
  <p>A minimalist personal site built with <code>Hugo</code> and customized from the <code>Terminal</code> theme.  
  Designed for clarity and speed, it showcases data-driven storytelling, research, and creative work — wrapped in a clean, command-line aesthetic.</p>
  <p><strong>Tech:</strong> Hugo, HTML, CSS, GitHub Actions, Markdown</p>
  <p><em>Added:</em> Nov 2025</p>
  <div class="project-buttons">
    <a href="https://github.com/rawring-riha/rawring-riha.github.io" target="_blank">GitHub</a>
    <a href="https://rawring-riha.github.io/" target="_blank">Live Site</a>
    <a href="#" target="_blank">Write-up</a>
  </div>
</div>


<div class="project-card">
  <img src="/img/projects/sweetviz.png" alt="Sweetviz EDA App Screenshot">
  <h3>Sweetviz EDA App</h3>
  <p>An interactive web app that automates exploratory data analysis using <code>Sweetviz</code> and <code>Streamlit</code>.</p>
  <p><strong>Tech:</strong> Python, Streamlit, Pandas</p>
  <p><em>Added:</em> Oct 2025</p>
  <div class="project-buttons">
    <a href="https://github.com/rawring-riha/sweetviz_eda_app" target="_blank">GitHub</a>
    <a href="https://eda-sweetviz.streamlit.app/" target="_blank">Live Demo</a>
    <a href="https://www.linkedin.com/pulse/democratising-data-social-sector-one-app-time-harikrishnan-p-rtrxc/" target="_blank">Write-up</a>
  </div>
</div>


<div class="project-card">
  <img src="/img/projects/ab_testing.png" alt="A/B Testing Dashboard Screenshot">
  <h3>A/B Testing simulation</h3>
  <p>This project offers an interactive dashboard built in <code>Streamlit</code> that explores Airbnb listing data, simulates feature-level <code>A/B tests</code>, and monitors data quality.</p>
  <p><strong>Tech:</strong> Python, SciPy, Plotly, Flask</p>
  <p><em>Added:</em> Oct 2025</p>
  <div class="project-buttons">
    <a href="https://github.com/rawring-riha/ab_testing" target="_blank">GitHub</a>
    <a href="https://www.linkedin.com/pulse/bridging-social-research-data-science-running-ab-style-harikrishnan-p-0xzrc/" target="_blank">Write-up</a>
  </div>
</div>

<div class="project-card">
  <img src="/img/projects/kenya_mapper.png" alt="Kenya Travel Risk Mapper Screenshot">
  <h3>Kenya Travel Risk Mapper</h3>
  <p>A tool to map and analyze travel risks across Kenya using public datasets and APIs.</p>
  <p><strong>Tech:</strong> Python, GeoPandas, Folium, Plotly</p>
  <p><em>Added:</em> Jan 2025</p>
  <div class="project-buttons">
    <a href="https://github.com/rawring-riha/kenya-travel-risk-mapper" target="_blank">GitHub</a>
  </div>
</div>

</div>

<style>
  /* Hide all project cards after the fourth one */
  .project-card:nth-of-type(n+5) {
    display: none;
  }

  /* Style for the "Show More" button */
  #show-more-btn {
    display: inline-block;
    margin: 2rem auto;
    padding: 0.6rem 1.2rem;
    border: none;
    border-radius: 6px;
    background: var(--accent);
    color: var(--background);
    font-weight: 600;
    cursor: pointer;
    font-size: 1rem;
    transition: background 0.3s ease;
  }

  #show-more-btn:hover {
    background: var(--accent-alt);
  }

  /* Optional fade-in animation when showing more cards */
  .fade-in {
    animation: fadeIn 0.5s ease-in-out forwards;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }
</style>

<div style="text-align: center;">
  <button id="show-more-btn">See more ↓</button>
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const cards = document.querySelectorAll('.project-card');
    const button = document.getElementById('show-more-btn');
    let showingAll = false;

    button.addEventListener('click', () => {
      if (!showingAll) {
        cards.forEach(card => {
          card.style.display = 'block';
          card.classList.add('fade-in');
        });
        button.textContent = 'Show less ↑';
        showingAll = true;
      } else {
        cards.forEach((card, i) => {
          if (i >= 4) card.style.display = 'none';
        });
        button.textContent = 'See more ↓';
        showingAll = false;
      }
    });
  });
</script>


---

*More projects are in progress — including open-source tools for field data systems, automation, and ecological analytics.*

