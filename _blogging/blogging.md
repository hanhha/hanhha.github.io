---
title: Blogging tips
---

{% for issue in site.blogging %}


<a href="{{ issue.url | prepend: site.baseurl }}">
        <h2>{{ issue.title }}</h2>
</a>

<p class="post-excerpt">{{ issue.excerpt | truncate: 160 }}</p>

{% endfor %}      
