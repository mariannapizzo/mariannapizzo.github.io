---
title: Teaching Activity
layout: home
nav_enabled: true
nav_order: 4
---
{% for year in site.data.teaching %}
## Academic Year {{ year.year }}

### Courses
{% for course in year.courses %}
- **{{ course.title }}** ({{ course.program }})  
  {% if course.page %}· <a href="{{ course.page }}" target="_blank"><i class="fa-solid fa-link"></i> Course website</a>{% endif %}
  {% endfor %}

{% if year.theses %}
### Theses
{% for thesis in year.theses %}
- {{ thesis.title }}
  {% endfor %}
  {% endif %}

---
{% endfor %}
