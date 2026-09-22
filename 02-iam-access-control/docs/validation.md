# Validation Results

## Test Objective

The lab was successful only if the restricted identity behaved differently against the two EC2 environments.

## Result Matrix

| Test | Expected | Observed |
|---|---|---|
| Restricted user attempts the tested EC2 action on production | Denied | Denied |
| Restricted user attempts the tested EC2 action on development | Allowed | Allowed |

## Interpretation

The validation showed that the IAM configuration enforced the intended separation between development and production for the tested action.

The key lesson was that IAM should be tested from the perspective of the actual restricted identity. Viewing a policy in the console is not enough to prove what a user can or cannot do.

## Evidence

The original screenshots are retained in chronological order in the [screenshots](../screenshots/) folder.

They cover the EC2 setup, IAM policy/group/user configuration, sign-in process, and the final allowed/denied permission tests.
