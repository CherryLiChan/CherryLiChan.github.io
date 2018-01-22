---
layout: archive
title: "信息可视化作品集"
date: 2018-1-1T14:25:45-04:00
modified:
excerpt: "黎婵的信息可视化作品集"
tags: []
image: 
  feature: 
  teaser:
---

<iframe src="https://public.tableau.com/views/_18774/3_1?:embed=y&:display_count=yes&publish=yes"></iframe>

其他作品
<div class="tiles">
{% for post in site.categories.visualization %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles 把所有categories 有 visualization 的列出来-->