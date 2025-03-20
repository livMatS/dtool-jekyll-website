---
layout: page
permalink: /development/
title: development
description: dtool and dserver abstraction layers
nav: true
nav_order: 2
---

_dtool_ and _dserver_ have been developed to integrate well into both manual and automized workflows.
Their design follows "Ten simple rules for making a software tool workflow-ready" postulated by
[Brack et al., 2022](https://doi.org/10.1371/journal.pcbi.1009823). Importantly, this means exposing both human-
and machine-accessible interfaces at different implementation layers. Diagrams below place core components of the
_dtool_ and _dserver_ ecosystem within a landscape of stacked abstraction layers. Whether you simply want to manipulate
_dtool_ datasets with a graphical user interface, or embed handling _dtool_ datasets within a complex computational
workflow, below you will find links to the documentation of the right interface to the ecosystem.

{% for tool in site.data.tools %}

  <section id="{{ tool.name | downcase | replace: ' ', '-' }}">
    <h2 class="">{{ tool.name }}</h2>
    <div class="tool-grid">
      {% for part in tool.parts %}
        <div class="{{ tool.name }}-h {{ part | downcase | replace: ' ', '-'}}">
          <span>{{ part }}</span>
        </div>
      {% endfor %}
      {% for block in tool.blocks %}
        <div class="{{ tool.name | downcase }}-block {{ block | downcase | replace: ' ', '-' }}">
          {% if block == 'terminal'%}
            <img src="{{ '/assets/icons/terminal.png' | relative_url}}" alt="Terminal icon">
            <span><a href="https://dtool.readthedocs.io">dtool CLI</a></span>
          {% elsif block == 'gui' %}
            <img src="{{ '/assets/icons/gtk.png' | relative_url}}" alt="GUI icon">
            <span><a href="https://dtool-lookup-gui.readthedocs.io">dtool GUI</a></span>
          {% elsif block == 'python-api' %}
            <img src="{{ '/assets/icons/python.png'| relative_url}}" alt="Python icon">
            <span><a href="https://dtoolcore.readthedocs.io/en/latest/">dtoolcore (Python API)</a></span>
          {% elsif block == 'storage-item-disk' %}
            <img src="{{ '/assets/icons/python.png'| relative_url}}" alt="Python icon">
            <span><a href="https://github.com/jic-dtool/dtoolcore/blob/master/dtoolcore/storagebroker.py#L403-L784">disk storage broker</a></span>
          {% elsif block == 'storage-item-smb' %}
            <span><a href="https://github.com/livMatS/dtool-smb">dtool-smb</a></span>
          {% elsif block == 'storage-item-s3' %}
            <span> <a href="https://github.com/jic-dtool/dtool-s3"> dtool-s3</a></span>
          {% elsif block == 'storage-item-other' %}
            <span>other storage brokers ...</span>
          {% elsif block == 'file-system' %}
            <img src="{{ '/assets/images/file-system.png'| relative_url}}" alt="File system icon">
            <span>classical file system</span>
          {% elsif block == 'network-share' %}
            <img src="{{ '/assets/icons/smb.png'| relative_url}}" alt="SMB icon">
            <span>Windows network share</span>
          {% elsif block == 'object-storage' %}
            <img src="{{ '/assets/icons/amazon-s3.png'| relative_url}}" alt="S3 icon">
            <span>S3 object storage</span>
          {% elsif block == 'other-infrastructure' %}
            <span>other infrastructure...</span>
          {% elsif block == 'webapp' %}
            <img src="{{ '/assets/icons/vuejs.png'| relative_url}}" alt="Vue.js icon">
            <span><a href="https://github.com/jic-dtool/dtool-lookup-webapp">Vue.js web app</a></span>
          {% elsif block == 'dtool-lookup-api' %}
            <img src="{{ '/assets/icons/python.png'| relative_url}}" alt="Python icon">
            <span><a href="https://dtool-lookup-api.readthedocs.io/en/latest/">dtool-lookup-api (Python API)</a></span>
          {% elsif block == 'restapi' %}
            <img src="{{ '/assets/icons/openapi.png'| relative_url}}" alt="OpenAPI icon">
            <span><a href="https://dserver.readthedocs.io">dserver</a> (<a href="https://demo.dtool.dev/lookup/doc/swagger">OpenAPI-compliant REST API</a>)</span>
          {% elsif block == 'flask' %}
            <img src="{{ '/assets/icons/flask.png'| relative_url}}" alt="Flask icon">
            <span><a href="https://dservercore.readthedocs.io">dservercore</a></span>
          {% elsif block == 'search-plugin' %}
            <span><a href="https://github.com/livMatS/dserver-search-plugin-mongo">dserver-search-plugin-mongo</a></span>
          {% elsif block == 'retrieve-plugin' %}
            <span><a href="https://github.com/livMatS/dserver-retrieve-plugin-mongo">dserver-retrieve-plugin-mongo</a></span>
          {% elsif block == 'other-plugins' %}
            <span><a href="https://dserver.readthedocs.io/en/latest/story.html#user-stories-that-lead-to-dserver-centered-additions-for-the-dtool-ecosystem">other server-side plugins...</a></span>
          {% elsif block == 'database' %}
            <img src="{{ '/assets/icons/sql.png'| relative_url}}" alt="SQL icon">
            <span>core database</span>
          {% elsif block == 'mongodb' %}
            <img src="{{ '/assets/icons/mongodb.png'| relative_url}}" alt="MongoDB icon">
            <span><a href="https://www.mongodb.com/">database with searchable and retrievable metadata</a></span>
          {% elsif block == 'other-database' %}
            <img src="{{ '/assets/icons/database.png'| relative_url}}" alt="Database icon">
            <span>other database technologies...</span>
          {% else %}
            {{ block }}
          {% endif %}
        </div>
      {% endfor %}
    </div>
  </section>
{% endfor %}
