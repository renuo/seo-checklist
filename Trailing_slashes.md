# Trailing slashes 
Trailing slashes at the level of a path are problematic because search engines consider them to be a different URL. https://example.com/fish does not equal https://example.com/fish/. This situation should be avoided, as search engines may interpret such content as duplicate content. 

### Best practice
Set a Canonical link to the preferred URL variant so that search engines know which of the two URLs to index.
If you use Rails check https://work.stevegrossi.com/2013/02/21/remove-trailing-slashes-in-your-rails-app/

### Note
Trailing slashes at the end of a hostname are no problem. http://www.example.com equals http://www.example.com/.