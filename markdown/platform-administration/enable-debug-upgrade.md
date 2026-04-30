---
title: Enable and use debug upgrade
description: Enable Debug Upgrade to analyze post-upgrade issues that may require follow up, then disable it when finished with the upgrade debugging session.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Debug upgrade, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Enable and use debug upgrade

Enable Debug Upgrade to analyze post-upgrade issues that may require follow up, then disable it when finished with the upgrade debugging session.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Diagnostics** &gt; **Session Debug**.

2.  Select **Debug Upgrade** to enable the upgrade debugger.

3.  Process a transaction \(for example, load a form\).

4.  Click the **Skipped During Last Upgrade**, **Customer Customized**, or **ServiceNow Modified During Last Upgrade** header to view the appropriate list.

<table id="table_epp_prc_ydb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of record processed during the last upgrade session.

</td></tr><tr><td>

Type

</td><td>

Type of record processed during the upgrade.-   **Business rule**

Server-side script that runs when a record is displayed, inserted, updated, or deleted, or when a table is queried. See [Classic Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

-   **Client script**

Client JavaScript run when client-based events occur. See [Client scripts](https://www.servicenow.com/docs/access?context=client-scripts&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

-   **Data policy**

Policies that enforce data consistency. See [Data policy](../../field-administration/concept/c_DataPolicy.md).

-   **Script include**

Script includes that store JavaScript run on the server. See [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

-   **UI action**

Buttons, links, and context menu items on forms and lists. See [UI actions](../../list-administration/concept/c_UIActions.md).

-   **UI macro**

Discrete scripted components added to the user interface. See [UI macros](https://www.servicenow.com/docs/access?context=c_UIMacros&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

-   **UI page**

Pages used to create and display forms, dialogs, lists, and other UI components. See [UI pages](https://www.servicenow.com/docs/access?context=r_UIPages&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

-   **UI policy**

Policies that change the behavior of information on a form and control custom process flows for tasks. See [UI policies](../../form-administration/task/t_CreateAUIPolicy.md#).

 **Note:** These are the only types of artifacts logged by the Upgrade Debugger.

</td></tr><tr><td>

Last Modified

</td><td>

Date and time the record was last modified.

</td></tr></tbody>
</table>5.  Click **Show more** to view all artifacts.

6.  Click the name of a listed artifact to view the underlying artifact record.

    For example, if you click a Script Include artifact, the underlying Script Include record appears.

7.  To turn off Debug Upgrade and all session debugging after completing your session:

    1.  Navigate to **System Diagnostics** &gt; **Session Debug**.

    2.  Select **Disable All** to disable the upgrade debugger.


**Parent Topic:**[Debug upgrade](../reference/debug-upgrade.md)

