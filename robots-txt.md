# Robots

**Generally you can not block access to your website if it's accessible on the web.**
Protect your page with a password if needed.

`robots.txt` is being used to manage crawler traffic and to avoid visits from inside your own page.
Links from external pages will still show up in Google results.

To manage what is shown in the search results, use Robots meta tag, `data-nosnippet` and `X-Robots` HTTP header.

Examples:

* `robots.txt`
  ```
  Sitemap: https://www.yourwebsite.ch/sitemap.xml
  User-agent: *
  Disallow: /kasse
  Disallow: /cart
  Disallow: /account
  ```
* Robots `meta` HTML tag:
  ```
  <meta name="robots" content="noindex" />
  ```
* `X-Robots` HTTP header:
  ```
  HTTP/1.1 200 OK
  Date: Tue, 25 May 2010 21:42:43 GMT
  (…)
  X-Robots-Tag: noarchive
  X-Robots-Tag: unavailable_after: 25 Jun 2010 15:00:00 PST
  ```
* `data-nosnippet` HTML attribute:
  ```
  <p>This text can be shown in a snippet
  <span data-nosnippet>and this part would not be shown</span>.</p>
  ```

## Best practice

* If a specific page should not be crawled, the use of "disallow" in the robots.txt file is recommended.
* Annotate your content with [tags, attributes and headers](https://developers.google.com/search/docs/advanced/robots/robots_meta_tag)
* Check the [Search Console Help](https://support.google.com/webmasters/answer/6062608)

## Check

* Synchronize crawler access rules with your sitemap
* Check your `robots.txt` for entries you don't want to have indexed and annotate the content with meta tags.
