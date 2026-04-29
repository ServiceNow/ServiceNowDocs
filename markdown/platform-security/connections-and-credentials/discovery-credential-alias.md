---
title: Credential aliases for Discovery
description: Credential aliases for Discovery allow an administrator to use specific credentials on Discovery schedules. You can configure behaviors for your aliases that determine how strictly the system enforces their use.Create the alias and then add that alias to a credential in the credential record. You can add a credential to multiple aliases and add multiple credentials to a single alias.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Get started with credentials, Connections and Credentials, Access Management]
---

# Credential aliases for Discovery

Credential aliases for Discovery allow an administrator to use specific credentials on Discovery schedules. You can configure behaviors for your aliases that determine how strictly the system enforces their use.

Without credential aliases, Discovery schedules can access all credentials that are defined in the instance. This behavior might not be desirable in some circumstances, particularly for credentials with elevated privileges. Credential aliases provide more control over which credentials a Discovery schedule is allowed to use and prevents the unnecessary exposure of credentials with elevated privileges.

## How credential aliases work

A business rule called **Insert Discovery Affinity &amp; Cred Aliases** \(previously named **Insert Discovery Affinity**\) runs when a record \(a task for performing Discovery\) is inserted into the ECC Queue.

The business rule attaches the credential aliases defined in the Discovery schedule to the probe, so when the probe reaches the MID Server on its way to performing discovery, the MID Server knows exactly which credentials it can use to attempt to access the device the probe was sent to scan.

The MID Server filters credentials by [affinity](c_CredentialAffinity.md) and then by tags, if any exist. Credentials must match all credential tags. The MID Server iterates until it finds a credential that works.

If the business rule determines that an affinity exists for the device, the rule identifies the proper **credential\_id** to use. This is the **__sys\_id__** of the record in the Credentials `[discovery_credentials]` table.

When the platform encounters an affinity with a credential alias value, defined as **credential\_alias** in the business rule, the business rule determines whether or not the credential referenced by the affinity has the specified alias. If it does, the business rule selects the **credential\_id** of the alias and passes that value to the MID Server.

If a credential alias is defined for a schedule and the schedule is configured to use that alias, the schedule will ignore any previously existing credential-to-target affinity—*but only if the credential itself is not associated with any other credential alias*. If the credential does not have any credential alias, any other affinities that exist for the target system are checked.

## Create a Discovery credential alias

Create the alias and then add that alias to a credential in the credential record. You can add a credential to multiple aliases and add multiple credentials to a single alias.

### Before you begin

Role required: admin, credential\_admin \(read access only\), connection\_admin \(read access only\)

### About this task

A Discovery schedule only uses credentials that are contained in the aliases defined for that schedule.

**Note:** If a credential alias is defined for a schedule, it will ignore any previously existing credential affinity between the credential and the target that is discovered in a schedule that is setup to use that credential alias.

### Procedure

1.  Create an alias.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Click **New**.

    3.  Enter a unique name for the alias and select **Credential** for the alias **Type**.

    4.  Click **Submit**.

        The **Credentials** related list appears. You can add new credentials for this alias in this list but not existing credentials.

        ![Credential alias record](../image/DiscoCredAlias.png)

2.  Configure a credential for the new alias.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Select an existing credential from the list or click **New** to create a new credential.

    3.  In the credential record, unlock the **Credential alias** field and select the alias you created.

        ![Credential record with alias defined](../image/DiscoCredforAlias.png)

    4.  Save or submit the record.

3.  Return to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases** and open your new alias.

    The credential you attached to the alias now appears in the related list.

    ![Credential attached to an alias](../image/DiscoAliaswithCred.png)

4.  To create an additional credential for this alias, click **New** in the related list and select a credential type.

    The alias name is pre-populated in the **Credential alias** field of the credential record.

5.  Complete the fields in the form and submit the record.


