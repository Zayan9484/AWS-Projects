# Validation and troubleshooting

## Observed failure

The initial object request returned `AccessDenied`. Uploading the file had not made it anonymously readable.

## Resolution recorded

The lab changed public-access settings, enabled ACLs, and used **Make public using ACL** on `index.html`. The subsequent browser screenshot shows the page loading from its S3 object URL.

Static website hosting is a separate feature. An object URL does not require that feature to serve an accessible object, so the initial error should not be attributed solely to disabled website hosting.

| Check | Evidence-based result |
|---|---|
| `index.html` uploaded | Visible in object details and bucket listing |
| Initial access error | `AccessDenied` response captured |
| ACL workflow | Ownership and object-action screenshots retained |
| Page loads through object URL | Confirmed by final browser screenshot |
| Static website hosting enabled | Described in notes; final enabled settings not captured |
| Website endpoint tested successfully | Not demonstrated by retained screenshots |

[Inline evidence](../README.md) · [All screenshots](../screenshots/README.md)
