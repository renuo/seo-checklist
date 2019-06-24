# Noindex Tag
The entry "noindex" in the meta tags tells a search engine robot that the visited page should not be included in the index. That way you can influence which URLs are to be indexed and which are not. 

### Best practice
* Use this tag for internal search result pages, double category pages, copyrighted content or paginated pages.

`<!DOCTYPE html>
<html><head>
<meta name="robots" content="noindex" />
(…)
</head>
<body>(…)</body>
</html>`

* Check if it works: Google the specific URL you don’t want to be indexed. Enter *site:www.meinedomain.de* in Google.

### Note
The meta tag "noindex" is only there to inform search engines no to index a specific page. If specific pages should not be crawled, the use of "disallow" in the robots.txt file is recommended.
