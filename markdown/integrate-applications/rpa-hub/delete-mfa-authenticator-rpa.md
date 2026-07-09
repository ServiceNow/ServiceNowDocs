---
title: Delete a TOTP authenticator in RPA Hub
description: Delete a Time-based One-time Password \(TOTP\) authenticator record in RPA Hub so that you can dissociate it from a bot process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/delete-mfa-authenticator-rpa.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Delete a TOTP authenticator in RPA Hub

Delete a Time-based One-time Password \(TOTP\) authenticator record in RPA Hub so that you can dissociate it from a bot process.

## Before you begin

Familiarize yourself with multi-factor authentication \(MFA\) concepts. For more information, see [Multi-factor authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/mfa-landing.md).

Familiarize yourself with the TOTP authentication in RPA Hub. For more information, see [TOTP authentication in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/totp-authentication-rpa.md).

Create a multi-factor authentication \(MFA\) authenticator record. For more information, see [Create an MFA authenticator in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/create-mfa-authenticator-rpa.md).

Map a TOTP authenticator to a robot credential in RPA Hub. For more information, see [Create a TOTP authenticator in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/map-totp-credential-set-rpa.md).

Verify if the life-cycle stage status of the associated bot process is either set to **Build** or **In Maintenance**.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Credential Management**, select **Robot Credentials**.

4.  Open the robot credential record that you want to dissociate the TOTP authenticator record from.

5.  On the **TOTP Authenticators** tab, select the TOTP authenticator that you want to delete.

6.  Select **Delete**.


**Parent Topic:**[Managing RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/managing-rpa-hub.md)

**Related topics**  


[Retire an MFA authenticator in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/retire-mfa-authenticator.md)

