---
title: Encrypting sensitive data in Individual Life Claims
description: Individual life claims contain personal or sensitive data fields that may require encryption. As an administrator for Individual Life Claims, you should take precautions to ensure that these fields are encrypted with Column Level Encryption. That way, you help to preserve the data privacy of your organization.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Individual Life Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Encrypting sensitive data in Individual Life Claims

Individual life claims contain personal or sensitive data fields that may require encryption. As an administrator for Individual Life Claims, you should take precautions to ensure that these fields are encrypted with Column Level Encryption. That way, you help to preserve the data privacy of your organization.

## Overview of encrypting data in Individual Life Claims

The Individual Life Claims data model enables you to record the details for individual benefits claims. Individual Life Claims includes a death benefit claim workflow that covers the entire claim life cycle, from the first-notice-of-loss \(FNOL\) to the case closure. For more information, see [Individual Life Claims workflows](individual-life-claims-workflows.md).

You may choose to encrypt fields that contain sensitive data by using Column Level Encryption.

## Sensitive data in a death benefit claim

In a death benefit claim, several fields may contain sensitive information.

The following table lists some fields that can contain sensitive data.

**Note:** This list isn’t definitive. Your data encryption and privacy requirements might differ based on your implementation.

|Field|Description|
|-----|-----------|
|Deceased|Name of the deceased individual in the claim.|
|Incident description|Details of the incident for the loss of life event.|
|Attachments|Supporting documents and files that are related to the claim. This field can contain sensitive information such as a death certificate.|

## Encrypting the sensitive data

Fields in Individual Life Claims can be encrypted by using Field Encryption. For more information, see Field Encryption.

**Parent Topic:**[Setting up Individual Life Claims](setting-up-individual-life-claims.md)

