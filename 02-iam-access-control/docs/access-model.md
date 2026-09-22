# Access Model

## Objective

The lab tested a simple least-privilege scenario:

> A restricted user should be able to manage the development EC2 resource used in the exercise, but should not have the same permission against the production EC2 resource.

## Components

| Component | Purpose |
|---|---|
| Development EC2 instance | Resource the restricted user was intended to manage |
| Production EC2 instance | Resource that should remain outside the user's permitted scope |
| Custom IAM policy | Defined the restricted access used in the lab |
| IAM user group | Central point for assigning the policy |
| Test IAM user | Identity used to validate the effective permissions |
| Resource tags / labels | Distinguished development from production resources |

## Authorization Flow

```text
IAM User
   |
   v
IAM Group
   |
   v
Custom Policy
   |
   +--> Development EC2: expected action allowed
   |
   +--> Production EC2: same action denied
```

## Why the Test Matters

A policy is not validated simply because it can be created successfully.

The useful part of this exercise was signing in as the restricted identity and checking both sides of the authorization boundary:

- a permitted action should work; and
- an out-of-scope action should fail.

That provides practical evidence that the access model behaved differently for the two environments.

## Historical Limitation

The original policy JSON is not currently stored as a separate file in this repository, so this documentation does not attempt to recreate its exact statements, actions, or conditions.
