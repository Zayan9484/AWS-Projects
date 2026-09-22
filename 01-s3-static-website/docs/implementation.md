# Implementation record

The lab was performed through the AWS Management Console.

1. Create an S3 bucket and upload `index.html`.
2. Open the object URL; observe `AccessDenied`.
3. The original notes describe enabling static website hosting with `index.html` as the index document. The retained hosting screenshot shows the initial disabled state, not the saved enabled configuration.
4. Edit Block Public Access, enable ACLs under Object Ownership, and select **Make public using ACL** for the HTML object.
5. Refresh the object URL. The final screenshot shows the HTML page loading.

See the [project README](../README.md) for inline configuration and result images and the [screenshot index](../screenshots/README.md) for every step.

The final screenshot does not show a website endpoint. The original HTML source is not retained in this repository, so no reconstructed source is presented as the original upload. Resource cleanup is not demonstrated by the retained evidence.
