# Access model

`user1` inherits `DevEnv_policy` through `DevGroup`.

| Policy element | Scope |
|---|---|
| Conditional Allow | `ec2:*`, resource `*`, condition `ec2:ResourceTag/Env` equals `development` |
| Read visibility | `ec2:Describe*` on `*` |
| Explicit Deny | `ec2:CreateTags` and `ec2:DeleteTags` on `*` |

The development tag is part of the authorization boundary. Blocking tag edits prevents this test identity from changing that label through these EC2 actions.

## What the tests establish

`ec2:StopInstances` failed for production and succeeded for development. Production remained visible because Describe permission was separately allowed. The production error states that no identity-based policy allowed StopInstances for that resource; it is not an explicit Deny of StopInstances.

## Limits

`ec2:*` is broader than a policy limited to the tested stop action. Not every EC2 action has identical resource and condition support. This lab therefore demonstrates a tested tag-based boundary, not exhaustive least privilege across EC2. Tag-edit denial and other actions were not independently tested in the retained screenshots.

[Policy transcribed from screenshot](../policies/development-ec2-lab-policy.json) · [Policy image](../screenshots/tag-based-iam-policy.png)
