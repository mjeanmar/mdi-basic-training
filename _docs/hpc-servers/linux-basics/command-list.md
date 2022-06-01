---
title: Command List
parent: Linux Basics
grand_parent: HPC Servers
has_children: false
nav_order: 30
---

## {{ page.title }}

Here is a cheat sheet of important Linux commands.

{% for category in site.data.linux.commands  %}
### {{ category.name }}
| Command | Examples | Description |
|---------|----------|-------------|
{% for command in category.commands  %}| {{ command.name }} | {{ command.examples | join: "<br>" }} | {{ command.description }} | {% endfor %}
{% endfor %}
