---
title: "Art-Sci /.."
readingTime: false
Toc: false
draft: false
---

Visual work and design that lives between data and art — presentations, panels, posters, and illustrated reports.  
Click any piece to open it in full.

---

<style>
/* ── Grid ─────────────────────────────────────────── */
.design-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}

/* ── Card ─────────────────────────────────────────── */
.design-card {
  border: 1px solid var(--accent);
  border-radius: 10px;
  overflow: hidden;
  background-color: var(--background-secondary);
  text-decoration: none;
  color: inherit;
  display: block;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.design-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 6px 20px rgba(0,0,0,0.25);
  text-decoration: none;
  color: inherit;
}

/* ── Thumbnail ────────────────────────────────────── */
.design-card .thumb-wrap {
  width: 100%;
  aspect-ratio: 16 / 9;
  overflow: hidden;
  background: var(--background);
}

.design-card .thumb-wrap img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.35s ease;
}

.design-card:hover .thumb-wrap img {
  transform: scale(1.04);
}

/* ── Card body ────────────────────────────────────── */
.design-card .card-body {
  padding: 1rem;
}

.design-card h3 {
  margin: 0 0 0.4rem;
  font-size: 1rem;
  line-height: 1.35;
}

.design-card .card-type {
  font-size: 0.78rem;
  font-weight: 600;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 0.5rem;
  display: block;
}

.design-card .card-desc {
  font-size: 0.875rem;
  color: var(--text-secondary);
  line-height: 1.5;
  margin: 0;
}

.design-card .card-meta {
  font-size: 0.78rem;
  color: var(--text-secondary);
  margin-top: 0.6rem;
  font-style: italic;
}
</style>

<div class="design-grid">

  <a class="design-card" href="/design/pangolin-sijimali">
    <div class="thumb-wrap">
      <img src="/img/design/pangolin-sijimali/pangolin-thumb.png" alt="Pangolin thumbnail">
    </div>
    <div class="card-body">
      <span class="card-type">Poster · Social Media</span>
      <h3>Pangolins of Sijimali</h3>
      <p class="card-meta">Added: April 2026</p>
    </div>
  </a>

 <a class="design-card" href="/design/red_lapwing">
    <div class="thumb-wrap">
      <img src="/img/design/red_lapwing/lapwing_thumbnail.png" alt="Lapwing thumbnail">
    </div>
    <div class="card-body">
      <span class="card-type">Infographic · Panel</span>
      <h3>Red Wattled Lapwing</h3>
      <p class="card-meta">Added: April 2026</p>
    </div>
  </a>

</div>

---

*More visual work in progress — posters, panel graphics, and illustrated essays.*