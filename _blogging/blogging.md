---
title: Blogging tips
---
{% for article in site.blogging %} 

<a href="{{ article.url | prepend: site.baseurl }}">
        - {{ article.title }} 
</a>

{% endfor %}      
