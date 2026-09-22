# Amazon S3 Static Website Hosting

## Overview

This project documents a hands-on AWS lab I completed in 2023 to understand how a static website can be hosted directly from Amazon S3.

The objective was to create an S3 bucket, upload a web page, enable static website hosting, resolve an initial access issue, and verify that the site could be reached through the S3 website endpoint.

## What I Implemented

- Created an Amazon S3 bucket for website content.
- Uploaded the static website file to the bucket.
- Tested direct access and observed that the object was not publicly reachable by default.
- Enabled **Static website hosting** and configured the index document.
- Adjusted the access settings required for this public website lab.
- Validated the final website through the S3 website endpoint.
- Documented the implementation with screenshots.

## Architecture

```text
User Browser
     |
     v
S3 Website Endpoint
     |
     v
Amazon S3 Bucket
     |
     v
Static Web Content
```

## AWS Concepts Practiced

- S3 buckets and objects
- Static website hosting
- Index documents
- Object/public access
- Difference between an object URL and an S3 website endpoint
- Basic troubleshooting of S3 access errors

## Project Evidence

- [Implementation walkthrough](./docs/implementation.md)
- [Validation and troubleshooting](./docs/validation-and-troubleshooting.md)
- [Screenshot evidence index](./screenshots/README.md)
- [Original 2023 lab notes](./docs/original-lab-notes.pdf)

## Security Note

This was a learning lab designed to make a static website publicly accessible from S3. The original implementation used the public-access approach available in the lab at that time.

For a production website today, I would normally evaluate a design using **CloudFront in front of a private S3 origin**, HTTPS, and tighter access controls rather than treating a publicly readable S3 website bucket as the default production architecture.

## Status

**Completed** - static website successfully hosted and validated in the lab environment.
