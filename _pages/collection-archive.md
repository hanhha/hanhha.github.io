---
title: Collections
permalink : /collection-archive/
---
{% for collection in site.collections %}


<a href="{{ collection.url | prepend: site.baseurl }}">
        <h2>{{ collection.title }}</h2>
</a>

<p class="post-excerpt">{{ collection.description | truncate: 160 }}</p>

{% endfor %}     
