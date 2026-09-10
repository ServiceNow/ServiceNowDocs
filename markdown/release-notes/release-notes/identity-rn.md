---
title: Identity release notes
description: The ServiceNow Identity application supports identity mechanisms that enable you to validate the identity of users. Identity was enhanced and updated in the Yokohama release.The ServiceNow Identity application supports identity mechanisms that enable you to validate the identity of users. Identity was enhanced and updated in the Yokohama release.The ServiceNow Identity application supports identity mechanisms that enable you to validate the identity of users. Identity was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Identity release notes

The ServiceNow® Identity application supports identity mechanisms that enable you to validate the identity of users. Identity was enhanced and updated in the Yokohama release.

## About Identity

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Configure AI Agents or AI users by selecting the `AI` option from the **Identity** drop-down menu.
-   Use the `ai_user_admin` role for creating, editing, and role management of AI users. Using the role you can view, create, edit, assign roles to, and delete users with the identity type as `AI`.
-   Use role masking for AI agents and agentic workflows to limit the inherited roles during tool execution, verifying that AI agents run with restricted privileges, minimizing potential security risks and helping prevent unintended actions. To learn more, see [Role masking in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-role-masking.md).

[Yokohama Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-10.md)

-   Use Federated ID to uniquely identify roles across multiple instances. Federated ID provides a unique identifier for roles, making it easier to manage and track them across instances. To know more, see [Exploring Federated ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/federated-id.md).

Yokohama

-   Use the Access Insights module in the ServiceNow® Access Analyzer V4 tool to get access insights of your users, while comparing the user access.
-   Assign the `access_analyzer_admin` role to the users to access and administer the Access Analyzer.

See [Identity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/identity-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Identity is a ServiceNow AI Platform product that is active by default.


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-security-rn-landing.md)

## Yokohama Early Availability

The ServiceNow® Identity application supports identity mechanisms that enable you to validate the identity of users. Identity was enhanced and updated in the Yokohama release.

### What's new

-   **[Access Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/access-insights.md)**

    Use the Access Insights module in the ServiceNow® Access Analyzer V4 tool to get access insights about role or group entitlements that are assigned to the user at a peer-level \(meaning at the same organization, department, and Manager\), while comparing the user access.

    **Important:** Access Insights \(Access Analyzer V4\) is available in the ServiceNow Store. For more information, visit ServiceNow Store.


## Yokohama

The ServiceNow® Identity application supports identity mechanisms that enable you to validate the identity of users. Identity was enhanced and updated in the Yokohama release.

### What's changed

-   **[Access Analyzer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/access-analyzer.md)**

    Assign the `access_analyzer_admin` role to the users to access and administer the Access Analyzer.


