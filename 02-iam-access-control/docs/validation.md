# Validation results

| Test as user1 | Observed | Evidence |
|---|---|---|
| View the instances | Both visible | [Initial list](../screenshots/two-running-ec2-instances.png) and final result |
| Stop production (`myec2`) | Denied: no identity-based policy allows `ec2:StopInstances` | [Authorization failure](../screenshots/production-stop-denied.png) |
| Stop development (`ec2_dev`) | Stopped; production remains Running | [Final states](../screenshots/development-stopped-production-running.png) |

These observations support the tested StopInstances boundary. They do not prove all EC2 operations are correctly restricted, that tag-edit denial was separately tested, or that resources were later deleted.

The policy text added during documentation cleanup was transcribed from the policy screenshot and checked for valid JSON. This was not a fresh AWS deployment or a rerun of the original lab.
