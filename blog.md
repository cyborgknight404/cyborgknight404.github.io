---
layout: default
title: Blog
description: Thoughts, writeups, and lessons learned
permalink: /blog
---

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
      <button data-filter="osint">OSINT</button>
      <button data-filter="popculture">Pop Culture</button>
      <button data-filter="social-engineering">Social Engineering</button>
    </div>
  </aside>

  <!-- MAIN BLOG CONTENT -->
  <section class="blog-content">
    <h1>📝 Cybersecurity Blog</h1>
    <p>This is where I reflect, document, and share what I’m building and learning.</p>

    {% for post in site.posts %}
      <div class="card" data-tags="{{ post.tags | join: ' ' }}">
        <div class="card-flex">
          <div class="card-text">
            <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
            <p class="post-date">📅 {{ post.date | date: "%B %e, %Y" }}</p>
            <p>{{ post.description }}</p>
            <a href="{{ post.url }}">Read More →</a>
          </div>
          {% if post.image %}
            <img src="{{ post.image }}" alt="{{ post.title }} badge" class="card-thumb">
          {% endif %}
        </div>
      </div>
    {% endfor %}
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

.card-flex {
  display: flex;
  align-items: stretch;
  gap: 1.5rem;
  justify-content: space-between;
  flex-wrap: wrap;
}

.card-thumb {
  width: 140px;
  height: auto;
  max-height: 100%;
  border-radius: 8px;
  flex-shrink: 0;
  object-fit: contain;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}

.card-text {
  flex: 1;
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

  .card-text h3 a {
    color: inherit;
    text-decoration: none;
  }
  
  .card-text h3 a:hover {
    text-decoration: underline;
    color: #007acc;
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
