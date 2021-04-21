# No follow tags

For good search rankings, make sure to add the “nofollow” attribute to external links (links to websites that you don’t own) which you don't want a search engine to follow. 

This is extremely useful in cases where you provide user generated content on your website, where anyone could write a comment or article containing links to boost their own website rankings.

Normal link:
```html
<a href="http://example.com">Example Website</a>
```

Link with the nofollow tag:
```html
<a href="http://example.com" rel="nofollow">Example Website</a>
```
