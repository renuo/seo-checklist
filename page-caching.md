# Page caching
A page cache saves dynamically generated pages and serves the pre-generated (cached) page to reduce server load and site loading time (by avoiding the re-loading and execution of PHP scripts).

# Best practice
* Use server caching: page caching, action caching, fragment caching: [Actionpack page caching](https://github.com/rails/actionpack-page_caching).
* Use browser caching: expires headers, cache-control headers.
