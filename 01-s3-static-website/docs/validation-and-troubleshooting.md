# Validation and Troubleshooting

## Issue Observed

The first browser test returned an access error after the website file had been uploaded to S3.

## Why It Happened

Uploading an object to S3 does not automatically make it publicly readable or turn the bucket into a website.

The lab still required:

1. static website hosting to be enabled;
2. an index document to be configured; and
3. public read access appropriate for the lab.

## Resolution

After configuring static website hosting and the required access settings, the S3 website endpoint was tested again.

## Validation Result

| Check | Result |
|---|---|
| Website file uploaded to S3 | Passed |
| Static website hosting enabled | Passed |
| Index document configured | Passed |
| Website endpoint reachable | Passed |
| Static page loaded in browser | Passed |

## What I Learned

The useful part of this lab was not only hosting the page. It also showed why an S3 object URL, an S3 website endpoint, and object access permissions are separate concepts.

The project screenshots are retained in chronological order in the [screenshots](../screenshots/) folder.
