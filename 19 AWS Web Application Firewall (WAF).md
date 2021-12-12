# AWS Web Application Firewall (WAF)

* It gives Layer 7 OSI Model content filtering
* Block/Allow/Count
* It integrates with Amazon CloudFront
* Protects against:
  * SQL Injections
  * XSS (**Cross**(**X**) **S**ite **S**cripting)
* Blocks on:
  * IP Addresses
  * HTTP Headers/body
  * URI strings
* Rate limiting per client IP
* Managed Rules for common threats:
  * OWASP - The **O**pen **W**eb **A**pplication **S**ecurity **P**roject - an online community that produces freely-available articles, methodologies, documentation, tools, and technologies in the field of web application security
  * Bots
  * **C**ommon **V**ulnerabilities and **E**xposures (CVE)
