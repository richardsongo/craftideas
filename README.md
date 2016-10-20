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

<pre>    {% <span class="pl-k">set</span> <span class="pl-smi">tags</span> <span class="pl-k">=</span> <span class="pl-smi">craft</span>.<span class="pl-smi">popularTags</span>.<span class="pl-smi">taglist</span>(<span class="pl-c1">15</span>) %}
    &lt;<span class="pl-ent">ul</span>&gt;
        {% <span class="pl-k">for</span> <span class="pl-smi">tag</span> <span class="pl-k">in</span> <span class="pl-smi">tags</span> %}
            &lt;<span class="pl-ent">li</span>&gt;{{<span class="pl-smi">tag</span>.<span class="pl-smi">title</span>}} - {{<span class="pl-smi">tag</span>.<span class="pl-smi">slug</span>}}&lt;<span class="pl-ent">span</span> <span class="pl-e">class</span>=<span class="pl-s"><span class="pl-pds">"</span>count<span class="pl-pds">"</span></span>&gt;({{<span class="pl-smi">tag</span>.<span class="pl-smi">count</span>}})&lt;/<span class="pl-ent">span</span>&gt;&lt;/<span class="pl-ent">li</span>&gt;
        {% <span class="pl-k">endfor</span> %}
    &lt;/<span class="pl-ent">ul</span>&gt;
    
    </pre>


<h2>Category</h2>

<pre>
{% for category in entry.mediaType %}
    <b>{{ category.title }}</b>
    {%- if not loop.last -%}
      ,
    {% endif %}
{% endfor %}
</pre>
