# JavaScript Caching

A page should be using caching headers for all JavaScript resources. 
Users browsers will check for these headers and, if any, will cache the JavaScript resources until the specified date (so that it does not keep re-fetching the unchanged file from your server). 
This speeds up your site the next time returning visitors arrive at your site and require the same JavaScript resource.


## Check

* Google lighthouse can identify issues with Javascript caching
