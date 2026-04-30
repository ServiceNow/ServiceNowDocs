---
title: Accept or reject a component request for inclusion in a component library
description: Review a request for adding a component to a component library and approve or reject it.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Sharing components among applications — Component libraries, Use, DevOps Config, IT Service Management]
---

# Accept or reject a component request for inclusion in a component library

Review a request for adding a component to a component library and approve or reject it.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Someone has requested to add a local component from an application to the component library as a shared component. If there are such requests in a library that need your approval, you see a **Requests** label \(![The Requests label beside the library name in the list.](../image/cdm-comp-library-request.png)\) beside the library name.

Role required: cdm\_admin or cdm\_editor

## Procedure

1.  Navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace**.

2.  Click the component libraries icon \(![Component libraries icon.](../image/icon-component-libraries.png)\) in the left navigation to open the **Component libraries** tab.

3.  Open a component library and select the **Requests** tab.

    **Note:** The **Requests** tab is available only when there’s an open request for adding a component to the library.

4.  Click a requests card to review its config data.

    The config data of the selected card appears in the preview pane.

5.  As required, click accept or reject the request.

<table id="choicetable_mcn_flw_dxb"><thead><tr><th align="left" id="d304574e141">

Approval action

</th><th align="left" id="d304574e144">

Description

</th></tr></thead><tbody><tr><td id="d304574e150">

**Accept a request**

</td><td>

1.  Click **Accept** on the card.
2.  As required, update the fields in the Approve Request pop-up window.
    -   Select a library in the **Target library** field to which the component will be added.
    -   Update the name of the component in the **Component** field.

**Note:** If a component with the same name exists in the library, enter a different name.

    -   Update the description of the component in the **Component description** field.
3.  Add comments about the approval for the requester to see in the request.
4.  Select an action option in the **Additional actions** field to perform after the request is processed.
    -   **No additional actions**: Does not process anything for the latest version of the component.
    -   **Publish version**: Publishes the component version.
5.  Click **Accept**.


</td></tr><tr><td id="d304574e220">

**Reject a request**

</td><td>

1.  Click **Reject** on the card.
2.  Enter the reason of rejection for the requester to see in the request.
3.  Click **Reject**.


</td></tr></tbody>
</table>
## Result

-   The request is removed from the **Requests** tab.
-   Any comments added in the request can be seen by the requester in the app from where the request was submitted.
-   If the request is approved:
    -   The state of the request updates to Accepted.
    -   The component is added to the selected component library as a shared component. Any secret data values \(such as account id or passwords\) for keys, referenced variables, and file attachments in file nodes are not included with the component. You have to replace the file attachments in all such file nodes.

        If the library is available, the component is ready for use in multiple CDM apps.

    -   If you selected **Publish version** in the **Additional actions** field, then the shared component is published.
-   If the request is rejected, the state of the request updates to Rejected.

