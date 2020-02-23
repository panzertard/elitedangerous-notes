### Jekyll and Github pages
It's a real problem getting Jekyll + Liquid to understand that all the URL's should be host at the `/myproject` path.  
Almost all config variants results with MD-pages being generated at rootlevel (base url?).  
So instead of getting "https://myuser.github.io/myproject/posts/mypost" relative links have been parsed and presented as "https://myuser.github.io/posts/mypost", missing the "myproject" directory.

Sample `index.md`:  
```javascript
  {% for post in site.posts %}
    <div>POST.URL: "{{ post.url }}"</div>
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
```
## Test 1
sample `_config.yml`:
```yaml
root: /elitedangerous-notes
#baseurl: /elitedangerous-notes
#url: /elitedangerous-notes

collections:
  posts:
    output: true
    permalink: /elitedangerous-notes/:categories/:year/:month/:day/:title:output_ext
```
```markdown
    [John Harper : And here the Wheel](./EDLore-author-JohnHarper.md)
```
Result:
    POST.URL: "/elitedangerous-notes/blog/2020/02/02/testing-a-post.html"
    Page is unavailable at that url
    
    `https://panzertard.github.io/elitedangerous-notes/EDLore-author-JohnHarper.html`  
    `[John Harper : And here the Wheel](./EDLore-author-JohnHarper.md)` works as expected.  

## Test 2
```yaml
# so we need to set both of these for a project?
#root: /elitedangerous-notes
baseurl: /elitedangerous-notes
#url: /elitedangerous-notes

collections:
  posts:
    output: true
    permalink: /elitedangerous-notes/:categories/:year/:month/:day/:title:output_ext
```
