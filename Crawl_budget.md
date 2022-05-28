# Crawl budget

Search engines determine how many subpages they crawl per URL.
This is not the same for all websites, but is primarily determined by the PageRank of a page.
The higher the PageRank, the larger the crawl budget.
The crawl budget also determines how often the most important pages of the website are crawled and how often a deep crawl takes place.

## Best practice

* Realization of a flat page architecture, where the way to the subpages is as short as possible and only requires a few clicks ([navigation structure](navigation-structure.md)).
* Very good internal linking of the most important pages.
* Internal linking of pages with many backlinks to pages that are to be crawled more frequently.
* Exclusion of unimportant pages from crawling by [Robots.txt](robots-txt.md) (e.g. log-in pages, contact forms, images).
* Exclusion of crawling using metadata ([noindex](noindex.md), nofollow).
* Offering an XML [sitemap](sitemap.md) with a URL list of the most important subpages.

## Check

* Are the most important pages reachable in few clicks? (max 2)
* is `robots.txt` implemented correctly, excluding login pages and similar, from crawling?
