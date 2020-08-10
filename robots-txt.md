# Robots.txt
A website should be using a robots.txt file. When search engine robots crawl a website, they typically first access a site's robots.txt file. Robots.txt tells Googlebot and other crawlers what is and is not allowed to be crawled on a site.

```
Sitemap: https://www.yourwebsite.ch/sitemap.xml
User-agent: *
Disallow: /kasse
Disallow: /cart
Disallow: /account
```

### Best practice
* If a specific page should not be crawled, the use of "disallow" in the robots.txt file is recommended.
* If you want to inform search engines not to index a specific page use the [noindex tag](noindex.md).
* Check the [Search Console Help](https://support.google.com/webmasters/answer/6062608)
