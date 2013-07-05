---
layout: project
title: Synonymizer
categories: coding
---

#####\[ *si-non-uh-mahyz-er*\]

<p><strong>Built using:</strong>&nbsp;&nbsp;<span class="pict-prog-nodejs01 icon-2x"> </span>&nbsp;<span class="pict-html5-01 icon-2x"> </span>&nbsp;<span class="pict-css3-01 icon-2x"> </span>&nbsp;<span class="pict-prog-js02 icon-2x"> </span></p>



Program to take inputted text and substitute words within it with their synonyms.

Backend server written in node.js.   

I have recently taken a keen interest in web development and am looking to hone my skills in it. I have heard very good things about NodeJS and as such have decided to pursue it. What particularly appeals to me about node is the simplicity of creating non-blocking code and writing both front and back end in JavaScript.    

If I become particularly comfortable during this project in JS I may try to write some of the more simple front end JS in CoffeeScript.
  
*Curently under construction* <!-- abridge -->

Originally planned to use the merriam-webster dictionary since they have an open API that allows you to query items to their thesaurus and will feed back well formatted XML for us to parse.   

However, their api limits you to 1000 requests per day and XML is the only return format.

Their [site](http://www.dictionaryapi.com/)   

I decided instead to use Big Huge Labs since they have more return options, including JSON, higher request limit, and also more verbose responses.

See their [site](http://words.bighugelabs.com/api.php)

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

####Progress so far:

- [x] Find Thesaurus API
- [x] Get rid of form elements -> clickless application
- [x] Modify current text box area so that it takes 50% of area instead of max 600, add <p></p> tag to fill on right hand side
- [x] Use JQuery to register event listener for changes in text area
- [x] Use JQuery to modify paragraph on right hand side so that it mirrors text in box
- [ ] Basic request for synonyms
- [ ] Implement smarter synonym logic

If you have any suggestions please feel free to pass them along:   	<a href="mailto:martin@magingras.com?Subject=Synonymizer%20Suggestion" title="Email Me!">martin@magingras.com</a>



* Check out: https://github.com/mikeal/request for simple requests...


Code pushed to heroku dev environment: [http://synonymizer.herokuapp.com/](http://synonymizer.herokuapp.com/)


![Under Construction](http://t3.gstatic.com/images?q=tbn:ANd9GcQxVIewybJj0mbyVLfpoFPIXkAfcYCtQKhRqdFrYvKRRyKwxy5p "Under Construction")

###Under Construction

See the [code](https://github.com/mgingras/synonymizer) *currently private* - Try the [app](http://synonymizer.herokuapp.com/)
