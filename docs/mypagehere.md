# Test at mypagehere.md

#### for each post
<ul>
  {% for post in site.posts %}
    <div>POST.URL: "{{ post.url }}"</div>
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
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
![avatar-no-baseurl](/assets/panzertard-sf.jpg)  
![avatar-w-baseurl](/elitedangerous-notes/assets/panzertard-sf.jpg)  

