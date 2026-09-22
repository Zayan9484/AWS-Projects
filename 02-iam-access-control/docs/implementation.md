# Implementation record

1. Launch the production and development EC2 test resources (`myec2` and `ec2_dev`). The screenshots show Amazon Linux and a launch without a key pair; this exercise tested console authorization rather than SSH.
2. Assign the development tag `Env=development`.
3. Create `DevEnv_policy` using the JSON policy editor. See the [transcribed policy](../policies/development-ec2-lab-policy.json).
4. Configure an account alias for console sign-in.
5. Create `DevGroup`, attach the policy, and add `user1` with console access.
6. Sign in as the test user and open EC2 in the instances' region.
7. Attempt **Stop instance** on production; record the authorization failure.
8. Attempt the same action on development; verify Stopped while production stays Running.

[README with inline evidence](../README.md) · [Complete screenshot index](../screenshots/README.md)

The original notes advise deleting lab resources afterward. No cleanup confirmation is retained, so completion of cleanup is not claimed.
