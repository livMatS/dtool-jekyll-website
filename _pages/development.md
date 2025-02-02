---
layout: page
permalink: /development/
title: development
description: dtool development hierarchy - dtool and dserver
nav: true
nav_order: 2
---

<!-- _pages/development.md -->

<link rel="stylesheet" href="{{ '/assets/css/styles.css' | relative_url }}">
{% for tool in site.data.tools %}
  <section id="{{ tool.name | downcase | replace: ' ', '-' }}">
    <h2 class="">{{ tool.name }}</h2>
    <div class="tool-grid">
      {% for part in tool.parts %}
        <div class="{{part}}">
          <span>{{ part }}</span>
        </div>
      {% endfor %}
      {% for block in tool.blocks %}
        <div class="{{ tool.name | downcase }}-block {{ block | downcase | replace: ' ', '-' }}">
          {% if block == 'terminal'%}
            <img src="{{ site.baseurl }}/assets/icons/terminal.png" alt="Terminal icon">
            <span><a href="https://dtool.readthedocs.io">dtool CLI</a></span>
          {% elsif block == 'gui' %}
            <img src="{{ site.baseurl }}/assets/icons/gtk.png" alt="GUI icon">
            <span><a href="https://dtool-lookup-gui.readthedocs.io">dtool GUI</a></span>
          {% elsif block == 'python-api' %}
            <img src="{{ site.baseurl }}/assets/icons/python.png" alt="Python icon">
            <span><a href="https://dtoolcore.readthedocs.io/en/latest/">dtoolcore (Python API)</a></span>
          {% elsif block == 'storage-item-disk' %}
            <img src="{{ site.baseurl }}/assets/icons/python.png" alt="Python icon">
            <span>disk storage broker</span>
          {% elsif block == 'storage-item-smb' %}
            <span><a href="https://github.com/livMatS/dtool-smb">dtool-smb</a></span>
          {% elsif block == 'storage-item-s3' %}
            <span> <a href="https://github.com/jic-dtool/dtool-s3"> dtool-s3</a></span>
          {% elsif block == 'storage-item-other' %}
            <span>other storage brokers ...</span>
          {% elsif block == 'file-system' %}
            <img src="{{ site.baseurl }}/assets/images/file-system.png" alt="File system icon">
            <span>classical file system</span>
          {% elsif block == 'network-share' %}
            <img src="{{ site.baseurl }}/assets/icons/smb.png" alt="SMB icon">
            <span>Windows network share</span>
          {% elsif block == 'object-storage' %}
            <img src="{{ site.baseurl }}/assets/icons/amazon-s3.png" alt="S3 icon">
            <span>S3 object storage</span>
          {% elsif block == 'other-infrastructure' %}
            <span>other infrastructure...</span>
          {% elsif block == 'webapp' %}
            <img src="{{ site.baseurl }}/assets/icons/vuejs.png" alt="Vue.js icon">
            <span><a href="https://github.com/jic-dtool/dtool-lookup-webapp">Vue.js web app</a></span>
          {% elsif block == 'restapi' %}
            <img src="{{ site.baseurl }}/assets/icons/openapi.png" alt="OpenAPI icon">
            <span><a href="https://dserver.readthedocs.io">dserver (OpenAPI-compliant REST API)</a></span>
          {% elsif block == 'flask' %}
            <img src="{{ site.baseurl }}/assets/icons/flask.png" alt="Flask icon">
            <span><a href="https://dservercore.readthedocs.io">dservercore</a></span>
          {% elsif block == 'search-plugin' %}
            <span><a href="https://github.com/livMatS/dserver-search-plugin-mongo">dserver-search-plugin-mongo</a></span>
          {% elsif block == 'retrieve-plugin' %}
            <span><a href="https://github.com/livMatS/dserver-retrieve-plugin-mongo">dserver-retrieve-plugin-mongo</a></span>
          {% elsif block == 'other-plugins' %}
            <span>other server-side plugins...</span>
          {% elsif block == 'database' %}
            <img src="{{ site.baseurl }}/assets/icons/sql.png" alt="SQL icon">
            <span>core database</span>
          {% elsif block == 'mongodb' %}
            <img src="{{ site.baseurl }}/assets/icons/mongodb.png" alt="MongoDB icon">
            <span><a href="https://github.com/livMatS/dserver-search-plugin-mongo">database with searchable and retrievable metadata</a></span>
          {% elsif block == 'other-database' %}
            <img src="{{ site.baseurl }}/assets/icons/database.png" alt="Database icon">
            <span>other database technologies...</span>
          {% else %}
            {{ block }}
          {% endif %}
        </div>
      {% endfor %}
    </div>
  </section>
{% endfor %}