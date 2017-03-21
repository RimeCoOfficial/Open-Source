---
layout: default
---

<h1>Public Repositories</h1>
<ul>
    {% for repo in site.github.public_repositories %}
        <li>
            <p>
                <a href="{{ repo.html_url }}">{{ repo.name }}</a> {{ repo.description }}
                <br>
                <small>{{ repo.language }} {{ repo.updated_at | time_tag: '%b %d, %Y' }}</small>
            </p>
        </li>
    {% endfor %}
</ul>

<h1>Organization Members</h1>
<ol>
    {% for contributor in site.github.organization_members %}
        <li>
            <a href="{{ contributor.html_url }}">{{ contributor.login }}</a>
        </li>
    {% endfor %}
</ol>