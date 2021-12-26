# Storage Pricing

## EBS

* Charges per GB per month for *provisioned* storage, not the actual use
* Additional charges may be taken for *provisioned* IOPS
* Additional charges may be taken for *S3 snapshots* per month

## S3

* Charges per GB per month for *consumed* storage, i.e. the actual storage use
* Additional charges may be taken for *requests*:
  * PUT, COPY, POST (browser-based PUT), LIST $/1000 (depends on region) (free 2000 in sum)
  * GET $/1000 (depends on region) (free 20 000 requests)
