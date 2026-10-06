# Security Policy

This policy applies to every repository in the KeiaiLab organization
unless a repository ships its own `SECURITY.md`.

## Supported versions

Only the latest minor release of each project receives security fixes.
Upgrade to it before reporting.

## Reporting a vulnerability

Do not open a public issue. Report privately through either channel:

- GitHub: the repository's **Security** tab, then **Report a
  vulnerability** (private vulnerability reporting is enabled for the
  organization).
- Email: support@keiailab.com

Include the affected project and version, reproduction steps, and the
impact you observed.

## Response targets

| Step | Target |
|---|---|
| Acknowledgement | 3 business days |
| Fix or advisory (high/critical) | 30 days |

## Scope: upstream container images

Some charts deploy images that KeiaiLab does not build: `mongo`,
`percona/mongodb_exporter`, `valkey`, and `qdrant`. These are marked
`whitelisted` in Artifact Hub. Report their vulnerabilities upstream
and track upstream advisories.

## Signing and provenance

- Helm charts are PGP-signed. The public key is published in each
  chart repository (for example
  `charts/keiailab-helm-signing-public.asc`); verify with
  `helm verify` or `helm pull --verify`.
- Container images built by KeiaiLab carry build provenance and an
  SBOM attestation.
