---
layout: page
title: 文档
permalink: /documents/
---

# 文档中心

这里存放了各种技术文档和资源，欢迎下载使用。

## 文档列表

{% assign documents = site.static_files | where: "dir", "/documents/" %}
{% if documents.size > 0 %}
  <ul class="document-list">
    {% for document in documents %}
      <li>
        <a href="{{ document.path | prepend: site.baseurl }}" target="_blank">
          {{ document.name }}
        </a>
        <span class="document-size">({{ document.path | file_size }})</span>
      </li>
    {% endfor %}
  </ul>
{% else %}
  <p>暂无文档，请上传文档到 <code>documents</code> 目录。</p>
{% endif %}
