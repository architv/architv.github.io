---
layout: post
title: Soccer CLI - How a simple CLI app went viral
comments: True
desc: Command line interface for all football scores. It's football for hackers
image: http://i.imgur.com/gJVJE0V.png
permalink: viral-cli-app
keywords: "cli, linux, python, football, soccer, open source, Archit Verma, app"
---

<img src="http://i.imgur.com/gJVJE0V.png?1" alt="trending image" style="width:100%;height:auto;">

Sunday evening, I am working on my laptop while Barclays Premier League commentary is playing in the background. I am trying to do two things simultaneously but I am able to do none.<!--more--> 

Since the work has to be done urgently, I switch off the TV. But now, I am constantly switching between my terminal and browser to check the scores, after all it's Manchester United who is playing.

This has happened to me dozens of time and every time I wish I didn't have to leave my terminal to check the scores. As a developer, my job is to find the solution. It was then the idea of [soccer-cli](https://github.com/architv/soccer-cli) came to me.

### A month and dozens of pull requests later:

It's been more than a month since I "launched" soccer cli and it got:

- Close to 250 stars on [Github](https://github.com/architv/soccer-cli)
- Number 1 trending python repo on Github
- Over 25k downloads on [PyPi](https://pypi.python.org/pypi/soccer-cli)
- Many more happy and productive football fans


<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">One of the geekiest things I&#39;ve ever seen...and it&#39;s awesome! <a href="https://t.co/LiEuKRd5Yx">https://t.co/LiEuKRd5Yx</a></p>&mdash; Oliver Roick (@oliverroick) <a href="https://twitter.com/oliverroick/status/639505433334558722">September 3, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">Soccer scores from the command line. Brilliant.&#10;<a href="https://t.co/vzloPoQsRC">https://t.co/vzloPoQsRC</a></p>&mdash; Jon Crowell (@jonrcrowell) <a href="https://twitter.com/jonrcrowell/status/639102520648822784">September 2, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-cards="hidden" lang="en"><p lang="en" dir="ltr">This open source command-line interface for soccer scores is pretty cool: <a href="http://t.co/ibMJsinORe">http://t.co/ibMJsinORe</a> <a href="http://t.co/Pxs7cwd5Nv">pic.twitter.com/Pxs7cwd5Nv</a></p>&mdash; Alex Sanchez (@_alxsanchez) <a href="https://twitter.com/_alxsanchez/status/639519993110073344">September 3, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" lang="en"><p lang="es" dir="ltr">sudo pip install soccer-cli; soccer --league=LLIGA. Aun hay gente que sabe hacer programas DE VERDAD.</p>&mdash; Raul Herranz (@rahego_) <a href="https://twitter.com/rahego_/status/639714442759008256">September 4, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

*Translation: sudo pip install soccer-cli; soccer - league = League. There are still people who know how to REALLY program.*

<blockquote class="twitter-tweet" lang="en"><p lang="en" dir="ltr">Soccer scores for hackers. Awesome. architv/soccer-cli · GitHub <a href="http://t.co/jXWKrmf66T">http://t.co/jXWKrmf66T</a></p>&mdash; Bill Horvath II (@billhorvath) <a href="https://twitter.com/billhorvath/status/642686647398723584">September 12, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>


It even made it's way to [Pycoders weekly newsletter](http://pycoders.com/)
![newsletter image](http://i.imgur.com/zAcafAK.png)

It was on Vietnam's hackernews too!
<img src="http://i.imgur.com/DHs6FjI.png" alt="vietnam image" style="width:100%;height:auto;">

The plan was not to create the next trending repo (even if it were, it would have been fine). it was to solve a problem that I myself was experiencing.

## How?

There were three basic things which were used to create soccer-cli:

__Football API__

The first task was to get the football scores. After a bit of looking for it, I stumbled across Joe Kampschmidt's [awesome curation](http://www.jokecamp.com/blog/guide-to-football-and-soccer-data-and-apis/) of all the source for getting data. 

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