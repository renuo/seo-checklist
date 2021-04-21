# JavaScript Caching

A page should be using caching headers for all JavaScript resources. Users browsers will check for these headers and, if
any, will cache the JavaScript resources until the specified date (so that it does not keep re-fetching the unchanged
file from your server). This speeds up your site the next time returning visitors arrive at your site and require the
same JavaScript resource.

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

## Best practice and links

* Enable PWA `<meta content="yes" name="apple-mobile-web-app-capable">`
    * [Using the application cache](https://developer.mozilla.org/en-US/docs/Web/HTML/Using_the_application_cache)
* Use CDNs for external libraries
* Google lighthouse can identify issues with Javascript caching

