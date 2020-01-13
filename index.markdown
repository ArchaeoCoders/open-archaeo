---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<link rel="stylesheet" href="index.css" />

## A list of open source archaeological software and resources.

## Tags <!--Make it so these tags can be selected/de-selected, which toggles them in and out of SelectedTags. SelectedTags needs to be an array, and multiple items from that array must be readable by the for/if loop (kinda like 'match').-->
### Topics

### Language / Platform

{% assign SelectedTags = "example1" %}

{% for item in site.data.items %}
  {% for x in item.tags %}
    {% if x contains SelectedTags %}

<article>
 <p>{{ item.name }}</p>
 <p>by {% if item.author-url %}<a href="{{ item.author-url }}">{% endif %}{{ item.author }}{% if item.author-url %}</a> {% endif %}</p>

 <span><p>🌐:
 {% if item.github %}
   <a href="{{ item.github }}">[GitHub]</a>
 {% endif %}
 {% if item.website %}
   <a href="{{ item.website }}">[Website]</a>
 {% endif %}
 {% if item.cran %}
   <a href="{{ item.cran }}">[CRAN]</a>
 {% endif %}
 {% if item.pypi %}
   <a href="{{ item.pypi }}">[PyPi]</a>
 {% endif %}
 {% if item.launchpad %}
   <a href="{{ item.launchpad }}">[Launchpad]</a>
 {% endif %}
 {% if item.bitbucket %}
   <a href="{{ item.bitbucket }}">[BitBucket]</a>
 {% endif %}
 {% if item.gitlab %}
   <a href="{{ item.gitlab }}">[GitLab]</a>
 {% endif %}
 </p></span>

 <span><p> 🏷:
   {% for tag in item.tags %}
     <a href="/tags/{{ tag }}/">[{{tag}}]</a>
   {% endfor %}
 </p></span>

 {% if item.description %}
   <span class="description">{{ item.description }}</span>
 {% endif %}

 <hr style="border-width: 1px 1px 0;
        border-style: solid;
        border-color: palevioletred;
        background-color: palevioletred;
        height: 1px;
        width: 100%;
        margin-left: auto;
        margin-right: auto;">

</article>

    {% endif %}
  {% endfor %}
{% endfor %}






### Tags
+ Quantitative & Statistical Analysis
+ Geospatial Analysis
  + Locational Analysis
  + Viewshed Analysis
  + Modelling & Inference
+ Site Mapping
+ Harris Matrices
+ ...

### Language / Platform
+ Python
+ R
+ QGIS
+ ...

## Items

{% for item in site.data.items %}
  <article>
    <p>{{ item.name }}</p>
    <p>by {% if item.author-url %}<a href="{{ item.author-url }}">{% endif %}{{ item.author }}{% if item.author-url %}</a> {% endif %}</p>

    <span><p>🌐:
    {% if item.github %}
      <a href="{{ item.github }}">[GitHub]</a>
    {% endif %}
    {% if item.website %}
      <a href="{{ item.website }}">[Website]</a>
    {% endif %}
    {% if item.cran %}
      <a href="{{ item.cran }}">[CRAN]</a>
    {% endif %}
    {% if item.pypi %}
      <a href="{{ item.pypi }}">[PyPi]</a>
    {% endif %}
    {% if item.launchpad %}
      <a href="{{ item.launchpad }}">[Launchpad]</a>
    {% endif %}
    {% if item.bitbucket %}
      <a href="{{ item.bitbucket }}">[BitBucket]</a>
    {% endif %}
    {% if item.gitlab %}
      <a href="{{ item.gitlab }}">[GitLab]</a>
    {% endif %}
    </p></span>

    <span><p> 🏷:
      {% for tag in item.tags %}
        <a href="/tags/{{ tag }}/">[{{tag}}]</a>
      {% endfor %}
    </p></span>

    {% if item.description %}
      <span class="description">{{ item.description }}</span>
    {% endif %}

    <hr style="border-width: 1px 1px 0;
           border-style: solid;
           border-color: palevioletred;
           background-color: palevioletred;
           height: 1px;
           width: 100%;
           margin-left: auto;
           margin-right: auto;">

  </article>
{% endfor %}
