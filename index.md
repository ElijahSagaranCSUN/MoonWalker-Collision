---
title: Home
layout: default
---

{% include site_header.html %}

## Group Members

<div class="member-card">
  <img src="{{ site.images.Elijah | relative_url }}" alt="Elijah Sagaran" class="member-photo">
  <div class="member-content">
    <h3>Elijah Sagaran</h3>
    <ul>
      <li>Worked on the Omniverse side for the Cadre rover</li>
      <li>Developed required collision detection and hosting switch scripts for Omniverse</li>
      <li>Handled hosting and consuming scripts for Omniverse</li>
      <li><strong>LinkedIn:</strong> <a href="{{ site.socials.ElijahLinkedIn }}">linkedin.com/in/elijahsagaran/</a></li>
    </ul>
  </div>
</div>

<div class="member-card">
  <img src="{{ site.images.Martin | relative_url }}" alt="Martin Ha" class="member-photo">
  <div class="member-content">
    <h3>Martin Ha</h3>
    <ul>
      <li>Worked on the Unity side for the Viper rover</li>
      <li>Developed required collision detection and hosting switch scripts for Unity-side interoperability support</li>
      <li>Handled hosting and consuming scripts for Omniverse/Unity communication</li>
      <li><strong>LinkedIn:</strong> <a href="{{ site.socials.MartinLinkedIn }}">linkedin.com/in/martindn-ha/</a></li>
    </ul>
  </div>
</div>

<div class="member-card">
  <img src="{{ site.images.Rowel | relative_url }}" alt="Rowel Espejo" class="member-photo">
  <div class="member-content">
    <h3>Rowel Espejo</h3>
    <ul>
      <li>Worked on the HSML API, allowing the two simulation platforms to connect</li>
      <li>Implemented MySQL authentication and authorization for secure communication</li>
      <li>Handled the internal Kafka server and feedback channel during collisions</li>
      <li><strong>LinkedIn:</strong> <a href="{{ site.socials.RowelLinkedIn }}">linkedin.com/in/rowelespejo</a></li>
    </ul>
  </div>
</div>

{% include footer.html %}