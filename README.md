# craftideas
<h1>craftideas</h1>


<h2>Plugins</h2>
<ul>
<li>Popular Tags: https://github.com/philbirnie/CraftPopularTags</li>
<li>Tags</li>
<li>Categories</li>
<li>UpVote <a href="">UpVote</a></li>
<li>Custom entry ID: <a href="">Unique ID</a></li>
<li><a href="https://github.com/engram-design/Comments">Comments</a></li>
<li>User Reputation: <a href="">Points</a></li>
<li>Favorites: <a href="">Points</a></li>
<li>Export as xml</li>
<li>Advances Search</li>
<li>Ajax Relation</li>
</ul>


<h2>Plugins</h2>

<h2>Tag Cloud</h2>

<pre>    

{% set tags = craft.popularTags.taglist(15) %}
    <ul>
        {% for tag in tags %}
            <li>{{tag.title}} - {{tag.slug}}<span class="count">({{tag.count}})</span></li>
        {% endfor %}
</ul>
    
    </pre>




<h2>Category</h2>

<pre>
{% for category in entry.ideaSpace %}
    <b>{{ category.title }}</b>
    {%- if not loop.last -%}
      ,
    {% endif %}
{% endfor %}
</pre>

<h2>Tags</h2>

<pre>
<ul>
{% for tag in craft.tags.group('ideaTags') %}
    <a href="ideas/tags/{{tag.slug}}">{{ tag.title }}</a> 
    {%- if not loop.last -%} , {% endif %}
{% endfor %}
</ul>
</pre>



<pre>
<article>
<h1><a href="{{ entry.url }}">{{ entry.title }}</a></h1>
<ul>
<li><strong>IdeaSpace:</strong><a href="">{{ entry.author.fullName }}</a></li>
<li><strong>Tags:</strong><a href="">{{ entry.author.fullName }}</a></li>
<li><strong>Idea author:</strong><a href="">{{ entry.author.fullName }}</a> on {{ entry.postDate|date("M d, Y") }} </li>
<li><strong>Idea status:</strong>{{ entry.status }}</li>
<li><strong>Link:</strong><a href="{{ entry.url }}">Permalink</a> / <a href="{{ entry.url }}">Email </a></li>
</ul>
    
<div class="idea-body">{{ entry.body }}</div>

<a href="{{ entry.url }}">Continue reading</a>

</article>
    
    
</pre>



<pre>


</pre>


