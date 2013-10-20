<h1><i class="icon-code"></i>&nbsp;&nbsp;Coding Projects</h1>
<h5>Here is a list of some of the projects that I have worked on recently:</h5>
<hr>
{% for project in site.categories.coding %}
<h4><i class="icon-terminal"></i> open<a href="{{ project.url }}"> {{ project.title }}/</a></h4>
<p>{{ project.content | split: '<!-- abridge -->' | first }}</p>
<hr>
{% endfor %}