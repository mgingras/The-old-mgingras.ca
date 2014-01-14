---
layout: project
title: HN Sentiment
categories: coding
---

####Check it out: [HN Sentiment](http://hn-sentiment.com)
#####*Web application that allows users to anylize the sentiment of the Hacker News community towards a particular topic*

<p><strong>Built using:</strong>&nbsp;&nbsp;<span title="node.js" class="pict-prog-nodejs01 icon-2x"> </span>&nbsp;<span title="CoffeeScript" class="pict-prog-coffeescr icon-2x"> </span>&nbsp;<span title="JQuery" class="pict-prog-jquery icon-2x"> </span>&nbsp;<span title="HTML5" class="pict-html5-01 icon-2x"> </span>&nbsp;<span title="CSS3" class="pict-css3-01 icon-2x"> </span></p>

This porject was done over a few days of my Christmas '13 holidays, for the Iron.io hackathon (where it placed [2nd](http://blog.iron.io/2014/01/holiday-hack-winners.html)). The intent is to generalize the way the entire HN community feels towards a particular topic.


<!-- abridge -->

###Technical Stuff
####This project is all open-sourced under the [The MIT License](https://github.com/mgingras/HN-Sentiment/blob/master/LICENSE)  and available [here](https://github.com/mgingras/HN-Sentiment)

The project is written in CoffeeScript on NodeJS using the Express framework.
How it functions:

1. The application generates http requests for the 25 (number in flux) most recent posts with the entered keyword in their content or title.
2. It then parses the content to determine the original post and, most interestingly, all of the comments.
3. The app then iterates over the title, content, and all of the comments of the post and analyzes them for any sentiment using the [AFINN-111](http://www2.imm.dtu.dk/pubdb/views/publication_details.php?id=6010) wordlist to determine an integer value for the desired topic.
4. The number discovered is then returned and displayed to the client.

In my next iteration I will be:

- Normalizing the returned values
- Work on caching (right now have fairly basic cacheing, which on Heroku gets dumped every time the repo sleeps).
- Cleaner (and more fun) UI
- Track down any bottlenecks or bugs

Send me an <a href="mailto:martin@mgingras.ca?Subject=HN-Sentiment" title="HN-Sentiment">email</a> with any suggestions!!