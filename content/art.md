---
title: "Art"
readingTime: false
Toc: false
draft: false
---

---

<style>
/* Filter buttons */
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

/* Masonry grid layout */
.gallery {
  column-count: 3;
  column-gap: 0;
  width: 100%;
}
.gallery img {
  width: 100%;
  height: auto;
  display: inline-block;
  margin: 0;
  padding: 0;
  border: none !important;
  break-inside: avoid;
  cursor: pointer;
  opacity: 0;
  transition: opacity 0.6s ease-in;
}
.gallery img[src] {
  opacity: 1;
}

/* Responsive */
@media (max-width: 1024px) {
  .gallery { column-count: 2; }
}
@media (max-width: 600px) {
  .gallery { column-count: 1; }
}

/* Lightbox overlay */
#lightbox {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.9);
  display: none;
  align-items: center;
  justify-content: center;
  z-index: 9999;
}
#lightbox img {
  max-width: 90%;
  max-height: 90%;
  border: none;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.6);
}
#lightbox:target {
  display: flex;
}
#lightbox-close {
  position: fixed;
  top: 20px;
  right: 30px;
  font-size: 2rem;
  color: white;
  cursor: pointer;
  text-decoration: none;
}
</style>

<!-- Filter buttons -->
<div class="filter-buttons">
  <button class="active" data-filter="all">All</button>
  <button data-filter="digital">Digital</button>
  <button data-filter="sketch">Sketch</button>
  <button data-filter="mixed">Mixed Media</button>
</div>

<!-- Art gallery -->
<div class="gallery">
  <img src="/img/art/1.jpg" data-tags="sketch" alt="Sketch 1">
  <img src="/img/art/2.png" data-tags="sketch" alt="Sketch 2">
  <img src="/img/art/3.png" data-tags="sketch" alt="Sketch 3">
  <img src="/img/art/4.png" data-tags="sketch" alt="Sketch 4">
  <img src="/img/art/5.jpg" data-tags="sketch" alt="Sketch 5">
  <img src="/img/art/6.png" data-tags="sketch" alt="Sketch 2">
  <img src="/img/art/7.jpg" data-tags="sketch" alt="Sketch 3">
  <img src="/img/art/8.png" data-tags="sketch" alt="Sketch 4">
</div>

<!-- Lightbox container -->
<div id="lightbox">
  <a id="lightbox-close">&times;</a>
  <img src="" alt="Expanded artwork">
</div>

<script>
document.addEventListener('DOMContentLoaded', () => {
  const buttons = document.querySelectorAll('.filter-buttons button');
  const images = document.querySelectorAll('.gallery img');
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = lightbox.querySelector('img');
  const closeBtn = document.getElementById('lightbox-close');

  // Filtering logic
  buttons.forEach(btn => {
    btn.addEventListener('click', () => {
      buttons.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;

      images.forEach(img => {
        img.style.display = (filter === 'all' || img.dataset.tags.includes(filter)) ? 'inline-block' : 'none';
      });
    });
  });

  // Lightbox logic
  images.forEach(img => {
    img.addEventListener('click', () => {
      lightbox.style.display = 'flex';
      lightboxImg.src = img.src;
    });
  });

  closeBtn.addEventListener('click', () => {
    lightbox.style.display = 'none';
  });

  lightbox.addEventListener('click', e => {
    if (e.target === lightbox) {
      lightbox.style.display = 'none';
    }
  });
});
</script>
