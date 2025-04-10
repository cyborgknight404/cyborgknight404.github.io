---
layout: page
title: Cybersecurity Blog
permalink: /blog/
---

<!-- Sidebar Toggle Button (Mobile Only) -->
<button id="toggleSidebar" class="sidebar-toggle">
  ☰ Blog Topics
</button>

<!-- Sidebar Container -->
<div class="sidebar" id="mobileSidebar">
  <h3>📚 Blog Topics</h3>
  <ul>
    <li><a href="#certifications">Certifications</a></li>
    <li><a href="#labs">Hands-On Labs</a></li>
    <li><a href="#reviews">Training Reviews</a></li>
    <li><a href="#soc">SOC Skills</a></li>
  </ul>
</div>

<!-- Blog Content Area -->
<div class="blog-posts">

  <section class="blog-post-card" id="certifications">
    <h3>🛡️ Google Cybersecurity Certificate Review</h3>
    <p>A breakdown of the Google Cybersecurity Certificate — how it's structured, what it actually teaches, and how I’m applying it in my lab setup.</p>
    <a href="/blog/google-cybersecurity-certificate-review">Read More →</a>
  </section>

  <section class="blog-post-card" id="reviews">
    <h3>🧠 First Impressions of Hack The Box Training</h3>
    <p>Early thoughts on HTB’s Blue Team learning path: what it covers, where it shines, and how it’s helping build practical detection skills.</p>
    <a href="/blog/htb-blue-team-review">Read More →</a>
  </section>

  <!-- Add more posts below this line using the same format -->

</div>

<!-- Inline Script for Sidebar Toggle -->
<script>
  document.getElementById('toggleSidebar').addEventListener('click', function () {
    const sidebar = document.getElementById('mobileSidebar');
    sidebar.classList.toggle('show');
  });
</script>

<!-- Mobile Responsive Styles -->
<style>
  .sidebar-toggle {
    display: none;
    background: #f5f5f5;
    border: none;
    padding: 0.75rem 1rem;
    font-size: 1rem;
    cursor: pointer;
    width: 100%;
    text-align: left;
    border-bottom: 1px solid #ddd;
  }

  .sidebar {
    width: 250px;
    float: left;
    padding: 1rem;
    background: #f9f9f9;
  }

  .blog-posts {
    margin-left: 270px;
    padding: 1rem;
  }

  .blog-post-card {
    background: #fff;
    border-radius: 8px;
    padding: 1rem;
    margin-bottom: 1.5rem;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  }

  @media screen and (max-width: 768px) {
    .sidebar-toggle {
      display: block;
    }

    .sidebar {
      display: none;
      width: 100%;
      float: none;
      margin: 0;
      border-top: 1px solid #ddd;
    }

    .sidebar.show {
      display: block;
    }

    .blog-posts {
      margin-left: 0;
      padding: 1rem;
    }

    .blog-post-card {
      margin-bottom: 1.5rem;
    }

    body {
      font-size: 1.1rem;
      line-height: 1.6;
    }
  }
</style>
