# Threat Model

What threats we think of when we design our tool and process.

## Tainted Artifacts

> Attackers may pose as a vetted maintainer and/or offer binaries that may be compromised.

Solutions:

1. Consume binaries liste only from [official channels](https://jreleaser.org/guide/latest/install.html).
2. Valid artifacts are always available from [https://github.com/jreleaser/jreleaser/releases](https://github.com/jreleaser/jreleaser/releases).
3. JReleaser provides SLSA attestations, checksums, SBOMs, and digital signatures for all its release assets. Use appropriate tools to verify these claims.

## Malware from third party extensions

> JReleaser allows running arbitrary code via [hooks](https://jreleaser.org/guide/latest/reference/hooks/index.html) and [extensions](https://jreleaser.org/guide/latest/extensions/index.html).

Solutions:

1. Only run code from trusted sources.
2. Review the code provided by a 3rd-party extension or ad-hoc scripts before using it in your project.
