# AWS Projects

Hands-on AWS labs completed during my cloud training in 2023 and reorganized here as portfolio projects.

These projects show what I actually configured and tested in AWS at the time. They are learning projects, not production deployments.

## Projects

| Project | What it demonstrates | AWS services / concepts |
|---|---|---|
| [S3 Static Website Hosting](./01-s3-static-website/) | Hosting and validating a static website from Amazon S3, including troubleshooting public access | Amazon S3, static website hosting, object access, website endpoints |
| [IAM Least-Privilege Access Control](./02-iam-access-control/) | Separating development and production EC2 access and validating allowed vs denied actions | IAM, EC2, user groups, custom policies, resource tagging |

Each project includes its implementation notes, validation evidence, screenshots, and the original lab notes retained for reference.

## Repository Structure

```text
AWS-Projects/
├── 01-s3-static-website/
│   ├── README.md
│   ├── docs/
│   └── screenshots/
└── 02-iam-access-control/
    ├── README.md
    ├── docs/
    └── screenshots/
```

## Note

The AWS console and some recommended practices have changed since these labs were completed in 2023. Where relevant, I have added current security notes without rewriting the historical implementation as something I did not originally perform.
