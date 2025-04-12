---
layout: default
title: Blog
description: Thoughts, writeups, and lessons learned
permalink: /blog
---

{% raw %}
<div class="blog-wrapper">

  <!-- SIDEBAR WITH TAG FILTER -->
  <aside class="blog-sidebar">
    <h2>🗂️ Filter by Tag</h2>
    <div class="tag-filter">
      <button data-filter="all" class="active">All</button>
      <button data-filter="certification">Certification</button>
      <button data-filter="training">Training</button>
      <button data-filter="labs">Labs</button>
      <button data-filter="blue-team">Blue Team</button>
      <button data-filter="python">Python</button>
      <button data-filter="detection">Detection</button>
      <button data-filter="homelab">Homelab</button>
    </div>
  </aside>

  <!-- MAIN BLOG CONTENT -->
  <section class="blog-content">
    <h1>📝 Cybersecurity Blog</h1>
    <p>This is where I reflect, document, and share what I’m building and learning.</p>
    
    <div class="card" data-tags="film-analysis war-games popculture osint ai social-engineering automation">
      <h3>🎮 WarGames (1983): What a Teen Hacker Still Teaches Us About Cybersecurity</h3>
      <p class="post-date">📅 April 11, 2025</p>
      <p>Classic movie, timeless lessons. From social engineering to automation run amok, this breakdown       shows how *WarGames* still maps to modern cybersecurity principles.</p>
      <a href="/posts/war-games-cybersecurity-lessons">Read More →</a>
    </div>
    
    <div class="card" data-tags="certification training beginner google">
      <h3>🔐 Google Cybersecurity Certificate Review</h3>
      <p class="post-date">📅 April 10, 2025</p>
      <p>My breakdown of the Google Cybersecurity Certificate: what’s solid, what’s fluff, and how I used it to launch lab work.</p>
      <a href="/posts/google-cybersecurity-cert-review">Read More →</a>
    </div>

    <div class="card" data-tags="labs blue-team training hackthebox">
      <h3>🧠 Hack The Box: First Impressions</h3>
      <p class="post-date">📅 April 10, 2025</p>
      <p>What HTB’s blue team training offers, and how it helps build detection skills.</p>
      <a href="/posts/hack-the-box-first-look">Read More →</a>
    </div>

    <div class="card" data-tags="lab hardware proxmox blue-team homelab">
      <h3>⚙️ Proxmox Lab Build Log</h3>
      <p class="post-date">📅 April 10, 2025</p>
      <p>From junk hardware to a functioning lab: how I built a full Proxmox-based blue team environment at home.</p>
      <a href="/posts/proxmox-lab-build">Read More →</a>
    </div>

    <div class="card" data-tags="tool python log-analysis detection scripting">
      <h3>🔍 Log Parser Tool (Python)</h3>
      <p class="post-date">📅 April 10, 2025</p>
      <p>Scan syslogs for suspicious activity using a simple Python script I built to sharpen my detection skills.</p>
      <a href="/posts/log-parser-tool">Read More →</a>
    </div>
  </section>

</div>

<!-- STYLES -->
<style>
.blog-wrapper {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 2rem;
  flex-wrap: nowrap;
}

.blog-sidebar {
  width: 220px;
  flex-shrink: 0;
  background: #f0f0f0;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 1px 5px rgba(0,0,0,0.05);
}

.blog-sidebar h2 {
  margin-top: 0;
}

.tag-filter {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.tag-filter button {
  background: #ddd;
  border: none;
  padding: 0.5rem;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  text-align: left;
  transition: background 0.2s ease;
}

.tag-filter button:hover,
.tag-filter button.active {
  background: #333;
  color: #fff;
}

.blog-content {
  flex-grow: 1;
  min-width: 0;
}

.card {
  background: #fff;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  border-radius: 8px;
}

@media screen and (max-width: 768px) {
  .blog-wrapper {
    flex-direction: column;
  }

  .blog-sidebar,
  .blog-content {
    width: 100%;
    padding: 1rem;
  }

  .card {
    font-size: 1.1rem;
    padding: 1.25rem;
  }

  .card h3 {
    font-size: 1.3rem;
  }

  .card a {
    font-size: 1.05rem;
  }

  .tag-filter {
    flex-direction: row;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .tag-filter button {
    flex: 1 1 auto;
    text-align: center;
  }
}
</style>

<!-- FILTER SCRIPT -->
<script>
  const filterButtons = document.querySelectorAll('.tag-filter button');
  const cards = document.querySelectorAll('.card');

  filterButtons.forEach(button => {
    button.addEventListener('click', () => {
      const tag = button.dataset.filter;

      filterButtons.forEach(btn => btn.classList.remove('active'));
      button.classList.add('active');

      cards.forEach(card => {
        const tags = card.dataset.tags.split(" ");
        const show = tag === "all" || tags.includes(tag);
        card.style.display = show ? "block" : "none";
      });
    });
  });
</script>
{% endraw %}
