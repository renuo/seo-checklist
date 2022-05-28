# HTTPS

A website must be using HTTPS, a secure protocol for sending/receiving data over the Internet.
Using HTTPS indicates that an additional encryption/authentication layer was added between client and server.
HTTPS should be used by any site that collects sensitive customer data such as credit card information.
Even for sites that do not collect such data, switching to https helps users by improving privacy and overall security.

### Links and further resources

* <https://en.wikipedia.org/wiki/HTTPS>
* <https://www.cloudflare.com/learning/ssl/what-is-https/>

### Check

When using Cloudflare, https will be configured automatically for us.
The application should also be configured to support https. In Rails for example, check that `config.force_ssl = true` in `config/environments/production.rb`
