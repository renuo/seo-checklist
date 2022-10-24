# Language

It is important to specify the language of an HTML page in the source code so that user agents can display the text of a web page correctly and search engines can show the correct search results to users from different countries. 

## Best practices

Use a lang attribute in the HTML element, that way it is inherited by all other elements and thus also determines the language for the text in the head area. This would not be the case if it were specified in the body element.


```
<html lang="en">
```


If your website contains pages in different languages you can either 
* acquier a different domain for each country, i.e. example.de, example.es, example.it, etc.
* or provide each language version on a corresponding subdomain, i.e. de.example.com, es.example.com, it.example.com, etc.
* or create a corresponding subdirectory for each language, with the main version of the website remaining in the main directory, e.g. example.com/es/ or example.com/it/.
* or finally for dynamic pages add a parameter for the respective language to the URL, e.g. example.com/products.php?lang=es.
