---
title: "My Writing"
readingTime: false
Toc: false
draft: false
---

<style>
/* Filter buttons */
.writing-filters {
  margin-bottom: 1.2rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.writing-filters button {
  background: none;
  border: 1px solid var(--accent);
  color: var(--accent);
  padding: 0.35rem 0.7rem;
  border-radius: 5px;
  font-size: 0.9rem;
  cursor: pointer;
}

.writing-filters button.active,
.writing-filters button:hover {
  background: var(--accent);
  color: var(--background);
}

/* Writing blocks */
.writing-item {
  margin-bottom: 2rem;
}

.writing-item h2 {
  margin-bottom: 0.3rem;
}

.writing-tags {
  color: var(--text-secondary);
  font-size: 0.85rem;
  margin-bottom: 0.4rem;
}
</style>

<div class="writing-filters">
  <button class="active" data-filter="all">All</button>
  <button data-filter="ecology">Ecology</button>
  <button data-filter="systems">Systems Thinking</button>
  <button data-filter="field">Field Notes</button>
  <button data-filter="data">Data + Society</button>
  <button data-filter="collab">Collaboration</button>
  <button data-filter="hate">Online Hate Speech</button>
</div>

<div id="writing-list">

<div class="writing-item" data-tags="ecology field collab">
  
## Creating wellbeing on the frontlines of climate and biodiversity crisis
<div class="writing-tags">Tags: ecology, field, collab</div>
On how indigenous communities in India’s Eastern Himalayas are redefining prosperity through nature-positive economies that heal both people and forests. (Page 23–27)

[Read →](https://doc-14-28-apps-viewer.googleusercontent.com/viewer/secure/pdf/jmhvstventbgrh9a6e65dkcii5foq8p3/i1iptuj55tncdootg48pffffp9a85isn/1762197600000/lantern/09001582930696203960/ACFrOgCnB3O55eeAyTbHzxlC31ZE3_-w7UPwE7aK27pyP8SJQ7ylsTAUziDWrJlKfXy2o5Exg6wp6c0QN_qMG7QkZ-pNkf1FjSC5fg_VoRzMmAzeJ9qenYBYGJ2KJKV5qbZQZwhFRuw83F1cNj_A?print=true&nonce=3r7tef1jgqh8e&user=09001582930696203960&hash=ecr2o0stqa4t0l05e4h72dkqhif95n87)
</div>

---

<div class="writing-item" data-tags="collab hate data">
  
## Overlap between communal and electoral hate speech
<div class="writing-tags">Tags: collab, hate, data</div>
In the wake of cases of blatant hate speech by prominent leaders, Shhor Al analyses Election-related online hate. Here's what we found!

[Read →](https://www.instagram.com/p/C6G5gvVyh6t/?utm_source=ig_web_copy_link&igsh=MzRlODBiNWFlZA==)
</div>

---

<div class="writing-item" data-tags="hate collab data">
  
## Shhor Al asks, how safe is the internet for women?
<div class="writing-tags">Tags: hate, collab, data</div>


[Read →](https://www.instagram.com/p/C4Ql09BxFB6/?utm_source=ig_web_copy_link&igsh=MzRlODBiNWFlZA==)
</div>

</div>

<script>
document.addEventListener("DOMContentLoaded", () => {
  const buttons = document.querySelectorAll(".writing-filters button");
  const items = document.querySelectorAll(".writing-item");

  buttons.forEach(btn => {
    btn.addEventListener("click", () => {
      buttons.forEach(b => b.classList.remove("active"));
      btn.classList.add("active");

      const filter = btn.dataset.filter;

      items.forEach(item => {
        const tags = item.dataset.tags.split(" ");
        item.style.display = (filter === "all" || tags.includes(filter))
          ? "block"
          : "none";
      });
    });
  });
});
</script>

---

*More essays are being edited, polished, and quietly queued for release. Stay tuned.*
