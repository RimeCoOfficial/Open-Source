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
                <small><b>{{ repo.language }}</b> Updated on {{ repo.updated_at | date: "%b %d, %Y" }}</small>
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

<p>
    Build Revision: <a href="./site.github.json">{{ site.github.build_revision | truncate: 7, "" }}</a>
</p>