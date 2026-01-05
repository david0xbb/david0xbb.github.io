---
layout: page
title: Welcome
permalink: /
---

<style>
  .main-container {
    max-width: 800px;       
    margin: 0 auto;         
    padding: 0 20px;        
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
  }

  .post-card {
    background-color: #f8f9fa; 
    border: 1px solid #e9ecef;
    border-radius: 8px;        
    padding: 20px;
    margin-bottom: 20px;       
    transition: transform 0.2s;
  }
  
  .post-card:hover {
    transform: translateY(-2px); 
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
  }

  .post-title {
    font-size: 1.4em;
    font-weight: bold;
    margin-bottom: 8px;
    display: block;
    color: #333;
    text-decoration: none;
  }

  .post-meta {
    font-size: 0.9em;
    color: #666;
  }
</style>

<div class="main-container">

  <div style="margin-top: 40px;"></div>

  <h1>👋 Welcome to David's Log</h1>

  <p style="font-size: 1.1em; line-height: 1.6; color: #444;">
    Hi, this is <strong>David</strong>. I'm documenting my learning notes in this blog. <br>
  </p>

  <div style="display: flex; gap: 20px; margin-top: 25px; margin-bottom: 50px;">
    <a href="https://github.com/david0xbb" target="_blank" style="text-decoration: none; border: none;">
      <svg height="28" width="28" viewBox="0 0 16 16" fill="currentColor" style="color: #333;">
        <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"></path>
      </svg>
    </a>

    <a href="/feed.xml" target="_blank" style="text-decoration: none; border: none;">
      <svg height="28" width="28" viewBox="0 0 24 24" fill="currentColor" style="color: #ee802f;">
        <path d="M6.18 15.64a2.18 2.18 0 0 1 2.18 2.18C8.36 19 7.38 20 6.18 20 5 20 4 19 4 17.82a2.18 2.18 0 0 1 2.18-2.18M4 4.44A15.56 15.56 0 0 1 19.56 20h-2.83A12.73 12.73 0 0 0 4 7.27V4.44m0 5.66a9.9 9.9 0 0 1 9.9 9.9h-2.83A7.07 7.07 0 0 0 4 12.93V10.1z"/>
      </svg>
    </a>
  </div>

  <hr style="margin: 40px 0; border: 0; border-top: 1px solid #eee;">

  <h2 style="margin-bottom: 30px;">Latest Notes</h2>

  {% for post in site.posts %}
    <div class="post-card">
      <a href="{{ post.url }}" class="post-title">
        {{ post.title }}
      </a>
      <div class="post-meta">
        {{ post.date | date: "%B %d, %Y" }} 
        | {{ post.content | strip_html | number_of_words | divided_by: 180 | plus: 1 }} min read
      </div>
      
      <p style="margin-top: 10px; color: #555;">
        {{ post.excerpt | strip_html | truncatewords: 30 }}
      </p>
    </div>
  {% endfor %}

</div>