# HTML compression

The size of all the HTML code on a webpage should be under the average webpage's HTML size of 33 Kb. Faster loading websites result in a better user experience, higher conversion rates, and generally better search engine rankings. To reduce the HTML size use HTML compression. HTML compression plays an important role in improving website speed by finding similar strings within a text file and replacing them temporarily to reduce overall file size.

## Best practice

* Optimise encoding and transfer size of text-based assets, see [Google Developers Tools](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer).
* Minify strip comments.
* Deliver CSS, JavaScript, HTML with GZIP. GZIP is of practically no use for images.

## Check

* Google lighthouse can identify issues with HTML compression.
