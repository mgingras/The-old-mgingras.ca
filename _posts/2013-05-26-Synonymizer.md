---
layout: project
title: Synonymizer
categories: coding
---

#####[\[*synonym-izer*\]](www.synonym-izer.com)

<p><strong>Built using:</strong>&nbsp;&nbsp;<span title="node.js" class="pict-prog-nodejs01 icon-2x"> </span>&nbsp;<span title="MongoDB" class="pict-dbs-mongodb icon-2x"> </span>&nbsp;<span title="JavaScript" class="pict-prog-js02 icon-2x"> </span>&nbsp;<span title="JQuery" class="pict-prog-jquery icon-2x"> </span>&nbsp;<span title="HTML5" class="pict-html5-01 icon-2x"> </span>&nbsp;<span title="CSS3" class="pict-css3-01 icon-2x"> </span></p>

This is a program which takes inputted text and substitute words within it for their synonyms.

Backend server written in node.js.   

I have recently taken a keen interest in web development and am looking to hone my skills in it. I have heard very good things about NodeJS and as such have decided to pursue my interest in it. What particularly appeals to me about node is the simplicity of creating non-blocking code and writing both front and back end in JavaScript.    
  
*Currently in Beta Testing, [check it out](http://www.synonym-izer.com/)*   
![In Beta Testing](/img/beta.png "In Beta Testing")

<!-- abridge -->

###Beta

Originally I planned to use the [merriam-webster](http://www.dictionaryapi.com/) dictionary since they have an open API that allows you to query items to their thesaurus and will feed back XML data.   

However, their api limits you to 1000 requests per day and XML is the only return format.

**Instead**, I decided instead to use [Big Huge Labs](http://words.bighugelabs.com/api.php) since they have more return options, including JSON, higher request limit, and retern more verbose responses.

Requests will be sent in the form: http://words.bighugelabs.com/api/{version}/{api key}/{word}/{format}

Responses will have the following relationship types:
- "syn" for synonyms
- "ant" for antonyms
- "rel" for related terms
- "sim" for similar terms
- "usr" for user suggestions

I will be getting JSON format responses parsing for focusing on the "syn" data

Big Huge labs also provieds the following HTTP Response Codes:

200 OK: The word was found and the results are in the body.
303 {alternate}: The original word was not found but an alternative has been. The alternative is the HTTP response message. For example, a request for "reminding" returns 303 remind. The Location header contains the URL for the API request for "remind."
404 Not Found: No data could be found for the word or alternates.
500 Usage Exceeded: Usage limits have been exceeded.
500 Inactive key: The key is not active.


After some testing I noticed that there were a lot of 303 messages returned, that would re-direct us to an un-related synonym, and 404, indicating that the word we were looking for did not have any data. I decided to then create a back end database to store these exceptions in order to minimize the number of API calls we made, and also to speed up the event loop.

How it has been implemented is:
- When a user hits the page the data is queried from database and passed to the browser as an array.
- Before a request is even sent up to the our server it is run through this exception list, if it is in there, no call to our server and thus to the API is required.
- Any API calls that we make that result in a 303 or 404 header being returned will have their word added to this excpetion list.

Depending how large this exception list gets I may move the exception checking to the server...

####Progress so far:

- Find Thesaurus API *done*
- Set up HTML UI, with text box on left, button in middle, output on right *done*
- Use JQuery to register event listeners *done*
- Use JQuery to modify paragraph on right hand side so that it mirrors text in box *done*
- Basic request for synonyms *done*
- Pass data from web application to server and get response back *done*
- Modify the output field on the right with synonymized data *done*
- Implement natural language recognition and replace words with valid synonymz (verb, noun, adjective) (currently just replace with whichever has data(stupid)) *doneish*
- Add node package natural, change words to singular when querying synonyms, then pluarlize when passing back to UI

<div>
<p>If you have any suggestions please feel free to pass them along: <a href="mailto:martin@mgingras.ca?Subject=Synonymizer%20Suggestion" title="Email Me!">martin@mgingras.ca</a></p>
</div>




Code pushed to heroku dev environment: [http://www.synonym-izer.com/](http://www.synonym-izer.com/)

See the [code](https://github.com/mgingras/synonymizer)
