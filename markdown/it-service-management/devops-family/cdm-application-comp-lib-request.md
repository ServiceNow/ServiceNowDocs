---
title: Request to include a component to a component library
description: Submit a request for a component in an application that could be reused across multiple applications to be added to a shared component library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-family/cdm-application-comp-lib-request.html
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Sharing components among applications — Component libraries, Using DevOps Config, DevOps Config, IT Service Management]
---

# Request to include a component to a component library

Submit a request for a component in an application that could be reused across multiple applications to be added to a shared component library.

## Before you begin

**Important:** Starting with the Washington D.C. release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

Role required: cdm\_admin or cdm\_editor

## About this task

While creating data models for their applications, DevOps Config editors and administrators may identify certain components could be reused across multiple applications. They can submit a request to the component library owners to add those components to the library.

**Note:** You can only submit one request for a component for the same library at a time.

## Procedure

1.  Navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace**.

2.  Select the apps icon \(\[Omitted image "icon-applications-nav.png"\] Alt text: Applications icon.\) in the left navigation to open the **Apps** tab.

3.  Open an application and select the **Config data** tab.

4.  Select the shared components icon \(\[Omitted image "icon-shared-components-panel.png"\] Alt text: Shared components icon.\).

    \[Omitted image "cdm-app-shared-comp-request.png"\] Alt text: Shared components pane.

5.  In the Shared components pane, select **+ Create request**.

6.  Enter the details in the request form.

<table id="table_vw1_lz3_bxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Component

</td><td>

Name of the component to be added to the request.**Note:** Config data from the last committed changeset is added to the request, excluding any secret data values for keys, referenced variables, and file attachments in file nodes.

</td></tr><tr><td>

Target library

</td><td>

Component library to which the requested component should be added.Only existing and available libraries are listed in the field.

</td></tr><tr><td>

Component description

</td><td>

Description about the component, such as how it works.

</td></tr><tr><td>

Additional details

</td><td>

More details about the component that could be helpful to the approver during approving.

</td></tr></tbody>
</table>7.  Select **Submit**.

    A request is created for the library owner to add the selected component as a shared component in the target library. The state of the request is set as Pending review and is listed in the Shared components pane.

    You can see all of your requests from the last 30 days and filter them by their state.


## What to do next

While a request is in the Pending review state, you can change its information or withdraw it by selecting the request card in the Shared components pane.

-   To update the request, update the component's description or additional details in the respective fields and select **Update**.
-   To withdraw the request, select **Withdraw**.

The library owner can review and approve or reject the request.

