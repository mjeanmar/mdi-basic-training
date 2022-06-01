---
title: Command List
parent: Linux Basics
grand_parent: HPC Servers
has_children: false
nav_order: 30
---

## {{ page.title }}

Here is a cheat sheet of important Linux commands.

| Command | Examples | Description |
|---------|----------|-------------|
{{% for command in site.data.linux.commands  %}}
| command.name | {{ command.examples | join: "  " }} | command.description |
{{% endfor %}}
