# Canonicalization

Canonicalization describes how a site can use slightly different URLs for the same page (e.g., if http://www.example.com and http://example.com displays the same page but do not resolve to the same URL). If this happens, search engines may be unsure about which URL is the correct one to index.

Is good practice to place canonical links in the `head` to help Search Engines understand which URL is the original one.

e.g.
```
<link href="https://example.com/" rel="canonical" />
```

## Best practices and links
* Use canonical links: [Google Webmaster Central Blog 1](https://webmasters.googleblog.com/2009/02/specify-your-canonical.html) and [2](https://support.google.com/webmasters/answer/139066?hl=en)
* Setup Google Analytics correctly: [Stack Overflow](https://stackoverflow.com/questions/9103794/canonical-url-in-analytics)
* [Article on MOZ](https://moz.com/learn/seo/canonicalization)
* Use a canonical link tag to nominate a primary page when you have several pages with duplicate or very similar content.


## Check

* Is the website accessible from different URLs? Are canonical links placed correctly in all the pages?
