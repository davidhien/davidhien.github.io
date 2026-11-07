## Teaching

{% for group in site.data.teaching %}
<h4 style="margin:0 10px 0;">{{ group.institution }}</h4>

<ul style="margin:0 0 {% if forloop.last %}20px{% else %}5px{% endif %};">
{% for course in group.courses %}
  <li>{% if course.link %}<a href="{{ course.link }}"><autocolor>{{ course.title }}</autocolor></a>{% else %}{{ course.title }}{% endif %}{% if course.role %}, {{ course.role }}{% endif %}{% if course.term %} ({{ course.term }}){% endif %}</li>
{% endfor %}
</ul>
{% endfor %}
