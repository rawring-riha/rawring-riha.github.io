---
title: "Photography"
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

/* Masonry grid */
.photo-grid {
  column-count: 4;
  column-gap: 0;
  width: 100%;
}
.photo-grid img {
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
.photo-grid img[src] {
  opacity: 1;
}

/* Responsive */
@media (max-width: 1280px) {
  .photo-grid { column-count: 3; }
}
@media (max-width: 900px) {
  .photo-grid { column-count: 2; }
}
@media (max-width: 600px) {
  .photo-grid { column-count: 1; }
}

/* Lightbox overlay */
#lightbox {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(255, 255, 255, 0.95);
  display: none;
  align-items: center;
  justify-content: center;
  z-index: 9999;
}
#lightbox img {
  max-width: 92%;
  max-height: 92%;
  border: 1px solid #ddd;
  box-shadow: 0 0 25px rgba(0, 0, 0, 0.2);
}
#lightbox:target {
  display: flex;
}
#lightbox-close {
  position: fixed;
  top: 20px;
  right: 30px;
  font-size: 2rem;
  color: #222;
  cursor: pointer;
  text-decoration: none;
}
</style>

<!-- Filter buttons -->
<div class="filter-buttons">
  <button class="active" data-filter="all">All</button>
  <button data-filter="nature">Nature</button>
  <button data-filter="urban">Urban</button>
  <button data-filter="portraits">Portraits</button>
  <button data-filter="travel">Travel</button>
</div>

<!-- Photography grid -->
<div class="photo-grid">
  <img src="/img/photography/1.jpg">
  <img src="/img/photography/2.jpg">
  <img src="/img/photography/3.jpg">
  <img src="/img/photography/4.jpg">
  <img src="/img/photography/5.jpg">
  <img src="/img/photography/6.jpg">
  <img src="/img/photography/7.jpg">
  <img src="/img/photography/8.jpg">
  <img src="/img/photography/9.jpg">
  <img src="/img/photography/10.jpg">
  <img src="/img/photography/11.jpg">
  <img src="/img/photography/12.jpg">
  <img src="/img/photography/13.jpg">
  <img src="/img/photography/14.jpg">
  <img src="/img/photography/15.jpg">
  <img src="/img/photography/16.jpg">
  <img src="/img/photography/17.jpg">
  <img src="/img/photography/18.jpg">
  <img src="/img/photography/19.jpg">
  <img src="/img/photography/20.jpg">
  <img src="/img/photography/21.jpg">
  <img src="/img/photography/22.jpg">
  <img src="/img/photography/23.jpg">
  <img src="/img/photography/24.jpg">
  <img src="/img/photography/25.jpg">
  <img src="/img/photography/26.jpg">
  <img src="/img/photography/27.jpg">
  <img src="/img/photography/28.jpg">
  <img src="/img/photography/29.jpg">
  <img src="/img/photography/30.jpg">
  <img src="/img/photography/31.jpg">
  <img src="/img/photography/32.jpg">
  <img src="/img/photography/33.jpg">
  <img src="/img/photography/34.jpg">
  <img src="/img/photography/35.jpg">
  <img src="/img/photography/36.jpg">
  <img src="/img/photography/37.jpg">
  <img src="/img/photography/38.jpg">
  <img src="/img/photography/39.jpg">
  <img src="/img/photography/40.jpg">
  <img src="/img/photography/41.jpg">
  <img src="/img/photography/42.jpg">
  <img src="/img/photography/43.jpg">
  <img src="/img/photography/44.jpg">
  <img src="/img/photography/45.jpg">
  <img src="/img/photography/46.jpg">
  <img src="/img/photography/47.jpg">
  <img src="/img/photography/48.jpg">
  <img src="/img/photography/49.jpg">
</div>


<!-- Lightbox -->
<div id="lightbox">
  <a id="lightbox-close">&times;</a>
  <img src="" alt="Expanded photograph">
</div>

<script>
document.addEventListener('DOMContentLoaded', () => {
  const buttons = document.querySelectorAll('.filter-buttons button');
  const photos = document.querySelectorAll('.photo-grid img');
  const lightbox = document.getElementById('lightbox');
  const lightboxImg = lightbox.querySelector('img');
  const closeBtn = document.getElementById('lightbox-close');

  // Filtering
  buttons.forEach(btn => {
    btn.addEventListener('click', () => {
      buttons.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');
      const filter = btn.dataset.filter;

      photos.forEach(photo => {
        photo.style.display = (filter === 'all' || photo.dataset.tags.includes(filter)) ? 'inline-block' : 'none';
      });
    });
  });

  // Lightbox
  photos.forEach(photo => {
    photo.addEventListener('click', () => {
      lightbox.style.display = 'flex';
      lightboxImg.src = photo.src;
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
