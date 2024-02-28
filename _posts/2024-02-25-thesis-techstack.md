---
layout: post
title: How I Wrote my Master's Thesis
date: 2024-02-25 16:55:16
description: An overview of everything I used to write my ML master's thesis.
tags: thesis, academia, tech
categories: 
---

# Workflow and Setup for writing a machine learning thesis
Last year, I finished my thesis on at the University of Tübingen. I wrote this post originally as a planning document for myself, but I'm editing it in order to make the most useful details publicly available.
This 6-month commitment involved researching academic literature, implementing and running algorithms on real-world data, and finally writing up the thesis document.

This post describes my workflow and technical setup for doing all that. Since I've only ever written one thesis before this one, I had to think hard about choosing processes that make me as productive as possible and keep frustration at bay.

## Hardware and Ergonomics
During my bachelor's thesis, I mostly worked on my Surface Pro, sitting at a desk. Eventually, I developed pain in my wrist that lasted for weeks after I finished working on the thesis.
If this is your first time working at a desk for an extended period of time, please take an hour to familiarize yourself with the health risks involved. You can't work on your thesis if the physical movements hurt.
Back pain (and repetitive strain injury) are the largest physical risks from working at a desk all day.

At home, I had a standing desk and a vertical mouse, but I mostly worked from my assigned seat at the university, because I wasn't productive at home.

To set myself up for success this time around, I used a 2020 M1 MacBook Air with a second, 24 inch monitor set at eye-level. 
The MacBook is amazing because it's quiet and has a stunningly long battery life. The M1 is nevertheless one of the fastest chips on the market, and I'm going to be running compute-intensive tasks on the Uni's compute cluster anyway.

To set it up for productivity, I went through [swyx's setup procedure](https://www.swyx.io/new-mac-setup-2021) and installed what seemed potentially useful. Notable mentions:
- [homebrew](https://brew.sh/), the package manager for macOS, which is my preferred way of installing and updating any kind of software.
- [Rectangle](https://rectangleapp.com/), a nice Window manager that lets me move around the messy macOS windows with keyboard shortcuts like on MS Windows, even across screens

## Literature Research
Just as you want to manage dependencies in a software project, you also want to manage references in a research project. I use the free program [Zotero](https://www.zotero.org/) with the corresponding Chrome extension. Other, non-free options exist.
You should be aware of [this guide that lets Zotero automatically download pdfs from sci-hub](https://gagarine.medium.com/use-sci-hub-with-zotero-as-a-fall-back-pdf-resolver-cf139eb2cea7). If you accept the legal risk of using Sci-Hub, I've heard this is really convenient.

I take notes and build a personal Wiki in [Obsidian](https://obsidian.md/). For any new concept I encounter, I add a new note with the #Master tag.
I found myself referring to specific papers a few times, so instead of creating a new note for every paper I want to cite, I followed a blogpost about [connecting Obsidian with Zotero](https://www.marianamontes.me/post/obsidian-and-zotero/). This requires the [BetterBibTex plugin for Zotero](https://retorque.re/zotero-better-bibtex/), which I can recommend either way, and the [Citations plugin for Obsidian](https://github.com/hans/obsidian-citation-plugin/tree/0.1.3). I did not change the default settings a lot.

## Project Management / Motivation
A thesis is a large project that consists of several subprojects. Keep track of progress like you would for any project, to give yourself an overview and to make it easier to prioritize what to work on.
I tried to:
- Be my own manager. A supervisor can help, but in the end it's my responsibility to stay happy, productive and figuring things out.
- Time tracking might help somewhat to keep myself accountable. I tried using [toggl track](https://toggl.com/), but didn't manage to follow through.

I asked on Twitter, and I'll share [Ninell's Tipps:](https://twitter.com/nellsn1/status/1523680712154808326) here:
> Things that helped me in the past:
> 1. setting milestones to keep track how far you are in the process
> 2. celebrating wins (from smaller to larger treats, plan those in!)
> 3. reminding yourself to zoom out. Every task becomes tiring if you‘re going down the rabbit hole at thesis skill (talking referencing, proofreading, you name it). Zooming out and reminding myself why this is cool/important always helps me a lot.
> 4. complaining! but in a productive way! Don’t try to suppress negative emotions. However, don’t take a bath in them.

Vacations are useful to get some needed distance and a fresh mind. Frequent breaks to the everyday routine make it really hard for me to keep showing up. When I have the option to chose whether to get work done, I too often chose not to. I found that it took me 2 days to get back into my productive flow after coming back from a trip.

### Notes on Focus
The greatest danger to the success of my thesis project was distraction of all sorts. This makes sense: Not working towards finishing my thesis does not go towards finishing my thesis.
You need focus on all levels:
- Do commit actual weeks, days and hours to working on your thesis. When the weather's good, it might seem tempting to spend every day outside, but this is a distraction. Make these decisions mindfully.
- Do only focus on the important tasks. Clarify your research question early on. Don't go on tangents. Don't expand the scope of your research. Do tasks because they help answer the research question, and skip tasks that are interesting but not useful.
- When working, actually work. Don't let Social Media creep in. Read email once a day. Don't take too many coffee breaks. Don't excessively watch the construction site next door. I pay for [Freedom Pro](https://freedom.to), which lets me set recurring sessions of blocking distracting websites and apps on both my laptop and my phone.


## Collaboration
A thesis is an individual project, but to keep me motivated I need to use the social structures that my research group has created. We use Slack channels to keep in touch.

## Coding
My project involved working with deep reinforcement learning in a python library, so I naturally used python, gymnasium and pytorch to implement my algorithm and experiments.
Python's biggest annoyance is package management. For that, I used pip and pipenv, and never really ran into trouble.
I also used git and github to keep track of my code and thesis project.

I ran the experiments on a Slurm cluster provided by my uni.

I used VSCodium as a Code editor, and only occasionally found it useful to ask an LLM chatbot for help.

## Writing the thesis
There are as many thesis structure guides as there are supervisors. Depending on your field, conventions might be different, but they all look similar to:
1. Introduction
2. Background / Related Work
3. Approach / Methods
4. Results
5. Discussion
6. Conclusion

I feel like you're quite free to move things around a bit. Some combine results and discussion, some only develop their approach after introducing the first batch of results. It's a matter of style, and you should consider style!

For additional resources, a professor in my undergrad recommended Paul J Silva's ["How to Write a Lot: A Practical Guide to Productive Academic Writing"](https://www.goodreads.com/book/show/39874447-how-to-write-a-lot), which covers how to make time to write, how to stay motivated, and a few notes on style. I reread that book for every large writing project I undertake.

On the tools side, you should not be surprised that I use LaTeX for writing and typesetting, with my master program's template. I installed LaTeX locally (using TexLive), using VSCodium as an editor, with the LaTeX Workshop extension and the LTEX spell checker extension.