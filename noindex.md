# Noindex tag

The entry `noindex` in the meta tags tells a search engine robot that the visited page should not be included in the index. 
That way you can influence which URLs are to be indexed and which are not.

```html
<head>
    <meta name="robots" content="noindex" />
    [...]
</head>
```

## Best practice
* Use this tag for internal search result pages, double category pages, copyrighted content or paginated pages.
* Check if it works: Google the specific URL you don't want to be indexed. Enter *site:www.meinedomain.ch* in Google.

## Note
The meta tag `noindex` is only there to inform search engines not to index a _specific_ page.
If specific pages should not be crawled, the use of `disallow` in the `robots.txt` file is recommended.
