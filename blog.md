---
layout: default
title: Blog
---

{% raw %}
<!-- === Blog Page Layout with Sidebar & Preview Cards === -->

<div class="blog-wrapper">

  <!-- Sidebar Section -->
  <aside class="blog-sidebar">
    <h2>🗂️ Topics</h2>
    <ul>
      <li><a href="#">Certifications</a></li>
      <li><a href="#">Labs & Tools</a></li>
      <li><a href="#">Platform Reviews</a></li>
      <li><a href="#">SOC Skill-Building</a></li>
    </ul>
  </aside>

  <!-- Blog Post Previews -->
  <section class="blog-content">
    <h1>📝 Cybersecurity Blog</h1>
    <p>Insights, reflections, and hands-on writeups from the trenches of blue team learning and home lab projects.</p>

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

<!-- === Styles for Sidebar + Cards === -->
<style>
.blog-wrapper {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
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
