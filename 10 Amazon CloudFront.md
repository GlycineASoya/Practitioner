# Amazon CloudFront

* The service is a edge-cache for Content Delivery Netwrok (CDN) and caches the content on the Edge Location
* It doesn't have it's own data, the source (called `Origins`) can be S3, LB
* It leverages the rules (`Behaviours`)
* It has it's own domain name __CNAME__ or __ALIAS__ records
* It leverages SSL certificates
* It supports RTMP and HLS streaming
