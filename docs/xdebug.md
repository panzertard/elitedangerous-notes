# Testpage

#### Categories
<ul>
  {% for cat in site.categories %}
    <li>
    {{ cat.CATEGORY }}
    </li>
  {% endfor %}
</ul>

#### Posts
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

#### Systems
<ul>
  {% for sys in site.systems %}
    <li>
      <a href="{{ site.baseurl }}{{ sys.url }}">{{ sys.title }}</a>
    </li>
  {% endfor %}
</ul>

#### Notes
<ul>
  {% for note in site.notes %}
    <li>
      <a href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

#### Sitemap
<ul>
  {% for page in site.pages %}
  {% if page.title != nil and page.title != "" %}
    <li>
      <a href="{{ site.baseurl }}{{ page.url }}">{{ page.title }}</a>
    </li>
  {% endif %}
  {% endfor %}
</ul>

#### Assets via Liquid inside MD 
{% assign image_files = site.static_files | where: "image", true %}
{% for myimage in image_files %}
<div>"{{ site.baseurl }}{{ myimage.path }}"</div>
<img src="{{ site.baseurl }}{{ myimage.path }}" alt="asset-w-baseurl" />
{% endfor %} 

#### Assets, relative path via viewable MD  
![assets-img-wo-baseurl](./assets/img/panzertard-sf.jpg)  
![assets-img-w-hardcoded-baseurl](/elitedangerous-notes/assets/img/panzertard-sf.jpg)  
![assets-img-w-relative-updir](/../assets/img/panzertard-sf.jpg)  
