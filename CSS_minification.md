# CSS minification
All CSS files used in your page must be minified. Minified files reduce page size and overall load time.

### Best practice
* The minification is performed by default when using the standard Rails setup, or using other build tools such as Webpack in a production mode.

### Check
* Google Lighthouse can identify non-minified CSS resources.

**Note:** Delivering assets with GZIP is actually already a very good form of minification.