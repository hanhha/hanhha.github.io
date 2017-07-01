---
title: Blogging tips
description: My summary to recall me how to blog on my site.
---
This collection is my summary to recall me syntax, flows, rules to blog in this site which was built on top of Jekyll and Github Pages.  

{% for article in site.blogging %} 
[{{ article.url | prepend: site.baseurl }}]( - {{ article.title }} )
        - {{ article.title }} 
{% endfor %}      
