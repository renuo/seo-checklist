# Sitemap

Every website should have a sitemap. A sitemap is important as it lists all the web pages of the site and let search engine crawlers to crawl the website more intelligently.

There are two different kinds of sitemaps search engines can check:

* XML format: containing the whole sitemap, **not** frequently checked by Google
* Atom/RSS format: containing small site updates, frequently checked by Google

### Best practice

* View the [Google Webmaster Central Blog](https://webmasters.googleblog.com/2014/10/best-practices-for-xml-sitemaps-rssatom.html).

### Check

* Does the website implement an XML sitemap?
* Does the website ping the search engine after a sitemap change?
* Are the entries in the sitemap correct?
  * Only canonical URLs?
  * Update last modification time must **not** be `Time.zone.now` but `updated_at`.
* Does the page change in ways which would benefit from an Atom/RSS feed (e.g. blog articles)?
