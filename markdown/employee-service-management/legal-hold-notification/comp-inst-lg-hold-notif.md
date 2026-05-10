---
title: Components installed with Legal Hold Notification
description: Various components are installed with Legal Hold Notification.
locale: en-US
release: australia
product: Legal Hold Notification
classification: legal-hold-notification
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Legal Hold Notification, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Components installed with Legal Hold Notification

Various components are installed with Legal Hold Notification.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles

<table id="table_dtg_nfg_xfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Legal hold admin

 \(sn\_Ig\_hold.legal\_hold\_admin\)

</td><td>

Provides the administrative permissions for Legal Hold Notification application and full access to the underlying data.

</td><td>

-   sn\_Ig\_hold.legal\_hold\_config
-   sn\_lg\_hold.legal\_hold\_fulfiller

</td></tr><tr><td>

Legal hold configurator

 \(sn\_Ig\_hold.legal\_hold\_config\)

</td><td>

Provides access to configure data for the Legal Hold Notification application.

</td><td>

sn\_lg\_ops.legal\_config

</td></tr><tr><td>

Legal hold fulfiller

 \(sn\_lg\_hold.legal\_hold\_fulfiller\)

</td><td>

Provides fulfiller access to all Legal Hold Notification records.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

Custodian

</td><td>

Responsible for preserving the data related to the legal hold.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr></tbody>
</table>## Tables

<table id="table_ixd_fj1_qfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Legal holdsn\_lg\_matter\_legal\_hold

</td><td>

Stores legal hold matters.

</td></tr><tr><td>

Legal hold custodiansn\_lg\_hold\_custodian

</td><td>

Stores custodian details.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Hold Notification reference](../concept/lg-hold-notif-ref.md)

