---
layout: post
title: Soccer CLI - How a simple CLI app went viral
comments: True
permalink: viral-cli-app
desc: "Command line interface for all football scores. It's football for hackers"
image: "http://i.imgur.com/gJVJE0V.png"
keywords: "cli, linux, python, football, soccer, open source, Archit Verma, app"
---

<img src="http://i.imgur.com/gJVJE0V.png?1" alt="trending image" style="width:100%;height:auto;">

Sunday Evening, I am working on my laptop while Barclays Premier League commentary is playing in the background. I am trying to do two things simultaneously but I am able to do none.<!--more--> 

Since the work has to be done urgently, I switch off the TV. But now, I am constantly switching between my terminal and browser to check the scores, after all it's Manchester United who is playing.

This has happened to me dozens of time and every time I wish I didn't have to leave my terminal to check the scores. As a developer, my job is to find the solution. It was then the idea of soccer cli came to me.

### A month and dozens of pull requests later:

It's been more than a month since I "launched" soccer cli and it got:

- close to 250 stars on github
- number 1 trending python repo on Github
- over 25k downloads on PyPi
- many more happy and productive football fans


<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/architv07">@architv07</a> I love your soccer-cli 😂 found on <a href="https://twitter.com/githuntio">@githuntio</a></p>&mdash; EGOIST (@egoistgogo) <a href="https://twitter.com/egoistgogo/status/640824213696155648">September 7, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/architv07">@architv07</a> saw your soccer-cli software in GitHub. Interesting. Congratulations! How I can help you add LigaMX support?</p>&mdash; Guillermo Sanchez (@gsanchez1982) <a href="https://twitter.com/gsanchez1982/status/639291703581503488">September 3, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/architv07">@architv07</a> <a href="https://twitter.com/github">@github</a> Awesome Stuff !👍</p>&mdash; Mohammed Faizan (@faizan_ke) <a href="https://twitter.com/faizan_ke/status/640115452170125312">September 5, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

It even made it's way to [Pycoders weekly newsletter](http://pycoders.com/)
![newsletter image](http://i.imgur.com/zAcafAK.png)

It was on Vietnam's hackernews too!
<img src="http://i.imgur.com/DHs6FjI.png" alt="vietnam image" style="width:100%;height:auto;">

The plan was not to create the next trending repo (even if it were, it would have been fine). it was to solve a problem that I myself was experiencing

## How?

There were three basic things which were used to create soccer-cli:

__Football API__

The first task was to get the football scores. After a bit of looking for it, I stumbled across Joe Kampschmidt's [awesome curation](http://www.jokecamp.com/blog/guide-to-football-and-soccer-data-and-apis/#openfooty) of all the source for getting data. 

Since, I had no intention to pay for the API, I looked for the free ones. I tried both [openfooty API](http://www.footytube.com/openfooty/) and [football-data API](http://api.football-data.org/index). Openfooty API had a stale community and it was hard to get an API key. football-data API on the other hand, had a good documentation, easy to get an API key and scores were updated fast enough to match my needs. So, I went ahead with it.

__Live Scores__

While the football-data API updated the scores fast enough, it still didn't implement real-time scores. So, to fix this problem I decided to create [my own API](http://soccer-cli.appspot.com/) to get live scores. It's a simple with just a single endpoint which fetches the scores from [ESPN](http://www.espnfc.com/scores) and spits it out in the json format

__Click__

Since the tool was entirely command line, I needed an easy way to get and parse command line arguments. [click](http://click.pocoo.org/5/) came to my rescue. From it's documentation:

> Click is a Python package for creating beautiful command line interfaces in a composable way with as little code as necessary. It’s the “Command Line Interface Creation Kit”. It’s highly configurable but comes with sensible defaults out of the box.
> It aims to make the process of writing command line tools quick and fun while also preventing any frustration caused by the inability to implement an intended CLI API.

## End

Doing all this has been fun. I have learnt a lot more about python through various pull requests. Open source is awesome, you get to learn new concepts and apply them. 

The rewards are amazing, seeing people love what I made and talk about it, makes me extremely happy and proud.

{% include twitter_plug.html %}