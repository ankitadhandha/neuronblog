---
title: "notes from ankita: Neuron and Sphinx"
date: "2020-06-04"
author: gg
---

Neuron and Sphinx are similar in this way:

- both generate HTML (and JS on which the runtime depends. Neuron example: search)
- both are controlled by an index
- neither run-time is dependent on its development environment
- a browser is the run-time environment

Sphinx HTML is anchored by a table-of-contents that is used by its development environment to generate menus

Sphinx menus are the principle method navigating a Sphinx-generated site (together with "next" and "previous")

Neuron does not have a menu interface. Instead, cards/zettels are connected using a URI in the form of a <link>

As links are added, Neuron development environment connects the zettels and builds an hierarchical index (a form of menu) based on relationships among zettels

Neuron and Sphinx are similar in this way:

- Sphinx build-process is activated by web-hooks. When a Sphinx GitHub repo is updated, web-hooks signal the Sphinx build environment to rebuild all HTML. The Sphinx build-process installs newly generated HTML on S3
- Neuron build-process depends on an integrated, self contained process. The Neuron build-process ahs fewer "moving parts" than does the Sphinx build-process. When new/changed content is added to a repo, a developer "starts" a new AWS EC2 server to integrate, build and generate new HTML. HTML is then installed on S3. When the process is complete, the developer "stops" the AWS EC2 server.

Optionally we could run Neuron all the time to allow for spontaneous zettel additions/change, but the AWS charges for the  server would be high

---

To edit this file, click [here](https://github.com/ankitadhandha/zettelkasten/edit/master/d7f6dac5084d4cbf.md)

To add new file, click [here](https://github.com/ankitadhandha/zettelkasten/new/master)

---
