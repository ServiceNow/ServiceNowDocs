---
title: Configure trusted certificate authorities
description: Configure certificate authorities \(CAs\) that your organization trusts and activate the certificate authority trust policy so that certificates from other authorities are flagged as untrusted. Configure certificate authorities \(CAs\) that your organization trusts and activate the certificate authority trust policy so that certificates from other authorities are flagged as untrusted.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/itom-visibility/add-trusted-certificate-authorities.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
keywords: [certificate authorities, trusted CA, policies]
breadcrumb: [Configure, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Configure trusted certificate authorities

Configure certificate authorities \(CAs\) that your organization trusts and activate the certificate authority trust policy so that certificates from other authorities are flagged as untrusted.

## Before you begin

Role required: sn\_itom\_cac.admin

## Procedure

1.  Navigate to **All** &gt; **Cryptographic Asset Compliance**.

2.  Select the Settings icon \[Omitted image "settings-display-icon.png"\] Alt text:.

3.  If **Policies** is not already selected, select it in the **Settings** tab.

4.  In the Policy form, select **Certificate authority trust**.

5.  Add trusted CAs.

    1.  Select the **Policy builder** tab.

    2.  In the Data sources panel, select **Add**.

        **Note:** If the **Add** button is not visible, select **Create copy** to duplicate the policy version.

    3.  Complete the fields in the Add API Variable dialog box.

        |Field|Description|
        |-----|-----------|
        |Label|Display name for the variable, for example, `Trusted CA List`.|
        |Name|Internal name that the policy uses to reference the variable.|
        |Type|Data type of the variable. Select **Data Array**.|
        |Mandatory|Option that determines whether a value is required for the variable.|
        |Description|Notes about the variable.|
        |Default value|The CAs that your organization trusts, as a JSON array of quoted names. For example, `["Test CA 1","Test CA 2"]`.|

    4.  Select **Save**.

6.  Publish the policy version.

    1.  In the Policy builder tab, select **Publish**.

    2.  Confirm the publication by selecting **Publish without testing** in the Publish without testing dialog box.

7.  Activate the policy.

    1.  In the Certificate authority trust form, select **Activate**.

    2.  Confirm the activation by selecting **Activate** in the Activate Policy dialog box.


## Result

The Certificate authority trust policy is active with the list of CAs that your organization trusts. Certificates issued by an authority not in your trusted list are flagged with the trusted CA risk indicator.

**Related topics**  


[Manage PaCE policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/pace-admin-manage-policies.md)

