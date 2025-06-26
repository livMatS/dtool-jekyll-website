---
layout: page
permalink: /tutorials/
title: tutorials
description: tutorials - getting started with dtool
nav: true
nav_order: 1
---

This page lists didactic material available for components of the _dtool_ ecosystem.

## command line client

The [dtool-demo](https://github.com/livMatS/dtool-demo) repository contains several sample terminal sessions that
demonstrate working with the dtool CLI. The following videos have been generated from these terminal sessions. For
thorough documentation, refer to [dtool.readthedocs.io](https://dtool.readthedocs.io).

<details>
<summary>setup</summary>
<br>
<script src="https://asciinema.org/a/660458.js" id="asciicast-660458" async="true"></script>
</details>
<p></p>

<details>
<summary>copy dataset from remote</summary>
<br>
<script src="https://asciinema.org/a/660459.js" id="asciicast-660459" async="true"></script>
</details>
<p></p>

<details>
<summary>dataset creation</summary>
<br>
<script src="https://asciinema.org/a/661484.js" id="asciicast-661484" async="true"></script>
</details>
<p></p>

<details>
<summary>copy dataset to remote</summary>
<br>
<script src="https://asciinema.org/a/660461.js" id="asciicast-660461" async="true"></script>
</details>
<p></p>

<details>
<summary>search and query dserver</summary>
<br>
<script src="https://asciinema.org/a/660463.js" id="asciicast-660463" async="true"></script>
</details>
<p></p>

## graphical user interface

Following videos show how to work with the [dtool-lookup-gui](https://github.com/livMatS/dtool-lookup-gui),
an experimental graphical user interface for the _dtool_ & _dserver_ research data management ecosystem.
For thorough documentation, refer to [dtool-lookup-gui.readthedocs.io](https://dtool-lookup-gui.readthedocs.io/).

<details>
<summary>setup</summary>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/dnx-kEI65Js?si=Y7vGJyV7MtVyjhhZ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</details>
<p></p>

<details>
<summary>copy dataset from remote</summary>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/Qu5_AF9zrb4?si=aLkDmqQHT1iJuxSC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</details>
<p></p>

<details>
<summary>dataset creation</summary>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/lGODxYxF3F4?si=rFLXpECINY00eYdK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</details>
<p></p>

<details>
<summary>copy dataset to remote and find with dserver</summary>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/FMIY8U7VXN8?si=h8ZpVzRXuagD8uya" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</details>
<p></p>

<details>
<summary>search professionally with MongoDB query language, navigate dependency graph</summary>
<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/ZhjALYz4XOw?si=1YQFx9iYJ1dXPTLN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</details>
<p></p>

## dserver demonstrator instance

[demo.dtool.dev](https://demo.dtool.dev) exposes an open _dserver_ instance as a playground for first steps with the _dtool_ ecosystem.

To populate a local _dserver_ instance with some sample datasets, download the dtool sample family [assets/files/sample-datasets.zip](sample-datasets.zip), extract them and run

```bash
docker run -v $(pwd)/sample-datasets:/tmp/data:ro -p 8888:8888 ghcr.io/livmats/dserver-minimal:latest
```

from within the folder of extraction. This mounts the local folder `sample-datasets` into the docker container as a dataset repository.
[http://localhost:8888](http://localhost:8888) now exposes the _dserver web app_ and lists a family of datasets.


## dtool & dserver cheat sheet

<iframe src="https://widgets.figshare.com/articles/26102227/embed?show_title=1" width="568" height="351" allowfullscreen frameborder="0"></iframe>
