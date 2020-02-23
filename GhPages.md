### Jekyll and Github pages
It's a real problem getting Jekyll + Liquid to understand that all the URL's should be host at the `/myproject` path.  
Almost all config variants results with MD-pages being generated at rootlevel (base url?).  
So instead of getting "https://myuser.github.io/myproject/posts/mypost" relative links have been parsed and presented as "https://myuser.github.io/posts/mypost", missing the "myproject" directory.

## _config.yml
This variant should produce a working `posts` collection.  
```yaml
# the only varient that hosts the _posts collection is this
#root: /elitedangerous-notes
baseurl: /elitedangerous-notes
#url: /elitedangerous-notes

collections:
  posts:
    output: true
    permalink: /:categories/:year/:month/:day/:title:output_ext
```

### Note - annoyingly missing the projectpath
If you use Markdown links the paths will be correctly pre-pended with the project name.  
if you use Liquid directly and `{{ post.url }}`, the project pre-pend will be missing.  
Instead use `{{ site.baseurl }}{{ post.url }}` access the project name.

You can even do crazy stuff like this in your MD:
```javascript
{% for post in site.posts %}
[{{ post.title }}]({{ site.baseurl }}{{ post.url }})
{% endfor %}
```

