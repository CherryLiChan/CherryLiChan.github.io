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

<a href="https://cherrylichan.github.io/infovis/gaodemap-final/index.html" target="_blank">![image](https://note.youdao.com/yws/api/personal/file/6A23B343DF0444B6A590DF2672164795?method=download&shareKey=e1ca4da924203dac25a013abff16ef07)</a>

其他作品
<div class="tiles">
{% for post in site.categories.visualization %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles 把所有categories 有 visualization 的列出来-->