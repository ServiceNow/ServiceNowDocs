---
title: Signature Verification in Code Signing
description: Signature verification helps confirm that records, scripts, and other signed content originate from trusted sources and remain unaltered.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [signature verification, multiple signatures]
breadcrumb: [Using Code Signing, Code Signing, Platform Security]
---

# Signature Verification in Code Signing

Signature verification helps confirm that records, scripts, and other signed content originate from trusted sources and remain unaltered.

## Signature Verification process

Signature verification is a core part of Code Signing. When the MID Server processes a signed record or script, it checks the attached digital signature against the certificate used to generate it. This verification helps confirm that the content is authentic and hasn’t been modified since it was signed. If the signature is valid and the certificate is trusted, the system permits the operation. If the signature is invalid or the certificate is untrusted, the system blocks execution to protect the environment.

## Support for multiple signatures per record

With the Australia release, there's enhanced support for verifying multiple signatures on a single record. A record might collect signatures over time from different certificates, such as customer-owned certificates and ServiceNow® build certificates. To provide more accurate verification, the system now groups signatures by certificate and evaluates the most recent signature in each group. Compared to the previous model, which evaluated only the most recent signature on the record, this approach provides a more reliable verification process.

Verification succeeds if any certificate group contains a valid latest signature. This improvement ensures that a valid signature from one certificate isn’t overlooked simply because a newer signature from another certificate is invalid. This approach helps avoid failures after upgrades and helps recognize all valid signatures from any trusted source.

**Parent Topic:**[Using Code Signing](../../encryption/concept/using-code-signing.md)

