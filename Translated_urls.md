# Translated URLs – How to handle languages

## Best practice

* Keep the content for each language on separate URLs. Don't use cookies to show translated versions of the page. Consider cross-linking each language version of a page. That way, a French user who lands on the German version of your page can get to the right language version with a single click.
* Search engines use the content of the page to determine its language, but the URL itself provides human users with useful clues about the page's content.
* Recommended URL structures:
  * *<http://example.de>*
  * *de.example.com*
  * *example.com/de*
* There is generally no need to "hide" the duplicates by disallowing crawling in a `robots.txt` file or by using a "noindex" robots meta tag. However, if you're providing the same content to the same users on different URLs (for instance, if both example.de/ and example.com/de/ show German language content for users in Germany), you should pick a preferred version and redirect (or use the rel=canonical link element) appropriately. In addition, you should follow the guidelines on rel-alternate-hreflang to make sure that the correct language or regional URL is served to searchers.

More information here: <https://webmasters.googleblog.com/2011/12/new-markup-for-multilingual-content.html>

## Specifying language and location

The `hreflang` attribute can specify the language, optionally the country, and URLs of equivalent content.
By specifying these alternate URLs, our goal is to be able to consolidate signals for these pages, and to serve the appropriate URL to users in search.
Alternative URLs can be on the same site or on another domain.

## Example usage

To explain how it works, let's look at some example URLs:

* <http://www.example.com/> - contains the general homepage of a website, in Spanish
* <http://es-es.example.com/> - is the version for users in Spain, in Spanish
* <http://es-mx.example.com/> - is the version for users in Mexico, in Spanish
* <http://en.example.com/> - is the generic English language version

### Code example

On all of these pages, we could use the following markup to specify language and optionally the region:

```
<link rel="alternate" hreflang="es" href="http://www.example.com/" />
<link rel="alternate" hreflang="es-ES" href="http://es-es.example.com/" />
<link rel="alternate" hreflang="es-MX" href="http://es-mx.example.com/" />
<link rel="alternate" hreflang="en" href="http://en.example.com/" />
```

Keep in mind that all of these annotations are to be used on a per-URL basis. You should take care to use the specific URL, not the homepage, for both of these link elements.

More information here: <https://support.google.com/webmasters/answer/182192?hl=en>
