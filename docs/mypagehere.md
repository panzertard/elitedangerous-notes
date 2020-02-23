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
      <a href="{{ site.baseurl }}{{ page.url }}">{{ page.title }}</a>
    </li>
  {% endfor %}
</ul>

#### Assets via HTML-scheme  
{% assign image_files = site.static_files | where: "image", true %}
{% for myimage in image_files %}
<div>"{{ myimage.path }}"</div>
<img src="{{ myimage.path }}" alt="avatar-no-baseurl" />
<div>"{{ site.baseurl }}{{ myimage.path }}"</div>
<img src="{{ site.baseurl }}{{ myimage.path }}" alt="avatar-w-baseurl" />
{% endfor %} 

#### Assets via MD-scheme  
![assets-wo-baseurl](/assets/panzertard-sf.jpg)  
![assets-w-hardcoded-baseurl](/elitedangerous-notes/assets/panzertard-sf.jpg)  
![assets-w-relative-updir](/../assets/panzertard-sf.jpg)  

![assets-img-wo-baseurl](/assets/img/panzertard-sf.jpg)  
![assets-img-w-hardcoded-baseurl](/elitedangerous-notes/assets/img/panzertard-sf.jpg)  
![assets-img-w-relative-updir](/../assets/img/panzertard-sf.jpg)  
