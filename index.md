---
layout: default
---

<h1>Public Repositories</h1>
<ul>
    {% for repo in site.github.public_repositories %}
        <li>
            <p>
                <a href="{{ repo.html_url }}">{{ repo.name }}</a>
                {% if repo.homepage %}<a href="{{ repo.homepage }}" target="_blank">↗️</a>{% endif %}
                {{ repo.description }}
                <br>
                <small><b>{{ repo.language }}</b> Updated on {{ repo.updated_at | date: "%b %d, %Y" }}</small>
            </p>
        </li>
    {% endfor %}
</ul>

<h1>Organization Members</h1>

<div class="row">
    {% for contributor in site.github.organization_members %}
    <div class="col">
        <a href="{{ contributor.html_url }}" class="thumbnail" title="@{{ contributor.login }}">
            <img src="{{ contributor.avatar_url }}" alt="{{ contributor.login }}">
        </a>
    </div>
    {% endfor %}
</div>

<p>
    Build Revision <a href="./site.github.json">{{ site.github.build_revision | truncate: 7, "" }}</a>
</p>
