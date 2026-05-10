---
title: Credential aliases for Orchestration activities
description: Credential alias gives an administrator more control over the credentials used in Orchestration activities.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Get started with credentials, Connections and Credentials, Access Management]
---

# Credential aliases for Orchestration activities

Credential alias gives an administrator more control over the credentials used in Orchestration activities.

This is useful when an activity requires specific credentials to perform a task. You can use a credential tag to assign individual credentials to any activity in a Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.

Credential alias interacts with [credential affinity](c_CredentialAffinity.md) to determine which credentials should be used for an Orchestration activity.

## How credential alias works

A [business rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/business-rules-classic/c_BusinessRules.md) called Insert Discovery Affinity \(renamed from Insert Credential Affinity in the Geneva release\) runs when a record is inserted into the ECC Queue. This rule determines whether a credential affinity exists for the device and identifies the proper credential\_id \(the sys\_id of the record in the Credentials `[discovery_credentials]` table\) to use. When the platform encounters an affinity with a credential alias value defined \(credential\_alias in the business rule\), the business rule determines if the credential referenced by the affinity has the specified alias. If it does, the business rule selects the credential\_id of the credential alias and passes that value to the MID Server. If the credential does not have the specified credential alias, any other affinities that exist for the target system will be checked. If no affinity references an appropriately tagged credential, the MID Server iterates through the Credentials \[discovery\_credentials\] table and selects the credential with the appropriate tag. The MID Server then creates a new affinity for this credential.

