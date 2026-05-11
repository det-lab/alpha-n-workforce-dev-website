---
layout: page
title: Resources
description: Tools, guides, and materials for current program participants.
permalink: /resources/
---

{% for category in site.data.resources %}
<section class="resource-section">
  <h2 class="resource-category">{{ category.category }}</h2>
  <div class="card-grid">
    {% for resource in category.items %}
      {% include resource-card.html resource=resource %}
    {% endfor %}
  </div>
</section>
{% endfor %}
