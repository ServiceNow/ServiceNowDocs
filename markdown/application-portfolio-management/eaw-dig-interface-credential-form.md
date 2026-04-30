---
title: Digital interface credentials form
description: short description.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Digital interface credentials form

short description.

## Credentials form fields

**Note:** The ‘Integration user’ and ‘Connection and credential alias’ fields will be editable when the 'Platform Host' field is set to 'ServiceNow' in the related Provider Business Application of the referenced Digital interface. You require the role 'credential\_admin' or 'connection\_admin' to view or set the ‘Connection and credential alias’ field.

<table id="table_skj_pgt_bcc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Digital Interface

</td><td>

Name of the digital interface. This field is auto-populated with the name of the interface that you’re editing. If you want to create the relationship to a different digital interface, use the Lookup icon to select a digital interface.

</td></tr><tr><td>

Number

</td><td>

Unique identifier of the digital interface credential record. This field is automatically generated and can’t be edited. The number starts with the prefix CRED. For example: CRED01001.

</td></tr><tr><td>

Digital Integration

</td><td>

Select a digital integration, where the digital interface is being used as a provider or subscriber digital interface.

</td></tr><tr><td>

Life cycle stage

</td><td>

Select the life cycle stage for the credentials. Choice list includes:-   Design
-   Operational
-   End of Life

</td></tr><tr><td>

Environment

</td><td>

Select the environment type from the choice list.

</td></tr><tr><td>

Life cycle stage status

</td><td>

Select the life cycle stage status for the credentials. The choice list depends on the selection in the **Life cycle stage** field.-   Design-Design
-   Operational-In use
-   End of Life-Retired

</td></tr><tr><td>

Managed by group

</td><td>

Select the name of the group who will manage the credentials.

</td></tr><tr><td>

Credential

</td><td>

Enter the name of the credentials.

</td></tr><tr><td>

Integration user

</td><td>

\(Optional\) Reference to the integration user or service account.

</td></tr><tr><td>

Authentication type

</td><td>

Select the authentication type from the choice list.

</td></tr><tr><td>

Connection and credential alias

</td><td>

Select the connection and credential alias ID from the from the reference field.

</td></tr><tr><td>

Authorization type

</td><td>

Select the authorization type from the choice list.

</td></tr><tr><td>

Credential store URL

</td><td>

Enter the URL where the credentials are stored and can be consulted.

</td></tr><tr><td>

Description

</td><td>

Description about the connection between the digital interface and the documented credentials.

</td></tr><tr><td>

Notes

</td><td>

Enter notes about the credentials.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Relate credentials to a digital interface](../../task/eaw-task/eaw-dig-interface-add-credential.md)

