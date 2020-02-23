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

#### Sitemap 2
<ul>
  {% for page in site.pages %}
    <div>PAGE.URL: "{{ page.url }}"</div>
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
