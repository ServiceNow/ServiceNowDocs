---
title: Care Team Portal
description: Use the Care Team Portal to create requests for supporting service departments and maintain visibility into all requests created by you or your team.
locale: en-US
release: australia
product: Care Team Operations
classification: care-team-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Care Team Portal

Use the Care Team Portal to create requests for supporting service departments and maintain visibility into all requests created by you or your team.

Care team members often rely on multiple, disconnected systems to report issues, leading to delays, frustration, and a lack of visibility into request status. This disconnection results in duplicate work, unnecessary escalations, and time taken away from patient care.

The Care Team Portal, part of Healthcare Operations Core, centralizes issue reporting and provides real-time visibility into request statuses, reducing frustration and ensuring efficient support.

Pre-installed record producers for ancillary departments, depending on which additional plugins are installed, allow care teams to easily create and track support requests. This enhances productivity and allows teams to focus more on patient care.

The Care Team Portal provides a responsive portal experience that can be used by clinicians in hospitals to report and track issues for support services departments. This experience can be used on a standalone portal or embedded in EMR systems.

![Landing page for Care Team Portal.](../image/care-team-portal-overview.png)

The Care Team Portal can also be embedded within Epic, with access to all features available in the browser experience. For instructions, see [Embedding Care Team Portal in Epic Hyperspace via Hyperdrive](configure-care-team-portal.md).

The following plugins provide preconfigured record producers for use with Care Team Portal:

-   Care Team Operations for Healthcare IT
-   Care Team Operations for Biomed
-   Care Team Operations for Facilities
-   Care Team Operations for Environmental Services

For information on the features available with the Care Team Portal, see [Navigate the Care Team Portal](hcls-cto-using-portal.md).

## Accessing the Care Team Portal

To access the Care Team Portal from a ServiceNow instance, add the portal suffix **/careteam** after the instance URL.

For example,

```
https://<instance name>.service-now.com/careteam
```

## Virtual Agent in Care Team Portal

Virtual Agent, ServiceNow’s conversational bot platform, is available when creating requests from the Care Team Portal.

Virtual Agent can be used to quickly obtain information, decide, and perform common work tasks.

To interact with Virtual Agent, simply select the chat window icon on the bottom right-hand corner of the screen.

For more information on Virtual Agent, see [Virtual Agent as an application design element](https://www.servicenow.com/docs/access?context=virtual-agent&version=australia&pubname=australia-application-development&ft:locale=en-US).

