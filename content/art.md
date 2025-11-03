---
title: "Art"
readingTime: false
Toc: false
draft: false
---


Sketches and paintings  
Filter by theme below to explore.

---

<style>
  .filter-buttons {
    margin-bottom: 1rem;
    text-align: center;
  }
  .filter-buttons button {
    background: none;
    border: 1px solid var(--accent);
    color: var(--accent);
    padding: 0.4rem 0.8rem;
    margin: 0.3rem;
    border-radius: 5px;
    cursor: pointer;
    transition: all 0.3s ease;
  }
  .filter-buttons button.active,
  .filter-buttons button:hover {
    background: var(--accent);
    color: var(--background);
  }
  .gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 0;
  }
  .gallery img {
    width: 33.33%;
    object-fit: cover;
    display: block;
  }
  @media (max-width: 768px) {
    .gallery img {
      width: 50%;
    }
  }
  @media (max-width: 500px) {
    .gallery img {
      width: 100%;
    }
  }
</style>

<div class="filter-buttons">
  <button class="active" data-filter="all">All</button>
  <button data-filter="digital">Digital</button>
  <button data-filter="sketch">Sketch</button>
  <button data-filter="mixed">Mixed Media</button>
</div>

<div class="gallery">
  <img src="/img/art/sketch_1.jpg" data-tags="sketch">
  <img src="/img/art/digital_1.jpg" data-tags="digital">
  <img src="/img/art/mixed_1.jpg" data-tags="mixed">
  <img src="/img/art/sketch_2.jpg" data-tags="sketch">
  <img src="/img/art/digital_2.jpg" data-tags="digital">
  <img src="/img/art/mixed_2.jpg" data-tags="mixed">
</div>

<script>
document.addEventListener('DOMContentLoaded', () => {
  const buttons = document.querySelectorAll('.filter-buttons button');
  const images = document.querySelectorAll('.gallery img');

  buttons.forEach(btn => {
    btn.addEventListener('click', () => {
      buttons.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;

      images.forEach(img => {
        img.style.display = (filter === 'all' || img.dataset.tags.includes(filter)) ? 'block' : 'none';
      });
    });
  });
});
</script>
