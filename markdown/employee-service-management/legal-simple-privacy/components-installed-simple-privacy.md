---
title: Components installed with Legal Simple Privacy
description: Several types of components are installed with activation of the Legal Simple Privacy application, including user roles.
locale: en-US
release: xanadu
product: Legal Simple Privacy
classification: legal-simple-privacy
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Legal Simple Privacy Reference, Legal Simple Privacy, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Components installed with Legal Simple Privacy

Several types of components are installed with activation of the Legal Simple Privacy application, including user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Roles

<table id="table_lqh_3b4_wvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_lg\_simple\_priva.privacy\_fulfiller

</td><td>

Provides fulfiller access for working on assigned privacy requests and matters.

</td><td>

sn\_lg\_ops.legal\_user

</td></tr><tr><td>

sn\_lg\_simple\_priva.privacy\_admin

</td><td>

Application-specific system administrator role for the Legal Simple Privacy application, which provides administrative access for the application and full access to the underlying data.

</td><td>

-   sn\_lg\_simple\_priva.privacy\_fulfiller
-   sn\_lg\_simple\_priva.privacy\_config

</td></tr><tr><td>

sn\_lg\_simple\_priva.privacy\_config

</td><td>

Provides access to configure data for the Legal Simple Privacy application such as search sources.

</td><td>

None

</td></tr></tbody>
</table>## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Privacy and Data Security\[sn\_lg\_ops\_privacy\_and\_data\_security\]

</td><td>

Stores the details of a privacy assessment request.

</td></tr><tr><td>

Privacy and Data Security\[sn\_lg\_matter\_privacy\_and\_data\_security\]

</td><td>

Stores the details of any legal matters created.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Simple Privacy Reference](../concept/legal-simple-privacy-reference.md)

