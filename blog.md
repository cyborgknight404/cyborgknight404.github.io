---
layout: default
title: Blog
---

{% raw %}

<!-- BLOG LAYOUT START -->
<div class="blog-layout">

  <!-- SIDEBAR SECTION -->
  <aside class="sidebar">
    <h2>🗂️ Blog Topics</h2>
    <ul>
      <li><a href="#">Certifications</a></li>
      <li><a href="#">Hands-On Labs</a></li>
      <li><a href="#">Training Reviews</a></li>
      <li><a href="#">SOC Skills</a></li>
    </ul>
  </aside>

  <!-- MAIN CONTENT SECTION -->
  <section class="content">
    <h1>📝 Cybersecurity Blog</h1>
    <p>This is where I reflect, document, and share what I’m building and breaking.</p>

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

<!-- STYLES FOR BLOG PAGE -->
<style>
/* Layout Structure */
.blog-layout {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 2rem;
  flex-wrap: nowrap;
}

/* Sidebar Styling */
.sidebar {
  width: 220px;
  flex-shrink: 0;
  background: #f0f0f0;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 1px 5px rgba(0,0,0,0.05);
}

.sidebar h2 {
  margin-top: 0;
}

.sidebar ul {
  list-style: none;
  padding-left: 0;
}

.sidebar li {
  margin-bottom: 0.75rem;
}

.sidebar a {
  text-decoration: none;
  font-weight: bold;
  color: #333;
}

/* Blog Post Content Area */
.content {
  flex-grow: 1;
  min-width: 0;
}

/* Blog Post Cards */
.card {
  background: #fff;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  border-radius: 8px;
}

/* Responsive Layout for Smaller Screens */
@media screen and (max-width: 768px) {
  .blog-layout {
    flex-direction: column;
  }

  .sidebar {
    width: 100%;
    margin-bottom: 1rem;
  }
}
</style>

{% endraw %}
