---
title: Blogging tips
---
{% for article in site.blogging %}
<a href="{{ article.url | prepend: site.baseurl }}">
        <h2>{{ article.title }}</h2>
</a>
<p class="post-excerpt">{{ issue.excerpt | truncate: 160 }}</p>

{% endfor %}      
