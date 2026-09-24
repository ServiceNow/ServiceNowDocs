---
title: Signature generation during source control commit
description: Generate Code Signing signatures automatically when you commit application files to source control from a trusted instance. The signatures are added to the same update set as their source records and are pushed to the remote repository together.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/c\_cs\_commit\_signing.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Code Signing, source control, commit, signature generation, ServiceNow Studio]
breadcrumb: [Using Code Signing, Code Signing, Platform Security]
---

# Signature generation during source control commit

Generate Code Signing signatures automatically when you commit application files to source control from a trusted instance. The signatures are added to the same update set as their source records and are pushed to the remote repository together.

## Signature generation during commit

Signature generation during source control commit adds signing as an inline step in the application commit flow. When you commit selected files from an application in ServiceNow Studio, the trusted instance generates a signature for each eligible record. The files then advance to the commit confirmation screen. The source records and their signatures are committed to the same update set and pushed to the remote repository together. A commit can't complete while a signature is missing for a selected record, so every record pushed to the repository has a signature.

Without this feature, records are committed to source control without signatures. Signatures are then generated in a separate step through the mass signing jobs, and they don't travel with the source records. As a result, an instance that imports the records can't validate them against a signature that was committed alongside them.

## How it works

During a commit, the trusted instance first verifies that it's eligible to generate signatures. If the instance is eligible, it generates a signature for each selected record that matches a signature configuration, including the record's attachments and embedded Flow Designer records. Each generated signature is written to the same update set as its source record, so the source records and their signatures are committed together. For example, five selected records produce five signatures, for a total of ten files to commit.

## Eligibility for signature generation

A trusted instance generates signatures during commit only when all of the following conditions are met:

-   The feature is turned on for the instance.
-   The instance is opted in to Code Signing, which occurs when the Code Signing Enterprise plugin is installed.
-   The instance isn't enforcing signature validation. Signatures can be generated only on a trusted instance, not on a protected instance.
-   A code signing crypto module with an active signing key exists, which occurs after you upload the signing certificate during the Circle of Trust guided setup.

**Note:**

If an instance isn't eligible, the commit flow runs as it does without the feature. No signatures are generated and no error appears. This behavior keeps the commit flow unchanged for instances that don't use Code Signing.

## Considerations

-   Signature generation during commit applies to records committed from an application in ServiceNow Studio. To sign records created directly on the instance, use the mass signing jobs or the Standalone Signing Tool.
-   Records with a delete action aren't signed during commit. If such a record has a previous signature, that signature isn't included in the update set and is removed by the orphan signatures cleanup job.
-   This feature generates signatures. It's works independently of signature validation, which is the separate enforcement step performed on a protected instance.

-   **[Generate signatures when committing to source control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)**  
Turn on signature generation during commit and commit application files from ServiceNow Studio. Eligible records are signed automatically and pushed to the remote repository with their signatures.

**Parent Topic:**[Using Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/using-code-signing.md)

**Related topics**  


[Generate signatures when committing to source control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)

