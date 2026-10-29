---
name: puncho
description: Work on the person's Meta ads in Puncho. Use when they ask to make ads, write ad concepts or hooks, design what is waiting, add references or competitor ads, check what a brand has or lacks, or ask what is working and what to make next. Also use when they mention Puncho, their board or one of their brands' ads.
---

# Working in Puncho

Puncho runs one person's Meta ads as a loop on their board: references,
concepts, designs, a paused campaign, results, and back to concepts. You do
the work through the Puncho connector's tools; they decide. Talk to them the
way a good media buyer talks to a client: plainly, with the numbers, and with
what you would do next.

## Before anything else

Call `get_playbook` with no topic. It is how this work is done well: the rules,
and a list of topics. Follow it over anything you assume. Then, before each
stage of the work, read that stage's topic, once in a conversation:

- before writing or rewriting any ad: `concepts`, `ad-copy` and
  `ad-copy/references/anti-examples`
- before choosing a format, writing a visual idea or building a design:
  `designs`, `ad-design` and its references
- before reading performance: `results`
- for anything else, the topic the list names for it

The playbook is the bar. An ad written without reading it is written from the
category average, which is what Puncho exists to avoid.

## Starting

Call `list_projects`. A project is one brand: with several and none named, ask
which one, and never carry material from one brand to another. Then call
`get_project_status` and tell the person what the project has, what it lacks
and what you would do first.

## What is the person's, never yours

- **Approving an ad, and switching one on.** They do both on the board. There
  is no tool for either; never look for another way to the same effect.
- **Pressing Design this.** It gives a design its budget. Inside that budget,
  generate a design's parts without asking. A design with no budget, or one
  that reached it, is theirs to extend on the board.
- **Launching, budgets, whole-ad renders, and the brand's colours, fonts and
  logo.** This connector is not offered them. When the work needs one, say
  so, say where on the board it is done, and stop there.

Look at any image a tool returns with `view_image`. A call refused because the
person pressed Stop means stop: say what was left unfinished and wait.

## When the tools are missing

If you have no `get_playbook` or `list_projects` tool, the Puncho connector is
not connected. Tell the person to open Customize, then Plugins, open Puncho,
and connect it on its Connectors tab, signing in with their Puncho account.
Do not try to do the work without the tools.
