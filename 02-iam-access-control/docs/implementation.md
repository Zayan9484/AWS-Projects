# Implementation

This document records the sequence used in the original 2023 IAM lab.

## 1. Create Development and Production EC2 Resources

Two EC2 instances were launched to represent separate environments:

- Development
- Production

The environments were differentiated so the access-control test could target one without granting the same access to the other.

## 2. Create the IAM Policy

A custom IAM policy was created for the restricted user scenario.

Its purpose was to permit the required EC2 action for the development resource while leaving the production resource outside the user's permitted scope.

The exact historical JSON is not reproduced because it is not retained as a standalone file in the current repository.

## 3. Configure an AWS Account Alias

An AWS account alias was created as part of the console sign-in workflow used in the lab.

The alias made the account sign-in URL easier to identify than using only the numeric AWS account ID.

## 4. Create the IAM User Group

A dedicated IAM user group was created.

The custom policy was attached to the group so permissions could be managed through group membership rather than by attaching the policy directly to one individual user.

## 5. Create the Test IAM User

A test IAM user was created with AWS Management Console access and added to the restricted group.

This identity was then used to validate the effective permissions.

## 6. Test Production Access

After signing in as the test user, an EC2 management action was attempted against the production instance.

AWS denied the action, showing that the restricted identity did not have the required authorization for that production resource.

## 7. Test Development Access

The corresponding action was then tested against the development instance.

The action succeeded, confirming that the user had the intended development access.

## 8. Clean Up

Temporary lab users, policies, groups, and EC2 resources should be removed after testing when they are no longer required.
