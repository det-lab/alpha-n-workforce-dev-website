---
layout: page
title: Staff
description: The dedicated team running the alpha, n Workforce Development Program.
permalink: /staff/
---

<div class="card-grid">
  {% for member in site.data.staff %}
    {% include staff-card.html member=member %}
  {% endfor %}
</div>
