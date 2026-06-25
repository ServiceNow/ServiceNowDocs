---
title: Masked
description: The masked variable inserts a field that masks the text entered.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/masked.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of service catalog variables, Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Masked

The masked variable inserts a field that masks the text entered.

Each character entered is displayed as an asterisk \(\*\). Use this variable to ask users for sensitive or confidential data such as passwords.

By selecting the **Use encryption** check box, you can configure the variable to encrypt its value using various encryption algorithms before storing in the database. These values can only be decrypted by using now\_GR.variables.var\_name.getDecryptedValue\(\) on RITM, Catalog Task, or any task extension record created using a record producer.

**Note:** By default, the **Use encryption** field is set to true to ensure secure storage of information.

On the variable editor, you can also decrypt and encrypt the values of a masked variable using the **Show** and **Hide** buttons. These buttons are not available for a fulfiller \(itil\) without the catalog\_view\_masked role. You can only view the value that you specified while requesting.

<table id="table_lrq_5vv_vdb"><tbody><tr class="sub-head"><td rowspan="2">

Action

</td><td colspan="3">

Roles

</td></tr><tr class="sub-head"><td>

Requester

</td><td>

Fulfiller with the catalog\_view\_masked role

</td><td>

Fulfiller without the catalog\_view\_masked role

</td></tr><tr><td>

View or hide the encrypted value on catalog forms

</td><td>

Yes

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr><tr><td>

Edit the encrypted value on catalog forms

</td><td>

Yes

</td><td>

Not applicable

</td><td>

Not applicable

</td></tr><tr><td>

View or hide the encrypted value on the variable editor

</td><td>

Yes

</td><td>

Yes

</td><td>

No

</td></tr><tr><td>

Edit the encrypted value on the variable editor

</td><td>

Yes**Note:** If the masked variable is read-only on the variable editor, the variable value is not editable

</td><td>

Yes**Note:** If the masked variable is read-only on the variable editor, the variable value is not editable

</td><td>

No

</td></tr></tbody>
</table>\[Omitted image "VariableMaskedVarTypesG.png"\] Alt text: A masked variable

**Parent Topic:**[Types of service catalog variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/r_VariableTypes.md)

**Related topics**  


[Attachment]()

[Break]()

[Check box]()

[Container start, container split, and container end]()

[Date, Date and time, and Duration]()

[Email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/email.md)

[HTML]()

[IP Address]()

[Label]()

[List collector]()

[Lookup multiple choice]()

[Lookup select box]()

[Custom and Custom with label]()

[Multi-line text]()

[Multiple choice]()

[Numeric scale]()

[Reference]()

[Requested for]()

[Rich Text Label]()

[Select box]()

[Single-line text]()

[UI page]()

[URL]()

[Wide single-line text]()

[Yes/No]()

[Variable support in various channels]()

