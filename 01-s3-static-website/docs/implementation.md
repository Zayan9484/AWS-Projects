# Implementation

This document records the implementation flow used in the 2023 lab.

## 1. Create the S3 Bucket

A new Amazon S3 bucket was created to hold the static website content.

The bucket acted as the storage layer for the website files.

## 2. Upload the Website File

The static web file was uploaded as an object inside the bucket.

At this stage, simply having an object URL did not mean the website was publicly accessible.

## 3. Test Initial Access

The uploaded object was tested from a browser.

The first access attempt produced an access error because the website content was not yet configured for public website delivery.

This was useful because it showed the difference between storing an object in S3 and intentionally publishing website content.

## 4. Enable Static Website Hosting

Static website hosting was enabled from the bucket properties.

The main website file was configured as the index document.

This created an S3 website endpoint for the bucket.

## 5. Configure Public Website Access

The bucket/object access settings were adjusted so that the static content could be read publicly for the purpose of the lab.

The screenshots preserve the exact console workflow used in 2023.

## 6. Validate the Website

The S3 website endpoint was opened in a browser after the configuration changes.

The website loaded successfully, confirming that:

- the bucket contained the expected website file;
- static website hosting was enabled;
- the index document was configured; and
- the required read access was in place.

## Cleanup

For a temporary lab, unused S3 resources should be removed after testing to avoid unnecessary exposure or future charges.
