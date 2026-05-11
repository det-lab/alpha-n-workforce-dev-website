---
layout: page
title: Students
description: Students accepted into the program, organized by cohort year.
permalink: /students/
---

{% for cohort in site.data.students.cohorts %}
<section class="cohort-section">
  <h2 class="cohort-year">{{ cohort.year }} Cohort</h2>
  <div class="card-grid">
    {% for student in cohort.students %}
      {% include student-card.html student=student %}
    {% endfor %}
  </div>
</section>
{% endfor %}
