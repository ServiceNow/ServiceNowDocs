---
title: Specify the virtual machine managers \(VMMs\) for which you are tracking IBM licenses
description: Specify the virtual machine managers \(VMMs\), such as VMware vCenter Servers and IBM Hardware Management Consoles \(HMCs\), for which you want to track IBM licenses. You can track licenses for IBM software that is discovered within these specified VMMs only.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Specify the virtual machine managers \(VMMs\) for which you are tracking IBM licenses

Specify the virtual machine managers \(VMMs\), such as VMware vCenter Servers and IBM Hardware Management Consoles \(HMCs\), for which you want to track IBM licenses. You can track licenses for IBM software that is discovered within these specified VMMs only.

## Before you begin

Role required: sam\_admin or sam\_user

## Procedure

1.  From your ServiceNow instance, navigate to **Workspaces** &gt; **Software Asset Workspace**.

    The Software Asset Workspace launches in a new tab.

2.  Open the License operations view.

3.  From the left navigation menu of the License operations view, navigate to **IBM ASP Integration** &gt; **Devices to scan**.

4.  Select **New**.

5.  On the IBM Licensing VM Manager form, fill in the fields.

<table id="table_wp2_ztg_svb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

VM Manager

</td><td>

VMM for which you want to track IBM licenses.

</td></tr><tr><td>

Type

</td><td>

Type of VMM. Select one of the following options:-   **vCenter**
-   **ESX Server**
-   **HMC**
-   **All AIX Servers**


</td></tr></tbody>
</table>6.  Select **Submit**.


**Parent Topic:**[Authorized SAM Provider \(ASP\) integrations for IBM](../concept/ibm-asp-integration.md)

