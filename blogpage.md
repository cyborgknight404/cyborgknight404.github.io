---
layout: default
title: Blog
permalink: /blog
---

{% raw %}
<div class="blog-wrapper">

  <aside class="blog-sidebar">
    <h2>🗂️ Topics</h2>
    <ul>
      <li><a href="#">Certifications</a></li>
      <li><a href="#">Labs & Tools</a></li>
      <li><a href="#">Platform Reviews</a></li>
      <li><a href="#">SOC Skill-Building</a></li>
    </ul>
  </aside>

  <section class="blog-content">
    <h1>📝 Cybersecurity Blog</h1>
    <p>This is where I reflect, document, and share what I’m building and learning.</p>

    <div class="card">
      <h3>🔐 Google Cybersecurity Certificate Review</h3>
      <p>My breakdown of the Google Cybersecurity Certificate: what’s solid, what’s fluff, and how I used it to launch lab work.</p>
      <a href="/posts/google-cybersecurity-cert-review">Read More →</a>
    </div>

    <div class="card">
      <h3>🧠 Hack The Box: First Impressions</h3>
      <p>What HTB’s new blue team modules look like, and how I’m using them to reinforce detection workflows in my lab.</p>
      <a href="/posts/hack-the-box-first-look">Read More →</a>
    </div>
  </section>

</div>

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

.blog-sidebar ul {
  list-style: none;
  padding-left: 0;
}

.blog-sidebar li {
  margin-bottom: 0.75rem;
}

.blog-sidebar a {
  text-decoration: none;
  font-weight: bold;
  color: #333;
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

  .blog-sidebar {
    width: 100%;
    margin-bottom: 1rem;
  }
}

</style>
{% endraw %}
