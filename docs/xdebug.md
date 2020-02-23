# Test at mypagehere.md

#### for each post
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

#### Sitemap
<ul>
  {% for page in site.pages %}
    <li>
      <a href="{{ site.baseurl }}{{ page.url }}">{{ page.title | "No title" }}</a>
    </li>
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
