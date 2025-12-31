---
layout: default
title: Home
---

## Welcome to David's Lab (0xbb)

Here are my research notes on Signal Processing, AI, Reinforcement Learning,
and end-to-end autonomous systems.

---

### Research Notes / Ideas (WIP)

- **End-to-End Trajectory Prediction**  
  *Directly predicting future trajectories from perception and latent world states,  
  bridging representation learning and control.*  
  *(Work in progress)*


RL and image ?
---

### Recent Posts

<ul>
  {% for post in site.posts %}
    <li>
      <span style="color:gray; font-size:0.8em;">{{ post.date | date: "%Y-%m-%d" }}</span>
      &nbsp;
      <a href="{{ post.url | relative_url }}">
        <strong>{{ post.title }}</strong>
      </a>
    </li>
  {% endfor %}
</ul>
