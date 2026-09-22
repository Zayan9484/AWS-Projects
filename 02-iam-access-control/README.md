# AWS IAM Least-Privilege Access Control Lab

## Overview

This project documents a hands-on AWS IAM lab I completed in 2023.

The goal was to create separate **development** and **production** EC2 resources, assign restricted access to a test IAM user through a user group and custom policy, and then verify that the user could perform an action on the development instance while the same action was denied on the production instance.

## What I Implemented

- Launched two EC2 instances to represent development and production environments.
- Used resource labels/tags to distinguish the two environments.
- Created a custom IAM policy for restricted EC2 access.
- Created an IAM user group and attached the policy to the group.
- Created a test IAM user and added the user to the restricted group.
- Used an AWS account alias as part of the sign-in workflow.
- Signed in as the restricted user and tested permissions.
- Confirmed that the production EC2 action was denied.
- Confirmed that the corresponding development EC2 action was allowed.
- Documented the complete process with screenshots.

## Access Model

```text
Test IAM User
     |
     v
IAM User Group
     |
     v
Custom IAM Policy
     |
     +--------------------+
     |                    |
     v                    v
Development EC2      Production EC2
   Allowed               Denied
```

## AWS Concepts Practiced

- IAM users and user groups
- IAM policies
- Least-privilege access
- EC2
- Resource tagging / environment separation
- Authorization testing
- Explicit validation of allowed and denied actions

## Project Evidence

- [Access model](./docs/access-model.md)
- [Implementation walkthrough](./docs/implementation.md)
- [Validation results](./docs/validation.md)
- [Screenshot evidence index](./screenshots/README.md)
- [Original 2023 lab notes](./docs/original-lab-notes.pdf)

## Important Documentation Note

The current repository does not retain the original IAM policy JSON as a standalone text file. I have therefore documented the access behavior that was actually tested rather than reconstructing or inventing policy code after the fact.

If the original policy file is recovered later, it can be added separately.

## Current Security Perspective

IAM users were appropriate for this learning exercise. For workforce access in a modern production environment, I would also evaluate AWS IAM Identity Center or federation, MFA, short-lived credentials, and tighter role-based access rather than relying on long-lived IAM user credentials.

## Status

**Completed** - restricted access was tested successfully against separate development and production EC2 resources.
