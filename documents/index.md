---
layout: default
title: 文档
---

<div class="page-content">
  <h1>文档中心</h1>
  
  <p>这里存放了各种技术文档和资源，欢迎下载使用。</p>
  
  <h2>文档列表</h2>
  
  {% assign documents = site.static_files | where_exp: "file", "file.path contains '/documents/' and file.name != 'index.md'" %}
  {% if documents.size > 0 %}
    <ul class="document-list">
      {% for document in documents %}
        <li>
          <a href="{{ document.path | prepend: site.baseurl }}" target="_blank">
            {{ document.name }}
          </a>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p>暂无文档，请上传文档到 <code>documents</code> 目录。</p>
  {% endif %}
</div>