# Index

## Subjects
### Princess Astrophile and the spiralling stars
* [Wikipedia, Astrophile and Stella](https://en.wikipedia.org/wiki/Astrophel_and_Stella)
* [My notes on the sonnet](./Astrophil-sonnet.md)

### Authors and lore
* [John Harper : And here the Wheel](./EDLore-author-JohnHarper.md)

## Test relative url via subpage
[Test mypagehere reference](mypagehere)

# Test relative url via this page, index.md
#### for each post
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

#### foreach using markdown
{% for post in site.posts %}
[{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}

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

![avatar-w-relative-updir](/../assets/panzertard-sf.jpg)  