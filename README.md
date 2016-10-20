# craftideas
<h1>craftideas</h1>


<h2>Plugins</h2>
<ul>
<li>Popular Tags: https://github.com/philbirnie/CraftPopularTags</li>
<li>Tags</li>
<li>Categories</li>
<li>UpVote <a href="">UpVote</a></li>
<li>Custom entry ID: <a href="">Unique ID</a></li>
<li>Comments</li>
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




