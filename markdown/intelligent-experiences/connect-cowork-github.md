---
title: Connect ServiceNow Cowork to GitHub
description: Connect ServiceNow Cowork to GitHub or GitHub Enterprise to enable pull request review, CI checks, read code, and manage issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/connect-cowork-github.html
release: australia
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
breadcrumb: [Connectors in ServiceNow Cowork, Use, ServiceNow Cowork, Enable AI experiences]
---

# Connect ServiceNow Cowork to GitHub

Connect ServiceNow Cowork to GitHub or GitHub Enterprise to enable pull request review, CI checks, read code, and manage issues.

## Before you begin

Role required: sn\_app\_cowork.user

## Procedure

1.  From your user name, navigate to **Settings** &gt; **Connectors**.

2.  Select **Add**.

3.  From the **Connector type** list, select **GitHub**.

4.  In **Hostname**, enter your GitHub host, such as github.com or your GitHub Enterprise hostname.

5.  In the **Token** field, paste your personal access token.

    To obtain a personal access token from GitHub:

    1.  Go to [https://code.devsnc.com/](https://code.devsnc.com/)

    2.  Select the user icon on the top right.

    3.  Go to **Settings** &gt; **Developer Settings** &gt; **Personal access tokens**.

    4.  Select scopes **repo** check box and under **admin.org** select **read.org** check box.

    5.  Copy the token starting with `ghp_` or `gho_`.

6.  Select **Show setup instructions** to see how to get a token through CLI.

7.  In **Label \(optional\)**, enter a name for the connection.

8.  Select **Add Host**.

    Host is added and the token is stored securely.


**Parent Topic:**[Connectors in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/connectors-in-cowork.md)

