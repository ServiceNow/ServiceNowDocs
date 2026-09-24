---
title: Create an application registry record
description: Create an application registry record to provide client ID and client secret for authenticating the requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/jira-setup-cc-app-reg.html
release: brazil
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [Option 2: Using OAuth authentication \(Client Credentials grant type\), Jira Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create an application registry record

Create an application registry record to provide client ID and client secret for authenticating the requests.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the application registry record. For example, `Jira Client Credentials OAuth`.|
    |Client ID|Client ID generated when the OAuth 2.0 integration was created in Atlassian Developer console.|
    |Client Secret|Client secret generated when the OAuth 2.0 integration was created in Atlassian Developer console.|
    |Default Grant type|Grant type used to establish the token. Select **Client Credentials**.|
    |Token URL|OAuth server token endpoint. Enter: `https://auth.atlassian.com/oauth/token`.|
    |Token Revocation URL|OAuth server token revocation endpoint. Enter: `https://auth.atlassian.com/oauth/token`.|
    |Active|Select the check box.|

5.  In the **OAuth Entity Scopes** tab, create these entity scope records.

    |Name|OAuth scope|
    |----|-----------|
    |Classic scopes|`manage:jira-configuration manage:jira-project manage:jira-webhook read:jira-work read:jira-user write:jira-work`|
    |Granular Scopes|`delete:sprint:jira-software read:issue-details:jira read:jql:jira read:sprint:jira-software write:sprint:jira-software read:board-scope:jira-software read:project:jira`|

6.  Right-click the form header and click **Save**.

    The record is saved and a OAuth Entity Profile record under the **OAuth Entity Profiles** tab.

7.  Click the **OAuth Entity Profiles** tab and open the default profile record.

8.  Verify these values.

    -   **Grant type** is set to **Client Credentials**.
    -   Scope records previously created are listed under the **OAuth Entity Profile Scopes** related list.
9.  Click **Update**.


