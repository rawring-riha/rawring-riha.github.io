---
title: "Photography"
readingTime: false
Toc: false
draft: false
---

Use the filters to browse themes.

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
  .photo-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 0;
  }
  .photo-grid img {
    width: 25%;
    object-fit: cover;
    display: block;
  }
  @media (max-width: 1024px) {
    .photo-grid img {
      width: 33.33%;
    }
  }
  @media (max-width: 768px) {
    .photo-grid img {
      width: 50%;
    }
  }
  @media (max-width: 500px) {
    .photo-grid img {
      width: 100%;
    }
  }
</style>

<div class="filter-buttons">
  <button class="active" data-filter="all">All</button>
  <button data-filter="nature">Nature</button>
  <button data-filter="urban">Urban</button>
  <button data-filter="portraits">Portraits</button>
</div>

<div class="photo-grid">
  <img src="/img/photography/nature_1.jpg" data-tags="nature">
  <img src="/img/photography/urban_1.jpg" data-tags="urban">
  <img src="/img/photography/portraits_1.jpg" data-tags="portraits">
  <img src="/img/photography/nature_2.jpg" data-tags="nature">
  <img src="/img/photography/urban_2.jpg" data-tags="urban">
  <img src="/img/photography/portraits_2.jpg" data-tags="portraits">
</div>

<script>
document.addEventListener('DOMContentLoaded', () => {
  const buttons = document.querySelectorAll('.filter-buttons button');
  const photos = document.querySelectorAll('.photo-grid img');

  buttons.forEach(btn => {
    btn.addEventListener('click', () => {
      buttons.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;

      photos.forEach(photo => {
        photo.style.display = (filter === 'all' || photo.dataset.tags.includes(filter)) ? 'block' : 'none';
      });
    });
  });
});
</script>
