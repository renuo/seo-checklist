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
