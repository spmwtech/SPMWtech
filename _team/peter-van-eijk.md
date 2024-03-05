---
title: "Peter Van Eijk"
date: 2018-11-19T10:47:58+10:00
image: "images/team/peter-van-eijk-711986-unsplash.jpg"
jobtitle: "Director"
linkedinurl: "https://www.linkedin.com/"
promoted: true
weight: 1
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

{% assign person-donations = site.data.donations | where: "First name","Michael M" %}
<table>
  {% for row in person-donations %}
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
