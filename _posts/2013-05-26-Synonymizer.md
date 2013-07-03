---
layout: project
title: Synonymizer
categories: coding
---

#####\[ *si-non-uh-mahyz-er*\]

<p><strong>Built using:</strong>&nbsp;&nbsp;<span class="pict-prog-nodejs01 icon-2x"> </span>&nbsp;<span class="pict-dbs-mysql icon-3x"> </span>&nbsp;<span class="pict-html5-01 icon-2x"> </span>&nbsp;<span class="pict-css3-01 icon-2x"> </span>&nbsp;<span class="pict-prog-js02 icon-2x"> </span></p>



Program to take inputted text and substitute words within it with their synonyms.

Backend server written in node.js.   

I have recently taken a keen interest in web development and am looking to hone my skills in it. I have heard very good things about NodeJS and as such have decided to pursue it. What particularly appeals to me about node is the simplicity of creating non-blocking code and writing both front and back end in JavaScript.    

If I become particularly comfortable during this project in JS I may try to write some of the more simple front end JS in CoffeeScript.
  
*Curently under construction* <!-- abridge -->

Decided to use the merriam-webster dictionary since they have an open API that allows you to query items to their thesaurus and will feed back well formatted XML for us to parse.   

Their [site](http://www.dictionaryapi.com/)   

For example, passing a request of the form: ```http://www.dictionaryapi.com/api/v1/references/thesaurus/xml/recourse?key=\[API KEY\]```

Will return the following XML data:

{% highlight xml %}
<entry_list version="1.0">
<entry id="recourse">
	<term>
		<hw>recourse</hw>
	</term>
	<fl>noun</fl>
	<sens>
		<mc>
			something that one uses to accomplish an end especially when the usual means is not available
		</mc>
		<vi>
			a toddler quickly learns that a tantrum is a surefire
			<it>recourse</it>
			when a polite request for something is met with parental indifference
		</vi>
		<syn>expedient, recourse, resort</syn>
		<rel>
			hope, opportunity, possibility, relief; makeshift, replacement, stopgap, substitute
		</rel>
	</sens>
</entry>
</entry_list>
{% endhighlight %}

As you can see the desired information is wrapped in ```<syn>``` tags. 

####Progress so far:

- [x] Find Thesaurus API -> Use Mirriam Webster API to retrieve synonyms
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

<!-- See the [code](https://github.com/mgingras/synonymizer) - Try the [app](http://synonymizer.herokuapp.com/) -->