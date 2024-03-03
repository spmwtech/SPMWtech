---
title: All Contributions
layout: page
permaink: /contributions-table/
description: About
---

# Contributions Table

<table>
  {% for row in site.data.donations %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
