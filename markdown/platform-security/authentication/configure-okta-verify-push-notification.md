---
title: Configure push notification \(Okta Verify\)
description: Configure Okta Verify to receive push notifications for secure and convenient identity verification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-okta-verify-push-notification.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Push notification - Okta verify, Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Configure push notification \(Okta Verify\)

Configure **Okta Verify** to receive push notifications for secure and convenient identity verification.

## Before you begin

Role required: auth\_factors\_admin

The push notification authentication factor on **Okta** must be enabled. To learn more, see [Okta Support Center](https://support.okta.com/help/s/article/Enable-Okta-Verify-Push-Notification-in-OIE?language=en_US).

**Note:**

-   Currently, only **Okta Verify** is supported for push notifications with ServiceNow AI voice agents.
-   The users must have the **Okta Verify** app installed and configured on their phones.

## Procedure

1.  Log in to your Okta admin account.

2.  Navigate to **Security** &gt; **API**.

3.  Select **Tokens**.

    \[Omitted image "okta-admin-console.png"\] Alt text: Okta Admin Console

4.  Select **Create** token to create token and copy its value.

    For example, `O0EYJEm|b34aYViOYaav3KnqxsItV_mPI9_p2N46Cc`.

5.  On the instance, open the **Connection &amp; Credential Alias** record.

    For example, `<instance_url>/sys_alias.do?sys_id=692e16a0ffb72210d487ffffffffff1b`.

    \[Omitted image "okta-configuration-push.png"\] Alt text: Connection &amp; Credential Alias record

6.  Select **New** under the Connections tab.

7.  Specify the following field on the **HTTP\(s\) Connections** form.

    -   Name
    -   Connection alias
    -   Connection URL
    \[Omitted image "okta-configuration-push-1.png"\] Alt text: HTTP\(s\) Connections

8.  Select the **Search** icon next to Credentials to add new **API Key Credentials**.

    \[Omitted image "okta-configuration-push-2.png"\] Alt text: API Key Credentials

9.  Specify the **Name** and **API Key** on the API Key Credentials form.

    **Note:** The API key should be prefixed with ‘SSWS'. If the copied token value is `00iJ88ydm9ZLnDNE8AeGsmjcUC-ZFyCt3pts2pNTwZ` you must provide the value as `SSWS 00iJ88ydm9ZLnDNE8AeGsmjcUC-ZFyCt3pts2pNTwZ`.

    \[Omitted image "okta-configuration-push-3.png"\] Alt text: API Key Credentials

10. Select **Submit** to submit the API Key Credentials.

11. Select **Submit** on the Connection record.

    \[Omitted image "okta-configuration-push-4.png"\] Alt text: HTTP\(s\) Connections record completion


