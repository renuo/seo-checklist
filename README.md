<img width="100%" alt="renuochecklist2" src="https://user-images.githubusercontent.com/17065978/114165642-06b47580-992d-11eb-8bce-cb873e541869.png">

<b align="center">The checklist that covers the latest search engine optimisations to help you have a user friendly website that ranks high in search results!</b>

Hi folks!

As developers, we might not think about SEO right away, while developing a new project. But to create a great website that performs well and can be found by possible users, good SEO is always essential.

This checklist is free for you to use and is meant as a reference for all the aspects that should be checked before the go-live of a project. We suggest reading this once before starting a new project, to keep yourself up-to-date, and then again before the go-live, to double check and verify that all the points that matter are respected.

We update this checklist regularly. Nevertheless, if you find any missing points let us know or commit them directly yourself.

Together we create the best SEO checklist on GitHub! :tada:

# Backlinks
Backlinks are any links to your website from an external site. Relevant backlinks from authority sites are great for higher search engine rankings. 

### Best practice
* Register the website in relevant directories.
* Look for high quality relevant websites that could place a backlink to your page.

# Broken links
Your website shouldn't have any broken or dead links. Broken links negatively impact the user experience and damage your website's overall ranking with search engines.

### Best practice
Scan your website regularly to locate both broken internal links (pointing within your website) and external broken links (pointing outside of your website). Use [Broken Link Check](https://www.brokenlinkcheck.com), [Dr Link Check](https://www.drlinkcheck.com) or [Dead Link Checker](https://www.deadlinkchecker.com).

# Canonicalization
Canonicalization describes how a site can use slightly different URLs for the same page (e.g., if http://www.example.com and http://example.com displays the same page but do not resolve to the same URL). If this happens, search engines may be unsure about which URL is the correct one to index.

### Code example
It's good practice to place canonical links in the `head` to help Search Engines understand which URL is the original one.

```html
<head>
    <link href="https://example.com/" rel="canonical" />
    [...]
</head>
```

### Best practice
* Use canonical links: [Google Webmaster Central Blog 1](https://webmasters.googleblog.com/2009/02/specify-your-canonical.html) and [2](https://support.google.com/webmasters/answer/139066?hl=en)
* Setup Google Analytics correctly: [Stack Overflow](https://stackoverflow.com/questions/9103794/canonical-url-in-analytics)
* [Article on MOZ](https://moz.com/learn/seo/canonicalization)

### Check
* Is the website accessible from different URLs? Are canonical links placed correctly in all the pages?

# Content
The content of your website is crucial for good SEO. It is important that your content is unique and relevant. If you have multiple pages with the same content (or if you have your content on other people’s websites), you will run the risk of getting penalized by search engines and your search rankings will suffer.

### Best practice
* Create meaningful and unique content.
* Use at least 300 words per page.
* Use different media types (video/visuals/graphs/tables/infographics)
* Check keywords that are relevant to the topic you're writing about
* Use [Google Trends](https://trends.google.com/trends/?geo=US) or Services like [PeopleAsk](https://alsoasked.com/)

# Contrast Ratio
For visually impaired people, it is important to have a good contrast ratio of texts, logotypes and images on a website.
Contrast Ratio can be easily checked with a Lighthouse check.

### Best practice
* [Understanding Contrast Minimum](https://www.w3.org/WAI/WCAG21/Understanding/contrast-minimum.html)

### Check
* Is text easily readable and big enough to read? Does it clearly separate itself from the background of the website?
* Is the logo well-placed? (e.g. navbar where the background colour supports the logotype)

# Crawl budget
Search engines determine how many subpages they crawl per URL. 
This is not the same for all websites, but is primarily determined by the PageRank of a page. 
The higher the PageRank, the larger the crawl budget. 
The crawl budget also determines how often the most important pages of the website are crawled and how often a deep crawl takes place.

### Best practice
* Realization of a flat page architecture, where the way to the subpages is as short as possible and only requires a few clicks ([navigation structure](navigation-structure.md)).
* Very good internal linking of the most important pages.
* Internal linking of pages with many backlinks to pages that are to be crawled more frequently.
* Exclusion of unimportant pages from crawling by [Robots.txt](robots-txt.md) (e.g. log-in pages, contact forms, images).
* Exclusion of crawling using metadata ([noindex](noindex.md), nofollow).
* Offering an XML [sitemap](sitemap.md) with a URL list of the most important subpages.

### Check
* Are the most important pages reachable in few clicks? (max 2)
* is `robots.txt` implemented correctly, excluding login pages and similar, from crawling?

# CSS caching
A page should be using caching headers for all CSS resources. 
Users' browsers will check for these headers and, if any, will cache the CSS resources until the specified date (so that it does not keep re-fetching the unchanged file from your server). 
This speeds up your site the next time returning visitors arrive at your site and require the same CSS resource.

### Check
* Google Lighthouse can identify possible issues with CSS caching

# CSS minification
All CSS files used in your page must be minified. Minified files reduce page size and overall load time.

### Best practice
* The minification is performed by default when using the standard Rails setup, or using other build tools such as Webpack in a production mode.

### Check
* Google Lighthouse can identify non-minified CSS resources.

**Note:** Delivering assets with GZIP is actually already a very good form of minification.

# Descriptive links
Link descriptions, which are the clickable words in links, help users and search engines better understand your content.

### Code example
```
<a href="https://www.example.com/webpage.html">Keyword in Anchor Text</a>
```

### Best practice
* Use descriptive links (e.g. "Today's menu" instead of "More").
* View this article about it in the [Google Developer Tools](https://developers.google.com/web/tools/lighthouse/audits/descriptive-link-text).

# Error pages
* Create custom 404 pages: [Google Search Console Help](https://support.google.com/webmasters/answer/93641).
* Use a [404 page analyser](https://websiteadvantage.com.au/404-Error-Handler-Checker#heading) to check it.
* Use a 301 page to redirect users to a new page or website when the old URL is not working anymore check out this useful article from [ahrefs]( https://ahrefs.com/blog/301-redirects/).
* Create custom 401 pages if you have sites which require admin rights.
* Users should never be confused about what happened and where to go next.

### Best practice
* Make sure your 404 page is unique and brings the user back to your homepage (check out our 404 page https://www.renuo.ch/de/404)

# Favicons
Favicons are small icons that appear in your browser's address bar, page tabs and bookmarks menu.
Usually, a favicon is 16 by 16 pixels and stored as an ICO file (gif and png are supported as well, however).
Your site should be using and correctly implementing a favicon. 
This helps brand your site and make it easy for users to navigate to your site among a list of bookmarks.

Tools that you can use to generate favicons for your website:

* https://www.favicon-generator.org/
* https://realfavicongenerator.net/

### Best practice
* Ensure your site has a favicon for each page
* The favicon should have enough contrast ratio
* Ensure that the favicon stays perceptible also when resized really small
* Keep the favicon as simple as possible (no photorealistic icons, max two colours, etc.)

# Font usage & formats
It is important to keep as much website content in readable text format (instead of graphic images of desired fonts) for good SEO and to maintain good search engine rankings.
Don't include too many different fonts and variants, as this will negatively impact the site load performance. Include only what is actually used and needed.

### Best practice
Use one of these main font formats: 
* TrueType Font (TTF, most common)
* Web Open Font Format (WOFF, specifically designed for use on webpages)
* WOFF2 (with improved compressing)
* Embedded OpenType (EOT, supported only by IE)

Each font family should be provided in all of these formats, so that the browser can choose the most optimised version supported.

# Google Maps
The visibility of a website in the search results can be increased if it also appears in the search engine map. 
So if the website belongs to a business or other location that can be showing up on a map, you should add it to [Google My Business](https://www.google.com/business/).

### Best practice
* Add all the important information about the business/website
* Always keep opening hours up to date
* Read and reply to reviews
* Add photos

# Heading tags
HTML heading tags are titles or subtitles that you want to display on a webpage.

Your webpage should be using at least one H1 and one H2 HTML header tag. Header tags are not visible to users, but help clarify and support the overall theme or purpose of your page to search engines. 

The H1 tag represents the most important heading, e.g., the title of the page or blog post. 
The H2 tag represents the second most important headings on the webpages, e.g., the subheadings.

### Code example
```
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Best practice
* Use one, individual H1 on every page (visible) containing the main keyword.
* Use an individual H2, H3 and H4 tag on every page.
* Too many heading tags on a page can make it hard for users and search engines to scan the content and determine where one topic ends and another begins.

# HTML compression
The size of all the HTML code on a webpage should be under the average webpage's HTML size of 33 Kb. Faster loading websites result in a better user experience, higher conversion rates, and generally better search engine rankings. To reduce the HTML size use HTML compression. HTML compression plays an important role in improving website speed by finding similar strings within a text file and replacing them temporarily to reduce overall file size.

### Best practice
* Optimise encoding and transfer size of text-based assets, see [Google Developers Tools](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer).
* Minify strip comments.
* Deliver CSS, JavaScript, HTML with GZIP. GZIP is of practically no use for images.

### Check
* Google lighthouse can identify issues with HTML compression.

# HTTPs
A website must be using HTTPS, a secure protocol for sending/receiving data over the Internet. 
Using HTTPS indicates that an additional encryption/authentication layer was added between client and server. 
HTTPS should be used by any site that collects sensitive customer data such as credit card information. 
Even for sites that do not collect such data, switching to https helps users by improving privacy and overall security. 

### Links and further resources
* https://en.wikipedia.org/wiki/HTTPS
* https://www.cloudflare.com/learning/ssl/what-is-https/

### Check
When using Cloudflare, https will be configured automatically for us. 
The application should also be configured to support https. In Rails for example, check that `config.force_ssl = true` in `config/environments/production.rb`

# Image alt tags
An image alt tag or alt description is written text that appears in place of an image if an image cannot be displayed (e.g. due to broken image source, slow internet connection, etc.). The alt attribute provides alternative information, and it allows search engines to better crawl and rank the website. Using relevant keywords and text in the alt attribute can help both users and search engines better interpret the subject of an image.

### Code example
```
//good example
<img src="img/a_cat_picture.jpg" alt="a lovely cat picture">

//bad example
<img src="img/a_cat_picture.jpg">
```

### Best practice
* Use descriptive filenames as image alt tags in target language.
* Use keywords in alt-tags in target language.
* Adding images to a [sitemap](https://developers.google.com/search/docs/advanced/sitemaps/image-sitemaps) helps search engines discover images that might not be found otherwise (such as images a site reaches with JavaScript code).

# Image caching
Your page should use image expire tags, which specify a future expiration date for your images. Users browsers will see this tag and cache the image in their browser until the specified date (so that it does not keep re-fetching the unchanged image from your server). This speeds up your site the next time returning visitors arrive at your site and require the same image.

# Image optimisation
Images often represent the largest part of downloaded bytes on a webpage and occupy a considerable part of the visible area. Therefore, image optimisation can often save the largest amount of bytes and achieve significant performance improvements for a website.

### Best practice
* Use small images (< 200 KB) that load quickly
* Choose the right image format: 
  * Instead of gifs use `<video>`: e.g. [Video formats](https://github.com/renuo/seo-checklist/blob/performance-1/video-formats.md) and https://web.dev/replace-gifs-with-videos/
  * Fine detail with highest resolution: `png` or `SVG`
  * Optimising a photo, screenshot, or a similar image asset: `jpeg`
  * If you use a WebView to render content in your platform-specific application: `WebP`
* Choose the correct level of compression: Use PNG and JPEG compression tools such as https://tinypng.com/, Imagemin (suggested by Google) or [ImageOptim](https://imageoptim.com)
* Serve responsive images with the `srcset` tag
* Use image CDNs to optimise images

Source: [web.dev Fast load times - Optimise your images](https://web.dev/fast/#i18n.paths.fast.topics.optimize_your_images)

### Check
* Google lighthouse can identify issues with image sizes

### Code example
Convert PNG to JPEG (settings from Google PageSpeed insights v4)

```
convert $IMG.png -sampling-factor 4:2:0 -strip -quality 85 -interlace JPEG -colorspace sRGB $IMG.jpg
```

As a special trick you can add `-gaussian-blur 0.05` to the above command to get much smaller (but blurry) images.
This can work very well for backgrounds.

# Inline CSS

## HTML Style-Attributes
Avoid inline CSS like `<p style="font-size: 16px">`: Inline CSS attributes unnecessarily increase page size, and can be moved to an external CSS stylesheet. Removing inline CSS properties can improve page loading time and make site maintenance easier.

## Prefer external files over <style>-Tags
Prefer external files over style-Tags in the HTML:

```html
<style>
  body {
    font-size: 14px;
  }
</style>
```

## (optional) Critical CSS
Since CSS-Files can become large and downloading them can get slow especially on slow connections, this makes CSS a render-blocking resource. If performance is bad, this can be improved with a technique called `Critical CSS`. The idea is to move CSS which is relevant for everything above-the-fold (all content a viewer sees on page load, before scrolling), so that no additional request is needed to fetch these styles. The remainder of the CSS can be loaded asynchronously.

**Note:** Aim to keep above-the-fold content under 14 KB (compressed).

Further reading: https://web.dev/extract-critical-css/

# JavaScript Caching
A page should be using caching headers for all JavaScript resources. Users browsers will check for these headers and, if
any, will cache the JavaScript resources until the specified date (so that it does not keep re-fetching the unchanged
file from your server). This speeds up your site the next time returning visitors arrive at your site and require the
same JavaScript resource.

### Code example
Cache larger files,
eg.

````javascript
self.addEventListener('install', (event) => {
  event.waitUntil(
    caches.open('v1').then((cache) => {
      return cache.addAll([
        './sw-test/',
              ...
        './sw-test/gallery/bountyHunters.jpg',
        './sw-test/gallery/myLittleVader.jpg',
        './sw-test/gallery/snowTroopers.jpg'
      ]);
    })
  );
});
````

### Best practice
* Enable PWA `<meta content="yes" name="apple-mobile-web-app-capable">`
    * [Using the application cache](https://developer.mozilla.org/en-US/docs/Web/HTML/Using_the_application_cache)
* Use CDNs for external libraries
* Google lighthouse can identify issues with Javascript caching

# JavaScript minification
External JavaScript files must be minified. Minified files reduce page size and overall load time.

### Best practice
* Minimize external JavaScript files with an online JS minifier such as [JSCompress](https://jscompress.com/), [Closure Compiler](https://closure-compiler.appspot.com/home) or [JSMin](https://www.crockford.com/jsmin.html).

### Check
* Google lighthouse can identify issues with Javascript minification

# Keywords

### Best practice
* Use max. 1 Keyword per page.
* Don’t use any meta keywords, as they are not used by google anymore and give competitors data about the keywords you are targeting, see: [Webmaster Central Blog](https://webmasters.googleblog.com/2009/09/google-does-not-use-keywords-meta-tag.html).
* Do not stuff keywords or unnatural phrasing - these times are long gone.

### Keyword density
* Check your keyword density: [Keyword density analysis tool](https://imninjas.com/seo-tools/keyword-density/).
* Make sure you also incorporperate keywords that are relevant to that specific topic.

# Lazy loading
Lazy loading is a technique that defers loading of non-critical resources at page load time. Instead, these non-critical resources are loaded at the moment of need. 

### Best practice
* Lazy Load image `<img loading=lazy>`
* Lazy Load fonts `<link remil="preload">`
* [Lazy Loading in Ruby (Turbo Links)](https://turbo-showcase.herokuapp.com/)
* [Google Developers Guide](https://developers.google.com/search/docs/guides/lazy-loading)

# Media queries
For public websites, your page should implement responsive design functionalities using the media query technique.
Media query techniques allow different presentation and content to be served depending on the output device, helping ensure that your website renders optimally on all devices and platforms. The '@media' rule allows different style rules for different screen sizes. Use a mobile-first approach.

### Code example
```css
// This applies from 0px to 600px
body {
  background: red;
}

// This applies from 600px onwards
@media (min-width: 600px) {
  body {
    background: green;
  }
}

```

### Best practice
* Always use `min-width`, never `max-width` and never ever both.
* Refactor old code which is not yet mobile first.

# Meta description
Your webpage's meta description is an HTML tag that is intended to provide a short and accurate summary of your page. Search engines use meta descriptions to help identify the page's topic - they may also use meta descriptions by displaying them directly in search engine results. Accurate and inviting meta descriptions can help boost both your search engine rankings and a user's likelihood of clicking through to your page.

### Code example
```
<head>
 <meta name="description" content="This is the description of this page and its content.">
</head>
```

### Best practice
* Use an individual meta description for every page in target language.
* Use meta description with up to 150 characters and keep in mind that on mobile devices only 120 characters are displayed.

# Mobile-friendly tap targets
Tap targets are the areas of a web page that users on touch devices can interact with. Buttons, links, and form elements all have tap targets.
Many search engines rank pages based on how mobile-friendly they are. Making sure tap targets are big enough and far enough apart from each other makes your page more mobile-friendly and accessible.

### Best practice
* Targets should be bigger than 48px x 48px and further apart than 8px. See more at https://web.dev/tap-targets/

# Navigation structure
Users and search engines want to find relevant content as fast as possible. 
A clean navigation structure helps to indicate what information is valuable, and bots can easily understand the hierarchy of important pages and less important ones.

Also, a good navigation can influence the results of sitelinks (a list of direct links to pages on your website) in the search results.

![sitelinks](https://neilpatel.com/wp-content/uploads/2014/08/1-quicksprout-in-serps.png "sitelinks example from neilpatel.com")

### Best practice
* Make your hierarchy logical.
* Create a URL structure that follows your navigation hierarchy.
* Keep the number of main categories between two and seven.
* Try to balance the number of subcategories within each category.
* Use a shallow depth navigation structure. A shallow website (that is, one that requires three or fewer clicks to reach every page) is far more preferable than a deep website (which requires lengthy strings of clicks to see every page on your site).
* Write your navigation links descriptively. If your site is all about building model trains, it’d be much better to have "Model Train Parts" than "Products".
* When you create your navigation, keep the coding simple. HTML and CSS are your safest approach.
* [How to Create a Site Structure That Will Enhance SEO](https://neilpatel.com/blog/site-structure-enhance-seo)


# No follow tags
For good search rankings, make sure to add the “nofollow” attribute to external links (links to websites that you don’t own) which you don't want a search engine to follow. 

This is extremely useful in cases where you provide user generated content on your website, where anyone could write a comment or article containing links to boost their own website rankings.

### Code example
Normal link:
```html
<a href="http://example.com">Example Website</a>
```

Link with the nofollow tag:
```html
<a href="http://example.com" rel="nofollow">Example Website</a>
```

# Open graph properties
In addition to the Schema.org metadata it can be helpful to add support for Facebook’s Open Graph protocol. This metadata format improves the user experience when your content is shared on their corresponding social network.

### Code example
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta property="og:title" content="The Rock" />
  <meta property="og:type" content="video.movie" />
  <meta property="og:url" content="https://example.com/" />
  <meta property="og:image" content="https://example.com/image.png" />
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>...</title>
</head>
<body>
  ...
</body>
</html>
```

### Best practice
* Best practice is to use these 5 properties: og:url, og:title, og:description, og:images and og:type.
* [How to use open graph properties](http://ogp.me/).
* Test your Open Graph markup with the [Facebook Object Debugger Tool](https://developers.facebook.com/tools/debug/).

# Page caching
A page cache saves dynamically generated pages and serves the pre-generated (cached) page to reduce server load and site loading time (by avoiding the re-loading and execution of PHP scripts).

### Best practice
* Use server caching.
* Use browser caching: expires headers, cache-control headers.

# Page size
A typical web page is made up of several files that may include HTML, CSS, Javascript, or image files, as well as other resources. The page size is made up of all the files that make up the page.

### Best practice
* Optimise images (Resize). To improve the speed of your website it is important to consider compressing or resizing images to the recommended size per file of 200 KB.
* Avoid unnecessary custom fonts.
* Minify resources.
* Employ Content Delivery Networks (CDN) (For example Google Fonts).
* Remove old / duplicate code.
* Separate javascript and css per use-case (e.g. Admin Page needs upload / User doesn't).
* Move javascript loading to the bottom of the file in order to have HTML rendered before!

# Page title
A document title is an HTML tag that defines the title of a page.
This tag displays a page title in search engine results, at the top of a user's browser, and also when a page is bookmarked in a list of favorites.
The contents of a page title can have significant implications for search engine optimisation and should be chosen carefully.
Hence, a concise, meaningful and descriptive title tag that accurately reflects your page's topic is important for ranking well in search engines.

A page title ideally identifies the page uniquely. This usually results in constructs like

> 1. MyWebsite - About Us
> 1. MyWebsite - Features
> 1. MyWebsite - Pricing

### Code example
```
<head>
 <title>Page Title</title>
</head>
```

### Best practice
Some rules to follow when chosing a page title (taken from mdn):
> * Avoid one- or two-word titles. Use a descriptive phrase, or a term-definition pairing for glossary or reference-style pages.
> * Search engines typically display about the first 55–60 characters of a page title. Text beyond that may be lost, so try not to have titles longer than that. If you must use a longer title, make sure the important parts come earlier and that nothing critical is in the part of the title that is likely to be dropped.
> * Don't use "keyword blobs." If your title is just a list of words, algorithms often reduce your page's position in the search results.
> * Try to make sure your titles are as unique as possible within your own site. Duplicate—or near-duplicate—titles can contribute to inaccurate search results.
>
> Source: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title#page_titles_and_seo

Gnerally valid:
* Use a unique, descriptive title per page (65 characters) in target language.
* Use the page's keyword in the title tag.

# Pagination
The correct pagination of a page is a challenging and much discussed topic. Most content management systems offer a solution, but it is not always suitable for SEO. In result individual pages can be excluded from the index.

### Best practice
* Avoid duplicate content.
* Consider disallowing indexing of subpages [Block indexing](https://knowledge.hubspot.com/reports/how-do-i-block-pages-from-being-indexed-by-search-engines).
* Each subpage should provide the Robots meta tag «index, follow».
* Subpages, like all other pages, should refer to themselves by means of self-referential Canonical tags. Google always recommends self-referencing Canonical tags for more clarity.
* Important content elements (e.g. for SEO) should only be on one page - the first - to prevent duplicate content.
* The subpages all have the same Title Tag and Meta Description. Alternatively, the page number can also be shown in the meta description and or in the title tag.
* In order to keep the click depth low for an enormous number of subpages, a suitable page linking strategy should be found. The reason for this is that Google does not usually crawl pages with a too high click depth, which means that they cannot be indexed.

# Responsive Webdesign

### Best practice
* For public websites, your page should implement responsive design functionalities using the media query technique.
Media query techniques allow different presentation and content to be served depending on the output device, helping ensure that your website renders optimally on all devices and platforms. The '@media' rule allows different style rules for different screen sizes.
* Develop mobile first: [Google Developer Help](https://developers.google.com/search/mobile-sites/mobile-seo/responsive-design).
* Consider limited network bandwith.
* Test your mobile friendliness: [Search Console Test](https://search.google.com/test/mobile-friendly) and [Lighthouse](https://developers.google.com/web/tools/lighthouse/).

### Code example
```css
// This applies from 0px to 600px
body {
  background: red;
}

// This applies from 600px onwards
@media (min-width: 600px) {
  body {
    background: green;
  }
}

```

### Best practice
* Always use `min-width`, never `max-width` and never ever both.
* Refactor old code which is not yet mobile first.

# Robots
**Generally you can not block access to your website if it's accessible on the web.**
Protect your page with a password if needed.

`robots.txt` is being used to manage crawler traffic and to avoid visits from inside your own page.
Links from external pages will still show up in search engine result pages.

To manage what is shown in the search results, use Robots meta tag, `data-nosnippet` and `X-Robots` HTTP header.

### Code example
* `robots.txt`
  ```
  Sitemap: https://www.yourwebsite.ch/sitemap.xml
  User-agent: *
  Disallow: /kasse
  Disallow: /cart
  Disallow: /account
  ```
* Robots `meta` HTML tag:
  ```html
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
  ```html
  <p>This text can be shown in a snippet
  <span data-nosnippet>and this part would not be shown</span>.</p>
  ```

### Best practice
* If a specific page should not be crawled, the use of "disallow" in the robots.txt file is recommended.
* Annotate your content with [tags, attributes and headers](https://developers.google.com/search/docs/advanced/robots/robots_meta_tag)
* Check the [Search Console Help](https://support.google.com/webmasters/answer/6062608)

### Check
* Synchronize crawler access rules with your sitemap
* Check your `robots.txt` for entries you don't want to have indexed and annotate the content with meta tags.

# Safe browsing
Google's safe browsing API identifies websites that have malware or exhibit phishing activity. Any site containing malware or suspicious for phising activity is seen as a threat to the online community and is often penalized by search engines. 

### Best practice
* Check regularly if your website is listed as suspicious (and if there is no malware or phishing activity found) with a [safe browsing checker](https://transparencyreport.google.com/safe-browsing/).

### wg-operations (for Renuoees only)
The wg-operations team will discuss the possibility to automate this check.

# SEO friendly URLs
In order for URLs and links to be SEO friendly, they should contain keywords relevant to the page's topic, and contain no spaces, underscores or other characters. 
You should avoid the use of parameters when possible, as they make URLs less inviting for users to click or share. 
Search engines's suggestions for URL structure specify using hyphens or dashes (-) rather than underscores (_). 
Unlike underscores, search engines treat hyphens as separators between words in a URL.

### Best practice
* Provide clean URLs without fragment identifiers (# or #!).
* Use hyphens as word separators.
* Avoid URLs with Umlaute. Use ae, oe, ue, etc. instead, see: [Search Console Support](https://support.google.com/webmasters/forum/AAAA2Jdx3sUn_XASERbfzw/?hl=en&gpf=%23!msg%2Fwebmasters%2Fn_XASERbfzw%2FKt1fG7jKCQAJ&msgid=Kt1fG7jKCQAJ).
* Use keywords in the URL in the target language.
* When possible, place content on the same subdomain to preserve authority. (Recommended: https://example.com/blog, less ideal: https://blog.example.com)

# Server side performance
Server side performance can affect SEO heavily.
A slow page increases jump rate of users and decreases the number of pages indexed by search engines. It has also bad effects on rating.
Tools like Newrelic should be installed on the application and monitored to identify the slowest pages and increase performance.

### Best practice
* Avoid N + 1 Queries
* Follow framework and language best practices
* Server cache for frequent requests
* Remove old / duplicate code (Clean code)

# Server signature
A server signature is the public identity of your web server and contains sensitive information that could be used to exploit any known vulnerability. Turning your server signature OFF is considered a good security practice to avoid disclosure of what software versions you are running.

### Best practice
* Check if your server signature ist turned off with [this](https://seositecheckup.com/tools/server-signature-test) or [this](http://security.firewallmonitor.org) tool.

### Check
When using Cloudflare, the server signature will be turned off automatically for us. 

# Site loading speed
Page speed is an important factor in search engine rankings and overall site success. Pages that take longer than 5 seconds to load can lose up to 50% of users. Faster webpages result in higher traffic, better conversions and increased sales over slower loading pages.

Follow the other best practices to improve the speed (Optimise images. Enable compression. Minify CSS, JavaScript, and HTML. Remove render-blocking JavaScript. etc.)

### Best practice
* [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)
* [WebPageTest](http://webpagetest.org/)
* [Test My Site](https://www.thinkwithgoogle.com/intl/en-gb/feature/testmysite)

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

# Social media linking
A page should be connected to one or more of the popular social networks. Social signals have become increasingly important as ranking factors for search engines to validate a site's trustworthiness and authority.

### Best practice
* Link to social media.
* Use share options.

# Structured data
Search engines use HTML microdata specifications (or structured data markups) to better understand the content of a site and create rich snippets in search results (which helps increase click-through rate to a site).

### Best practice
* View Google's guide for getting started with microdata: [How to structure data](https://developers.google.com/search/docs/guides/intro-structured-data).
* Check the [Google Search Gallery](https://developers.google.com/search/docs/guides/search-gallery) for structured data you might want to use.
* Check this [starter guide](https://moz.com/learn/seo/schema-structured-data).
* Find here the [schema hierarchy](https://schema.org/docs/full.html) and here the [schema documentation](https://schema.org/docs/documents.html).
* Test your structured data with this [testing tool](https://search.google.com/structured-data/testing-tool/u/0/).

# Trailing slashes 
Trailing slashes at the level of a path are problematic because search engines consider them to be a different URL. https://example.com/fish does not equal https://example.com/fish/. This situation should be avoided, as search engines may interpret such content as duplicate content. 

### Best practice
Set a Canonical link to the preferred URL variant so that search engines know which of the two URLs to index.
If you use Rails check https://work.stevegrossi.com/2013/02/21/remove-trailing-slashes-in-your-rails-app/

### Note
Trailing slashes at the end of a hostname are no problem. http://www.example.com equals http://www.example.com/.

# Translated URLs – How to handle languages

### Best practice
* Keep the content for each language on separate URLs. Don't use cookies to show translated versions of the page. Consider cross-linking each language version of a page. That way, a French user who lands on the German version of your page can get to the right language version with a single click.
* Search engines use the content of the page to determine its language, but the URL itself provides human users with useful clues about the page's content.
* Recommended URL structures:
  * *http://example.de*
  * *de.example.com*
  * *example.com/de*
* There is generally no need to "hide" the duplicates by disallowing crawling in a `robots.txt` file or by using a "noindex" robots meta tag. However, if you're providing the same content to the same users on different URLs (for instance, if both example.de/ and example.com/de/ show German language content for users in Germany), you should pick a preferred version and redirect (or use the rel=canonical link element) appropriately. In addition, you should follow the guidelines on rel-alternate-hreflang to make sure that the correct language or regional URL is served to searchers. 

More information here: https://webmasters.googleblog.com/2011/12/new-markup-for-multilingual-content.html

## Specifying language and location
The `hreflang` attribute can specify the language, optionally the country, and URLs of equivalent content. 
By specifying these alternate URLs, our goal is to be able to consolidate signals for these pages, and to serve the appropriate URL to users in search. 
Alternative URLs can be on the same site or on another domain.

## Example usage
To explain how it works, let's look at some example URLs:
* http://www.example.com/ - contains the general homepage of a website, in Spanish
* http://es-es.example.com/ - is the version for users in Spain, in Spanish
* http://es-mx.example.com/ - is the version for users in Mexico, in Spanish
* http://en.example.com/ - is the generic English language version

### Code example
On all of these pages, we could use the following markup to specify language and optionally the region:

```
<link rel="alternate" hreflang="es" href="http://www.example.com/" />
<link rel="alternate" hreflang="es-ES" href="http://es-es.example.com/" />
<link rel="alternate" hreflang="es-MX" href="http://es-mx.example.com/" />
<link rel="alternate" hreflang="en" href="http://en.example.com/" />
```

Keep in mind that all of these annotations are to be used on a per-URL basis. You should take care to use the specific URL, not the homepage, for both of these link elements. 

More information here: https://support.google.com/webmasters/answer/182192?hl=en

# URL redirects
Redirects often cause search engine indexing issues and can also lead to some minor loading delays. Google recommends removing or keeping redirects to a minimum. One redirect may be acceptable, particularly if the URL is redirecting from a non-www version to its www version, or vice-versa.

### Best practice
* recommended for SEO:
  * 307, "Moved Permanently"
* NOT recommended for SEO:
  * 301, "Moved Temporarily"
  * Meta Refresh `<http-equiv="refresh" content="0; url=https://example.com/">`

# Simple URL structures
While it's important for to represent URLs in a user-friendly way (see [SEO friendly URLs](seo-friendly-urls.md) it's also
important to be aware what your URL structure means for the content. For example filters can produce duplicated content.

### Best practice
* Block robots-access to dynamically created search results (in [robots-txt.md](robots-txt.md) or with `nofollow`).

### Check
* Do you build content dynamically based on query parameters (e.g. documents or searches)?
* Consult the [Google Developer Docs](https://developers.google.com/search/docs/advanced/guidelines/url-structure)

# Video formats
Large GIFs are inefficient for delivering animated content. Consider using MPEG4/WebM videos for animations and PNG/WebP for static images instead of GIF to save network bytes.

### Best practice
Check [the following link](https://web.dev/replace-gifs-with-videos/) for the best practices for this topic.

### Code example
* Use MPEG4 as a legacy option

```
ffmpeg -i my-animation.gif -b:v 0 -crf 25 -f mp4 -vcodec libx264 -pix_fmt yuv420p my-animation.mp4
```

* Use WebM for browsers that support it. WebM videos are much smaller than MP4 videos, but not all browsers support WebM so it makes sense to generate both.

```
ffmpeg -i my-animation.gif -c vp9 -b:v 0 -crf 41 my-animation.webm
```

* Compare the difference to see if it's useful

* Use the video on the webpage:

```
<video autoplay loop muted playsinline>
  <source src="my-animation.webm" type="video/webm">
  <source src="my-animation.mp4" type="video/mp4">
</video>
```

### Check
* Google lighthouse can identify issues with large GIF files.


# More links
* [Google SEO Starter Guide](https://support.google.com/webmasters/answer/7451184)
* [Official news on crawling and indexing sites for the Google index](https://webmasters.googleblog.com/)
* [SEO Cheat Sheet](https://d2eeipcrcdle6.cloudfront.net/seo-cheat-sheet.pdf)
