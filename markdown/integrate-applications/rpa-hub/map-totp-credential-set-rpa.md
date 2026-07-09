---
title: Create a TOTP authenticator in RPA Hub
description: Map a multi-factor authentication \(MFA\) authenticator record with a seed in a robot credential. This mapping results in creating a Time-based One-time Password \(TOTP\) authenticator record in RPA Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/map-totp-credential-set-rpa.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [authenticate unattended robot rpa hub, authenticate bot rpa hub, unattended robot authentication rpa hub, bot authentication rpa hub]
breadcrumb: [Create a robot credential, Configuring credentials, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create a TOTP authenticator in RPA Hub

Map a multi-factor authentication \(MFA\) authenticator record with a seed in a robot credential. This mapping results in creating a Time-based One-time Password \(TOTP\) authenticator record in RPA Hub.

## Before you begin

Familiarize yourself with multi-factor authentication \(MFA\) concepts. For more information, see [Multi-factor authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/mfa-landing.md).

Familiarize yourself with the TOTP authentication in RPA Hub. For more information, see [TOTP authentication in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/totp-authentication-rpa.md).

Create an MFA authenticator record. For more information, see [Create an MFA authenticator in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-mfa-authenticator-rpa.md).

Create a robot credential. For more information, see [Create a robot credential in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-credential-set-botprocess.md).

Do this task only when you select the **Process Type** field as **Unattended** on the Bot process configuration form while you're creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-botprocess.md), [Bot process configuration form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/bot-process-config-form.md), and [Bot Process form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/bot-process-form.md).

Verify that the life-cycle stage status of the associated bot process is set to either **Build** or **In Maintenance**.

Role required: sn\_rpa\_fdn.rpa\_developer,sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

A seed is a secret key of the authenticator that is used to generate the TOTP.

An authenticator application is a third-party software that generates temporary passcodes. Users can use these passcodes with their password to log in to an instance that requires multi-factor authentication \(MFA\).

With TOTP authentication, you can store the seed of the authenticator at the instance level so that your unattended robots can seamlessly authenticate against MFA-enabled applications.

If a TOTP authenticator is using external credential vault, then ensure that the associated external credential vault is active.

In RPA Hub, you can retrieve robot credentials, application credentials, or TOTP seed in two ways:

-   From ServiceNow credentials record \(application credential, robot credential, or TOTP authenticator\).
-   From an external credential vault. For more information, see [External credential vault in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/external-credentials-rpa.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Credential Management**, select **Robot Credentials**.

4.  Select the robot credential record that you want to associate an MFA authenticator record to.

5.  On the **TOTP Authenticators** tab, select **New**.

6.  On the form, fill in the fields.

<table id="table_lgf_nm1_sqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authenticator

</td><td>

MFA authenticator to be mapped to this robot credential. Alternatively, you can select the search icon and select the MFA authenticator.

For example, Okta.

</td></tr><tr><td>

Seed

</td><td>

Secret key of the authenticator that is used to generate the TOTP.This field does not appear if the **External Credential** check box is selected.

</td></tr><tr><td>

External Credential

</td><td>

Select this check box to fetch the seed from external credential vaults.

</td></tr><tr><td>

External Credential Vault

</td><td>

Select an external credential vault record that is used for fetching the seed from an external credential vault.Use the search icon to select an external credential vault record. For example, DemoCyberArk.

Only active external credential vault records are listed here.

This field appears only when the **External Credential** check box is selected.

</td></tr><tr><td>

Subflow Input

</td><td>

Provide a JSON that acts as an input to the subflow mapped in the selected external credential record. This JSON is used by the Subflow REST Step and must contain the necessary information for retrieving seed from the external credential vault.

The value must be in JSON format. You cannot enter an empty JSON value.

For more information about the JSON, see [Steps to configure an external credential vault in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/config-ext-cred-rpa.md).

This field appears only when the **External Credential** check box is selected.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  In the **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


## What to do next

[Use the GetTOTP component in the RPA Desktop Design Studio to generate TOTP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/preview-data-rpa-studio.md).

**Related topics**  


[Delete a TOTP authenticator in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/delete-mfa-authenticator-rpa.md)

[Retire an MFA authenticator in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/retire-mfa-authenticator.md)

