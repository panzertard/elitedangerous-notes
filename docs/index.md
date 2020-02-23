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
    <div>POST.URL: "{{ post.url }}"</div>
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

#### foreach using markdown
{% for post in site.posts %}
[{{ post.title }}]({{ post.title }})
{% endfor %}

#### Sitemap
<ul>
  {% for page in site.pages %}
    <div>PAGE.URL: "{{ page.url }}"</div>
    <li>
      <a href="{{ page.url }}">{{ page.title }}</a>
    </li>    
    <div>BASEURL+URL: "{{ site.baseurl }}{{ page.url }}"</div>
    <li>
      <a href="{{ site.baseurl }}{{ page.url }}">{{ page.title }}</a>
    </li>
  {% endfor %}
</ul>

#### Assets
{% assign image_files = site.static_files | where: "image", true %}
{% for myimage in image_files %}
<div>"{{ myimage.path }}"</div>
<div>"{{ site.baseurl }}{{ myimage.path }}"</div>
{% endfor %}