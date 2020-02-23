# Index 8

#### for each post
<ul>
  {% for post in site.posts %}
  <li>
    <div>"{{ post.url }}"</div>
  </li>
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


#### Using page instead of posts
<ul>
  {% for page in page.posts %}
    <li>
      <a href="{{ page.url }}">{{ page.title }}</a>
    </li>
  {% endfor %}
</ul>

#### As sub category
{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
  <li>
    <div>"{{ post.url }}"</div>
  </li>
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}


#### SItemap
<ul>
  {% for page in site.pages %}
  <li>
    <div>"{{ page.url }}"</div>
  </li>
    <li>
      <a href="{{ page.url }}">{{ page.title }}</a>
    </li>
  {% endfor %}
</ul>

#### Assets
{% assign image_files = site.static_files | where: "image", true %}
{% for myimage in image_files %}
<div>"{{ myimage.path }}"</div>
{% endfor %}