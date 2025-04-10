---
layout: default
title: Blog
---

{% raw %}
<!-- BLOG LAYOUT START -->
<div class="blog-wrapper">

  <!-- SIDEBAR NAVIGATION -->
  <aside class="blog-sidebar">
    <h2>🗂️ Topics</h2>
    <ul>
      <li><a href="#">Certifications</a></li>
      <li><a href="#">Labs & Tools</a></li>
      <li><a href="#">Platform Reviews</a></li>
      <li><a href="#">SOC Skill-Building</a></li>
    </ul>
  </aside>

  <!-- MAIN BLOG CONTENT -->
  <section class="blog-content">
    <h1>📝 Cybersecurity Blog</h1>
    <p>This is where I reflect, document, and share what I’m building and learning.</p>

    <div class="card">
      <h3>🔐 Google Cybersecurity Certificate Review</h3>
      <p>Breakdown of the course, key takeaways, and how I’m applying it in my lab.</p>
      <a href="/_posts/2025-04-10-google-cybersecurity-cert-review.md">Read More →</a>
    </div>

    <div class="card">
      <h3>🧠 First Impressions of Hack The Box Training</h3>
      <p>What HTB's blue team training offers, and how it helps build detection skills.</p>
      <a href="/_posts/2025-04-11-hack-the-box-first-look.md">Read More →</a>
    </div>
  </section>

</div>
<!-- BLOG LAYOUT END -->

<!-- BLOG PAGE STYLES -->
<style>
.blog-wrapper {
  display: flex;
  flex-direction: row;
  gap: 2rem;
  flex-wrap: wrap;
}

.blog-sidebar {
  flex: 0 0 220px;
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
  flex: 1 1 600px;
}

.card {
  background: #fff;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  border-radius: 8px;
}

/* Responsive Fix */
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
