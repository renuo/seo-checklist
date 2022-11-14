# Canonicalization

Canonical URLs help search engines better understand your site and in turn help it get a higher rank in the results. This is achieved by letting search engines and users know where the duplicate pages originate from, so the site becomes easier to crawl and index.

Consider the following two URLs that lead to the same content page:

* `https://www.example.com/page-1/`
* `https://www.example.com/index.php?id=2`

Which link would you rather click in the search results? Most likely the first one.

## Code example

It's good practice to place canonical links in the `head` to help Search Engines understand which URL is the original one.

```html
<head>
    <link rel="canonical" href="https://example.com/page-1" />
    [...]
</head>
```

Although this is the most common way of specifying canonical URLs, it is not the only way to do it:

* They can also be specified in the sitemap. The sitemap suggests to Google that all listed pages are canonical, but Google will understand which ones are duplicates if the page they are derived from is explicitly declared as a canonical URL.
* By using 301 redirects, Google will understand the redirected page as canonical. This is because, if you use 301 redirects, only the canonical URL will actually exist. All the duplicate versions will just redirect to this page.

That being said, 301 redirects are typically the best way to resolve duplicate content issues in certain cases (check [this blog](https://www.semrush.com/blog/canonical-url-guide/?kw=&cmp=FR_SRCH_DSA_Blog_EN&label=dsa_pagefeed&Network=g&Device=c&utm_content=622456720002&kwid=dsa-1754723161193&cmpid=18361911540&agpid=141829996536&BU=Core&extid=60109561348&adpos=&gclid=Cj0KCQiAyMKbBhD1ARIsANs7rEHLdvdrEtdLYTmvLYs4scW8sCyLGwYqph5XoqoG7VdT8EBM2O6yRoYaAlwrEALw_wcB) for more insight).

## Best practice

* Help Google choose the right canoical URL: [Consolidate duplicate URLs](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)
* [Article on MOZ](https://moz.com/learn/seo/canonicalization)

## Check

* Is the website accessible from different URLs?
* Are canonical links placed correctly in all the pages?
* Did you consider 301 redirects instead of duplicating the page itself?
