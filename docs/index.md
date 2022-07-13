---
links_name: index
table_width: 6
---


# Hey dude

{% for group in links[links_name] %}
|{{ group }}{% for n in range(table_width) %}|{% endfor %}
|{% for n in range(table_width) %}-|{% endfor %}
{% for link in links[links_name][group] %}|[{{ link.name }}]({{link.url}}){% if loop.index % table_width == 0 %}
{% endif %}{% endfor %}
{% endfor %}

