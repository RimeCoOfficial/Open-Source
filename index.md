---
layout: default
---

<h1>Public Repositories</h1>
<ul>
    {% for repo in site.github.public_repositories %}
        <li>
            {{ repo.full_name }}
        </li>
    {% endfor %}
</ul>

<h1>Organization Members</h1>
<ol>
    {% for contributor in site.github.contributors %}
        <li>
            {{ contributor.login }}
        </li>
    {% endfor %}
</ol>