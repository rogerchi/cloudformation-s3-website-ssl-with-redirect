# cloudformation-s3-website-ssl-with-redirect
YAML CloudFormation template for S3 static website with SSL (HTTPS) with redirect from bare domain to www.

Prerequisites: 
* Existing Route53 hosted zone for the domain name

Creates:
* S3 buckets for website content, bare domain redirect, and logs
* Certificate manager SSL certificate for bare domain and *.domain
* Two CloudFront distributions (one for redirect, one for website)
* Route53 aliases for the CloudFront distributions